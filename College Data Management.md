Create a Database called `College Database` and table `StudentDetails`

```

-- Lets create College database

CREATE DATABASE College_Database;


-- Now create tables of each department on Students, Faculty and Library.

CREATE TABLE StudentDetails (
    FirstName VARCHAR(256) NOT NULL,
    LastName VARCHAR(25) NOT NULL,
    RollNumber VARCHAR(15) NOT NULL PRIMARY KEY,
    Branch VARCHAR(5) NOT NULL,
    CurrentYear VARCHAR(10) NOT NULL,
    YearOfPass TINYINT NOT NULL
);

```

Now go with the flow that creates `Faculty_Details`  

```

CREATE TABLE FacultyDetails (
    FacultyID INT PRIMARY KEY AUTO_INCREMENT,
    FirstName VARCHAR(256) NOT NULL,
    LastName VARCHAR(25) NOT NULL,
    Department VARCHAR(25) NOT NULL,
    Salary FLOAT
);

``` 



