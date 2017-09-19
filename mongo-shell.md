Mongo shell
===========

Summary
-------

1. [Basis](#basis)
2. [Collection methods](#collection-methods)
3. [Operators](#operators)


Basis
-----

### Select database

	use DB

### Show selected database

	db

### Show all server databases

	show dbs

### Show all selected database collections

	show collections

Collection methods
------------------

### CRUD

####	Create

| Action              | Command                      |
| ------------------- | ---------------------------- |
| Insert one DOC      | `db.COLL.insert(DOC)`        |
| Insert multiple DOC | `db.COLL.insert([DOC, DOC])` |

####	Read

| Action                       | Command                    |
| ---------------------------- | -------------------------- |
| Read first COLL documents    | `db.COLL.findOne()`        |
| Read first 20 COLL documents | `db.COLL.find()`           |
| Read next 20 COLL documents  | `it`                       |
| Human readable format        | `db.COLL.find().pretty()`  |	
| Limit results number to N    | `db.COLL.find().limit(N)`  |
| Match by CRIT                | `db.COLL.find(CRIT)`       |
| Reshape data from PROJ       | `db.COLL.find(CRIT, PROJ)` |
	
#### Update

##### Update documents matching CRIT with PROP
	
	db.col.update(CRIT, PROP)

> Delete all fields in document matching CRIT (except id) and add PROP

####	Delete

| Action                             | Command                                   |
| ---------------------------------- | ----------------------------------------- |
| Remove all documents from COLL     | `db.COLL.remove({})`                      |
| Remove all documents matching CRIT | `db.COLL.remove(CRIT)`                    |
| Remove one document matching CRIT  | `db.COLL.remove(CRIT, {'justOne': true})` |

### Other

#### Count

| Action                                | Command               |
| ------------------------------------- | --------------------- |
| Count documents in COLL               | `db.COLL.count()`     |
| Count documents matching CRIT in COLL | `db.COLL.count(CRIT)` |

Operators
---------

### Comparisons

| Comparison                | Pattern |
| ------------------------- | ------- |
| Greater than              | `$gt`   |
| Greater than or equal     | `$gte`  |
| Less than                 | `$lt`   |
| Less than or equal        | `$lte`  |
| Not equal                 | `$ne`   |
| Equal values in array     | `$in`   |
| Not equal values in array | `$nin`  |

### Logicals

| Logical | Pattern |
| ------- | ------- |
| Or      | `$or`   |
| And     | `$and`  |
| Not     | `$not`  |
| Nor     | `$nor`  |

### Documents fields

| Field            | Pattern   |
| ---------------- | --------- |
| Exist            | `$exists` |
| Type             | `$type`   |

### Modifyers

| Value            | Pattern |
| ---------------- | ------- |
| Set              | `$set`  |
| Increment        | `$inc`  |

### Evaluations

| Value                           | Pattern  |
| ------------------------------- | -------- |
| Modulo                          | `$mod`   |
| Regular expression              | `$regex` |
| Text indexed field value search | `$text`  |
| Execute JavaScript              | `$where` |

### Geospatials

| Location value                   | Pattern          |
| -------------------------------- | ---------------- |
| Within GeoJSON coordinates       | `$geoWithin`     |
| Intersecting GeoJSON coordinates | `$geoIntersects` |
| Near a GeoJSON point             | `$near`          |
| Near a GeoJSON sphere            | `$nearSphere`    |

### Arrays

| Array value                | Pattern      |
| -------------------------- | ------------ |
| Contain all values         | `$all`       |
| Contain at least one value | `$elemMatch` |
| Size                       | `$size`      |

### Projection

| Projection                         | Pattern        |
| ---------------------------------- | -------------- |
| Array value first item             | `arrayField.$` |
| Matching document field            | `$elemMatch`   |
| Matching document text query score | `$meta`        |
| Limit number of item               | `$slice`       |
