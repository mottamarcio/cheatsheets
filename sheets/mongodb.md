## **MONGODB**

### **Basic Commands:**

| Command             | Description                              | Example             |
| ------------------- | ---------------------------------------- | ------------------- |
| `mongo`             | Start the MongoDB shell                  | `mongo`             |
| `show dbs`          | List available databases                 | `show dbs`          |
| `use <database>`    | Switch to a database                     | `use mydb`          |
| `db`                | Show the current database                | `db`                |
| `show collections`  | List collections in the current database | `show collections`  |
| `db.dropDatabase()` | Drop the current database                | `db.dropDatabase()` |

---

### **CRUD Operations:**

#### **Insert:**

```javascript
db.users.insertOne({ name: "John Doe", age: 30 }); // Insert a single document
db.users.insertMany([{ name: "Jane Doe", age: 25 }, { name: "Peter Pan", age: 18 }]); // Insert multiple documents
```

#### **Read (Query):**

```javascript
db.users.find(); // Find all documents in the collection
db.users.find().pretty(); // Find all documents in the collection and format the output
db.users.findOne({ name: "John Doe" }); // Find a single document
db.users.find({ age: { $gt: 20 } }); // Find documents where age is greater than 20
db.users.find({ name: { $regex: /Doe$/ } }); // Find documents where name ends with "Doe"
```

#### **Update:**

```javascript
db.users.updateOne({ name: "John Doe" }, { $set: { age: 31 } }); // Update a single document
db.users.updateMany({ age: { $lt: 30 } }, { $inc: { age: 1 } }); // Increment age by 1 for all users under 30
```

#### **Delete:**

```javascript
db.users.deleteOne({ name: "John Doe" }); // Delete a single document
db.users.deleteMany({ age: { $gte: 30 } }); // Delete all users aged 30 or older
```

---

### **Query Operators:**

| Operator  | Description                                     |
| --------- | ----------------------------------------------- |
| `$eq`     | Equal to                                        |
| `$ne`     | Not equal to                                    |
| `$gt`     | Greater than                                    |
| `$lt`     | Less than                                       |
| `$gte`    | Greater than or equal to                        |
| `$lte`    | Less than or equal to                           |
| `$in`     | Matches any of the values in an array           |
| `$nin`    | Matches none of the values in an array          |
| `$regex`  | Matches a regular expression                    |
| `$exists` | Matches documents that have the specified field |

---

### **Projection:**

```javascript
db.users.find({}, { name: 1, age: 1, _id: 0 }); // Include only name and age, exclude _id
```

---

### **Sorting:**

```javascript
db.users.find().sort({ age: 1 }); // Sort by age in ascending order
db.users.find().sort({ age: -1 }); // Sort by age in descending order
```

---

### **Limiting and Skipping:**

```javascript
db.users.find().limit(5); // Return only the first 5 documents
db.users.find().skip(5).limit(5); // Skip the first 5 documents and return the next 5
```

---

### **Indexing:**

```javascript
db.users.createIndex({ name: 1 }); // Create an index on the name field
```

---

### **Aggregation Framework:**

```javascript
db.users.aggregate([
  { $match: { age: { $gt: 20 } } },
  { $group: { _id: null, averageAge: { $avg: "$age" } } }
]); // Calculate the average age of users over 20
```

---

### **Advanced Concepts:**

#### **Geospatial Queries:**

```javascript
db.places.createIndex({ location: "2dsphere" }); // Create a 2dsphere index for location data
db.places.find({ location: { $near: { $geometry: { type: "Point", coordinates: [ -73.9667, 40.78 ] } } } }); // Find places near a specific point
```

#### **Text Search:**

```javascript
db.articles.createIndex({ title: "text", content: "text" }); // Create a text index on title and content
db.articles.find({ $text: { $search: "mongodb" } }); // Find articles containing the word "mongodb"
```

#### **Change Streams:**

```javascript
const changeStream = db.users.watch();
changeStream.on("change", change => console.log(change)); // Watch for changes in the users collection
```

#### **Transactions:**

```javascript
const session = client.startSession();
session.startTransaction();
try {
  // Perform database operations within the transaction
  await db.collection("inventory").updateOne({ _id: 1 }, { $inc: { quantity: -1 } }, { session });
  await db.collection("orders").insertOne({ _id: 2, item: "abc", quantity: 1 }, { session });
  await session.commitTransaction();
} catch (error) {
  await session.abortTransaction();
} finally {
  session.endSession();
}
```

---

### **Tips and Tricks:**

* Use the `explain()` method to analyze query performance.
* Use the `mongodump` and `mongorestore` tools for backup and restore.
* Use a GUI tool like MongoDB Compass for easier data visualization and management.

---

### **Resources:**

* **Official MongoDB Documentation:** [https://docs.mongodb.com/](https://docs.mongodb.com/)
* **MongoDB University:** [https://university.mongodb.com/](https://university.mongodb.com/)
* **MongoDB Atlas:** [https://www.mongodb.com/cloud/atlas](https://www.mongodb.com/cloud/atlas)
