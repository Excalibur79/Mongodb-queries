# Mongo db queries

### 1. Write a MongoDB query to display all the documents in the collection restaurants. 
    db.restaurants.find({})

### 2. Write a MongoDB query to display the fields restaurant_id, name, borough and cuisine for all the documents in the collection restaurant.
    db.restaurants.find({_id:false,restaurant_id:true,name:true,cuisine:true,borough:true})

### 5. Write a MongoDB query to display all the restaurant which is in the borough Bronx.
    db.restaurant.find({borough:"Bronx"})

### 7.Write a MongoDB query to display the next 5 restaurants after skipping first 5 which are in the borough Bronx. 
    db.restaurant.find({borough:"Bronx"}).skip(5).limit(5)

### 8. Write a MongoDB query to find the restaurants who achieved a score more than 90.
    db.restaurants.find({grades:{ $elemMatch:{ score:{$gt:90} } }})

### 9. Write a MongoDB query to find the restaurants that achieved a score, more than 80 but less than 100.
    db.restaurants.find({grades:{$elemMatch:{ score:{ $gt:80,$lt:100 } }}})