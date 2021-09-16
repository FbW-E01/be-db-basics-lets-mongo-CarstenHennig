# Backend - Database - Basics - Let's MonGO

## Let's monGO

Add your answers directly into this README file.

1. Explain ObjectIDs in MongoDB; what are they?
   The MongoDB ObjectID is a 12-byte value consisting of
   a) 4-byte timestamp
   b) 5-byte random value  
    c) 3-byte incrementing counter

2. You have a collection called "users" with a document like this: `{ _id: 1, name: "Veera" }`. What query would you use to update the name to "Princess Veera Silkenfur"?
   'db.users.updateOne(
   { "name": "Veera },
   { $set { name: "Princess Veera Silkenfur" } }
   );'

3. How do you make a collection?
   db.createCollection("newCollection");

4. So the (old) mongo shell is kind of like a JavaScript REPL. What is a REPL? Which other REPL have we used?
   For loops

5. So the (old) mongo shell is kind of like a JavaScript REPL. You can use things like variables, try...catch statements and loops. Experiment with it and find at least three other JavaScript things that we have used that work in the (old) shell. If you can, try to find even more!

6. (Research) So the old shell is pretty cool. How is the new shell better?

7. (Research) How can you insert multiple documents at the same time?
   db.collection.insertMany(
   [
   { item: "test1, tags: ["test", "one"] }, { item: "test2, tags: ["test", "two"] }, { item: "test3, tags: ["test", "three"] }
   ]
   );

8. (Research) You have a collection called `cats` with a documents like this: `{ name: "Veera" }, { name: "Rauli" }, { name: "BenBen" }` - How can you insert the field `cute: true` into all of them with one command?
   db.cats.update({},
   {$set:{"cute":"true"}},
   {upsert:false,
   multi:true}
   );

9. (Task) Start a timer for 30 minutes. Spend all that time getting to know and reading https://docs.mongodb.com/manual/introduction/ - how far did you get? What was the most cool or interesting thing you learned?

10. Find one SQL Cheatsheet and one MongoDB Cheatsheet and add links to them here.
    SQL cheat sheet: https://www.sqltutorial.org/sql-cheat-sheet/
    MongoDB cheat sheet: https://www.mongodb.com/developer/quickstart/cheat-sheet/
    https://blog.codecentric.de/files/2012/12/MongoDB-CheatSheet-v1_0.pdf

🌿
