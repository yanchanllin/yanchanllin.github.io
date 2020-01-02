---
layout: post
title:      "Review On SQL "
date:       2020-01-01 23:54:20 -0500
permalink:  review_on_sql
---


I learned SQL a long time ago, then continued on learning other languages and frameworks. Today I want to write down some notes for SQL:


```
CREATE TABLE cats (
id INTEGER PRIMARY KEY,
name TEXT,
age INTEGER,
breed TEXT);
```

```
INSERT INTO cats (name, age, breed)
VALUES ("Maru", 3, "Scottish Fold");
 
INSERT INTO cats (name, age, breed)
VALUES ("Hana", 1, "Tabby");
```

```
CREATE TABLE owners (id INTEGER PRIMARY KEY, name TEXT);
```

Use the following statement to add this column:
```
ALTER TABLE cats ADD COLUMN owner_id INTEGER;
```

Let's make a new owner:
```
INSERT INTO owners (name) VALUES ("mugumogu");
```

Check that we did that correctly with the following statement:

```
SELECT * FROM owners;
```
or update something:
```
UPDATE cats SET owner_id = 1 WHERE name = "Maru";
```

To check the new updated table:
```
SELECT * FROM cats WHERE owner_id = 1;
```
