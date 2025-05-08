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
    FacultyID VARCHAR(20) NOT NULL PRIMARY KEY,
    Department VARCHAR(25) NOT NULL,
    Salary FLOAT
);

``` 

Now create Library table

```
CREATE TABLE Library (
    BookName VARCHAR(256),
    BookCode VARCHAR(20),
    FacultyID INT,
    Rollnumber INT,
    FOREIGN KEY (FacultyID) REFERENCES FacultyDetails(FacultyID),
    FOREIGN KEY (Rollnumber) REFERENCES StudentDetails(Rollnumber)
);
```

Now altering the table to add one more row to the `library` table,

```

ALTER TABLE Library
ADD COLUMN ReturnDate DATE;

```
