# Oracle APEX Region Plug-In - MT APEX FancyTree
A region plug-in that shows data in a tree format based on a SQL query.

## Install

- Import Plug-In file into your application.

## How to use

- Create a region based on the plug-in.
- Add a SQL statement like the one below.
```
select  empno as value,
        ename as title,
        ename as tooltip,
        'fa fa-user' as icon,
        null as link,
        level as lvl,
        mgr as parent_id
from emp
start with mgr is null
connect by prior empno = mgr
order siblings by ename 
```
- Set the static ID of the region.
- Create 3 page items.
- Reference the page items in the required attributes of the plug-in.

## Demo
[https://apex.mt-ag.com/apex/f?p=140](https://apex.mt-ag.com/apex/f?p=140)

