# Web App Security

## Many to Many Relationships
Think about the many-to-many association between two edtities: epmloyee and project.
Any given employee can be assigned to multiple project and a project may 
have multiple employees working on it.  If you have an employee table with an emplyee_id
as it's primary key and a project table with project_id as its primary key, then you'll
need a join table to connect both sides.  

##Database Setup
Here is some sample code creating a employee table, project table, and
employee_project table that joins them with employee_id and project_id as 
foreign keys.  
```
CREATE TABLE `employee` (
  `employee_id` int(11) NOT NULL AUTO_INCREMENT,
  `first_name` varchar(50) DEFAULT NULL,
  `last_name` varchar(50) DEFAULT NULL,
  PRIMARY KEY (`employee_id`)
) ENGINE=InnoDB AUTO_INCREMENT=17 DEFAULT CHARSET=utf8;
 
CREATE TABLE `project` (
  `project_id` int(11) NOT NULL AUTO_INCREMENT,
  `title` varchar(50) DEFAULT NULL,
  PRIMARY KEY (`project_id`)
) ENGINE=InnoDB AUTO_INCREMENT=18 DEFAULT CHARSET=utf8;
 
CREATE TABLE `employee_project` (
  `employee_id` int(11) NOT NULL,
  `project_id` int(11) NOT NULL,
  PRIMARY KEY (`employee_id`,`project_id`),
  KEY `project_id` (`project_id`),
  CONSTRAINT `employee_project_ibfk_1` 
   FOREIGN KEY (`employee_id`) REFERENCES `employee` (`employee_id`),
  CONSTRAINT `employee_project_ibfk_2` 
   FOREIGN KEY (`project_id`) REFERENCES `project` (`project_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
``` 
## Model Classes
 Model classes Employee and Project need to be created with JPA annotations:
 ``` 
    @Entity
    @Table(name = "Employee")
    public class Employee { 
     
        @ManyToMany(cascade = { CascadeType.ALL })
        @JoinTable(
            name = "Employee_Project", 
            joinColumns = { @JoinColumn(name = "employee_id") }, 
            inverseJoinColumns = { @JoinColumn(name = "project_id") }
        )
        Set<Project> projects = new HashSet<>();
    }
    @Entity
    @Table(name = "Project")
    public class Project {    
     
        @ManyToMany(mappedBy = "projects")
        private Set<Employee> employees = new HashSet<>();
        
    }
```
Both the Employee class and Project class refer to one another, creating
a bidirectional association between them.  



### Reading Links
[Hibernate Many To Many](https://www.baeldung.com/hibernate-many-to-many) <br>
[Security: A humurous overview](https://scholar.harvard.edu/files/mickens/files/thisworldofours.pdf) <br>


[Return to Homepage](https://claudiobailon.github.io/reading-notes/401.html)


 
>Education is not the learning of facts,
>but the training of the mind to think.
> -- <cite>[Albert Einstein][1]</cite>

[1]:https://www.goodreads.com/quotes/6137386-education-is-not-the-learning-of-facts-but-the-training 