# Firestore

### Setup

Create a firebase project by going   [firebase.google.com](firebase.google.com) then create a project and click on add android app. Than follow along the tutorial that will be provided. For adding firestore implementation  add `implementation("com.google.firebase:firebase-firestore")` 

### Insert data

To get started open the `MainActivity.kt` and add the following piece of code `val db = Firebase.firestore` this is like an initializer for the firestore. We can use the following code snippet to insert into firestore

```kotlin
val db = Firebase.firestore
        // Create a new user with a first and last name
        val user = hashMapOf(
            "name" to "Rahim",
            "email" to "info@rahim.com",
            "prof" to "Engineer",
        )
        // Add a new document with a generated ID
        db.collection("users")
            .add(user)
            .addOnSuccessListener { documentReference ->
                Log.d("FBASE", "DocumentSnapshot added with ID: ${documentReference.id}")
            }
            .addOnFailureListener { e ->
                Log.w("FBASE", "Error adding document", e)
            }
```

Run the code and you'll see an insertion in the database
