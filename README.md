<img src="https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png" style="margin: 0;">

Welcome yuhengen,

This is the Code Institute student template for Gitpod. We have preinstalled all of the tools you need to get started. You can safely delete this README.md file, or change it for your own project. Please do read it at least once, though! It contains some important information about Gitpod and the extensions we use.

## Gitpod Reminders

To run a frontend (HTML, CSS, Javascript only) application in Gitpod, in the terminal, type:

`python3 -m http.server`

A blue button should appear to click: *Make Public*,

Another blue button should appear to click: *Open Browser*.

To run a backend Python file, type `python3 app.py`, if your Python file is named `app.py` of course.

A blue button should appear to click: *Make Public*,

Another blue button should appear to click: *Open Browser*.

In Gitpod you have superuser security privileges by default. Therefore you do not need to use the `sudo` (superuser do) command in the bash terminal in any of the lessons.

## Updates Since The Instructional Video

We continually tweak and adjust this template to help give you the best experience. Here is the version history:

**October 21 2020:** Versions of the HTMLHint, Prettier, Bootstrap4 CDN and Auto Close extensions updated. The Python extension needs to stay the same version for now.

**October 08 2020:** Additional large Gitpod files (`core.mongo*` and `core.python*`) are now hidden in the Explorer, and have been added to the `.gitignore` by default.

**September 22 2020:** Gitpod occasionally creates large `core.Microsoft` files. These are now hidden in the Explorer. A `.gitignore` file has been created to make sure these files will not be committed, along with other common files.

**April 16 2020:** The template now automatically installs MySQL instead of relying on the Gitpod MySQL image. The message about a Python linter not being installed has been dealt with, and the set-up files are now hidden in the Gitpod file explorer.

**April 13 2020:** Added the _Prettier_ code beautifier extension instead of the code formatter built-in to Gitpod.

**February 2020:** The initialisation files now _do not_ auto-delete. They will remain in your project. You can safely ignore them. They just make sure that your workspace is configured correctly each time you open it. It will also prevent the Gitpod configuration popup from appearing.

**December 2019:** Added Eventyret's Bootstrap 4 extension. Type `!bscdn` in a HTML file to add the Bootstrap boilerplate. Check out the <a href="https://github.com/Eventyret/vscode-bcdn" target="_blank">README.md file at the official repo</a> for more options.

--------

Happy coding!

# SQL Commandds
## Login

In the terminal, type
```
mysql -u root
```

## Create database
```
create database <name>;
```

## List database
```
show databases;
```

## Switch to a database (Make it active)
```
use <name>
```

## Create a new table
```
create table parents (
    parent_id int unsigned auto_increment primary key,
    surname varchar(50) not null,
    proper_name varchar(50) not null
) engine=innodb;
```
## To see all tables
```
show tables;
```

## To see all the columns of a table
```
describe <table name>;
```

## To delete table
```
drop table <name>
```

## To add to table
```
alter table <table name> add <name> <type> not null;
```

## To delete from table
```
alter table <table name> drop <name>;
```

## To modify name in table
```
alter table <table name> rename column <old name> to <new name>;
```

## Add a new foreign key
```
// 1. create the new column
alter table sessions add coach_id int unsigned not null;

// 2. create the foregin key
alter table sessions add constraint fk_coach_id foreign key (coach_id) references coaches(coach_id);
```

## Add rows to table
```
insert into <table name> (<var1>,<var2>) values ("<val1>","<val2>");
```

## See content of table
```
Select * from <table name>;
```