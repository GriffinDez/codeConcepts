## Defn
- Mongoose is a helperlib, which helps to write MongoDb validation, casting and business boilerplate
- Generally used for for object modeling


```javascript
// 1. import the lib
const mongoose = require("mongoose");
// 2. connect with service/Function
mongoose.connect("MongoDB URL");

// 3. creation of schema

// 4. connecting with the next Step/ MongoDb for structure creation
// Creating model so as it can be shipped directly to mongoDB
const car = mongoose.model("Car", { name: String });

// insertion of values/ structure using "new" Keyword
const cars = new Car({ name: "jaguar" });

// save
cars.save().then(() => console.log("Super cool car"));
```

<!-- timestamp -->
- passed as a second argument. i.e after the model creation add {timestamps:true} as shown below.
- `{Model..},{timestamps:true}` // this results in addition of 2 properting in your schema.
- results in addition of 2 properties in the schema
    - createdAt
    - updatedAt

<!-- Relation -->
- how to add/refrence otherSchemas in a Schema
    - `type:Mongoose.Schema.Types.ObjectId`, always takes a ` ref:"User" `.
    - directly refrence to a type in anArray, `type:[UserSchema]`

<!-- Enum -->
- provides predefined options for a field.
- `enum:['M','F']`