# SQL
## Terminology
**RDBMS** Relational Database Management System, relational referring to relational data (i.e. tables).
**Schema** Like packages/namespaces, groupings of tables expressing some database logical structure. In Oracle SQL its synonymous with the user.
**SQL implementations** There is OracleSQL is an Enterprise Database like PostgreSQL, SQL Server, but there are others like MySQL, MariaSQL, as well as non relational SQL databases (NoSQL).

**Candidate Key** A column that can uniquely identify a row (or entry) and thus is a potential candidate for a primary key.
**Composite Key** A primary key consisting of multiple columns.
**Primary Key** Unique (in that table), non-null candidate key.
**Foreign Key** A key that points to another primary key of a row (either in another table, or the same).

**Multiplicity** Refers to the relationship between linked tables. One-to-One (University, President), One-to-Many (University, Students), Many-to-Many (Students, Teachers). In 1:1, FKs will be within same table. 1:many, FKs will be in the other table. many:many, FKs will be in a junction/transition/join/lookup table.

**Referential Integrity** Enforcing data relationships, changes reflected between foreign keys. No orphans, all child rows must have their parent rows deleted as well.
**Domain Integrity** Column data is restricted to allowed range of allowed type.

**Normalization** A process in which you eliminate redundancy and maintain data integrity.

### Starting point (no normalization)
| SalesStaff |
| --- |
| EmployeeID |
| SalesPerson |
| SalesOffice |
| Age |
| DOB |
| Customer1 |
| Customer2 |
| Customer3 |

### 1st NF (Atomic values, No repeating Columns)
| SalesStaff |
| --- |
| EmployeeID |
| SalesPersonName |
| Age |
| DOB |
| SalesOfficeStreet |
| SalesOfficeCity |
| SalesOfficeState |
| SalesOfficeZip |

| Customer |
| --- |
| CustomerId |
| EmployeeId |
| CustomerName |


### 2nd NF (Remove Partial Dependencies)
| SalesStaff |
| --- |
| EmployeeID |
| SalesPersonName |
| Age |
| DOB |
| SalesOfficeID |

| SalesOffice |
| --- |
| SalesOfficeId |
| SalesOfficeStreet |
| SalesOfficeCity |
| SalesOfficeState |
| SalesOfficeZip |

| Customer |
| --- |
| CustomerId |
| EmployeeId |
| CustomerName |

### 3rd NF (Remove Transitive Dependencies)
| SalesStaff |
| --- |
| EmployeeID |
| SalesPersonName |
| DOB |
| SalesOfficeID |

| SalesOffice |
| --- |
| SalesOfficeId |
| SalesOfficeStreet |
| SalesOfficeZip |

| Customer |
| --- |
| CustomerId |
| EmployeeId |
| CustomerName |

**ERD** Entity-Relational Diagram