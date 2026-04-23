# Node with Express API

## Node.Js

- Node.js is a JavaScript runtime.
- Runtime: A program that runs another program.
- Run JS in local machine.
- Built on C++
- Powered by Google Chrome v8 engine
- Used to build: API, real time apps, micro-services

## Architecture

- Single threaded
- Non-blocking I/O operation
- Event loop

## Express.js

- It is a Node.js API/backend framework.
- Used to build API (Application program interface)
- It simplies the HTTP module of node.js
- Minimalist, fast and unopinionated framework

## API

- API format: JSON (JavaScript Object Notation)
- REST API (Representational state transfer)

### JSON

- JS Object => JSON.stringify() => JSON
- JSON => JSON.parse() => JS Object

## HTTP Methods

1. GET - Read/Fetch
2. POST - Create
3. PUT - Update
4. DELETE - Delete
5. PATCH - Partial update

## Layered Architecture

1. API Layer
   a. Routes: Handle routes/endpoints
   b. Controllers: Handle request/response
   c. Middlewares: Handle request/response, Logging, Auth

2. Business logic layer
   a. Services

3. Data logic layer
   a. Models

4. Database layer

=========================

- mongodb
- Postman

---mongodb commands
show dbs -> show database
use mern-Mongo-> use or create database
show collections-> show collection or datatables
db.users.insertone({name:"Ram",Age:"12"}) oneormany to insert data
db.users.insertMany([{name:"Bipin",Age:"20"},{Phone:"900",address:"123qwe"}])
db.users.find()->find all data
db.users.find({name:"Ram"}) -> finbd specific data'
db.users.updateOne({name:'RRam'},{$set:{Age:"24"}})-> update database
db.deleteOne({name:"RRam"})-> delete data

equaloity operator:
ds.users.find({name:{$eq:"Hari}})

complex operator::
not equality operator
ds.users.find({name:{$ne:"Hari}})
$gt/gte(greater / greater or equalto): and $lt/lte:
ds.users.find({Age:{$gt:"20"}})
ds.users.find({Age:{$gte:"20"}})
ds.users.find({Age:{$lt:"20"}})
ds.users.find({Age:{$lte:"20"}})

---

%and-op:
db.users.find({$and:[{name;"Hari"},{Age:"40"}]})
db.users.find({$or:[{name;"Hari"},{Age:"40"}]})

---

limit:db.users.find().limit(2)
skip:db.users.find().skip(2)
sort:db.users.find().sort({name:1}) 1:asc -1:desc
