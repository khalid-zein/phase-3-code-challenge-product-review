# phase-3-code-challenge-product-review

## Introduction

For this assignment, we'll be working with an e-commerce domain. We'll be focusing on the product reviews.

 

We have three models: User, Review, and Product.

 

For our purposes, a Product has many Users, a User has many Products’ s, and a Review belongs to a User and to a Product.

 

Product - User is a many-to-many relationship.

 

Note: You should design your domain/Entity Relationship Diagram(ERD) using any Unified Modelling Language such as starUML Links to an external site.before you start coding. You are required to include it in your README.

## Topics

This assignment focused on the following topics:
<ul>
 <li>Active Record Migrations</li>
 <li>Active Record Associations</li>
 <li>Class and Instance Methods</li>
 <li>Active Record QueryingProject Setup</li>
</ul>

## Project Setup

Once you have the plan in place for the application you want to build take the following steps:
<ul>
 <li>Create a new project folder</li>
 <li>Create a new GitHub repository (NB: ENSURE IT IS PRIVATE).</li>
 <li>Add your TM as a contributor to the project. (This is only for grading purposes. We promise we won't steal your code)</li>
 <li>Please make sure you regularly commit to the repository.</li>
</ul>

## Instructions

Build out all of the methods listed in the deliverables. The methods are listed

in a suggested order, but you can feel free to tackle the ones you think are

easiest. Be careful: some of the later methods rely on earlier ones.

 

Remember! This code challenge does not have tests. You cannot run rspec

and you cannot run and learn. You'll need to create your own sample instances so

that you can try out your code on your own. Make sure your associations and

methods work in the console before submitting.

 

We've provided you with a tool that you can use to test your code. To use it,

run rake console from the command line. This will start a pry session with

your classes are defined. You can test out the methods that you write here. You are

also encouraged to use the seeds.rb file to create sample data to test your

models and associations.

 

Writing error-free code is more important than completing all of the

deliverables listed - prioritize writing methods that work overwriting more

methods that don't work. You should test your code in the console as you write.

 

Similarly, messy code that works is better than clean code that doesn't. First,

prioritize getting things working. Then, if there is time in the end, refactor

your code to adhere to best practices.

 

Before you submit! Save and run your code to verify that it works as you

expect. If you have any methods that are not working yet, feel free to leave

comments describing your progress.

## Deliverables

Create the following classes and their respective methods.

Set up your application so it runs from a configured run file. 

Create instances of the classes on the run file and try out the methods you just created.

Use the notation # for instance methods, and .(dot) for class methods.

Feel free to build out any helper methods if needed.

 

Remember: Active Record gives your classes access to a lot of methods already!

Keep in mind what methods Active Record gives you access to in each of your

classes when you're approaching the deliverables below.

### Migrations

Before working on the rest of the deliverables, you will need to create a

migration for the reviews table.

<ul>
 <li>A Review belongs to a Product, and a Review also belongs to a User. In your migration, create any columns your reviews table will need to establish   these relationships.</li>
 <li>The reviews table should also have:
  <ul>
   <li>A star_rating column that stores an integer.</li>
   <li>A comment column that stores a string.</li>
  </ul>
 </li>
</ul>

After creating and running your migration, create your Review class, and use

the seeds.rb file to create Review instances so you can test your code.

 

Once you've set up your reviews table, work on building out the following

deliverables.

### Object Association Methods

Use Active Record association macros and Active Record query methods where

appropriate (i.e. has_many, has_many through, and belongs_to).


<ul>
 <li>Review
  <ul>
   <li>Returns the User instance for this Review</li>
   <li>Returns the Product instance for this Review</li>
   <li>Review#user</li>
   <li<Review#product</li>
  </ul>
 </li>
</ul>

<ul>
 <li>Product
  <ul>
   <li>Product#reviews</li>
   <ul>
    <li>Returns a collection of all the Reviews for the Product</li>
   </ul>
   <li>Product#users</li>
   <ul>
    <li>Returns a collection of all the Users who reviewed the Product</li>
   </ul>
  </ul>
 </li>
</ul>

<ul>
 <li>User
  <ul>
   <li>User#reviews</li>
   <ul>
    <li>Returns a collection of all the Reviews that the User has given</li>
   </ul>
   <li>User#products</li>
   <ul>
    <li>Returns a collection of all the Products that the User has reviewed</li>
   </ul>
  </ul>
 </li>
</ul>



Use the rake console and check that these methods work before proceeding. For

example, you should be able to call User.first.products and see a list of the

products for the first user in the database based on your seed data, and Review.first.user should return the user for the first review in the database.


###  Aggregate and Association Methods

<ul>
 <li>Review
  <ul>
   <li>Review#print_review
    <ul>
     <li>This should puts in the terminal a string formatted as follows: Review for {insert product name} by {insert user name}: {insert review       star_rating}. {insert review comment}</li>
    </ul>
   </li>
  </ul>
 </li>
</ul>

<ul>
 <li> Product
  <ul>
   <li>Product#leave_review(user, star_rating, comment)
    <ul>
     <li>Takes a User (an instance of the User class), a star_rating (integer), and a comment (string) as arguments, and creates a new Review in the  database associated with this Product and the User</li>
    </ul>
   </li>
   <li>Product#print_all_reviews</li>
  </ul>
 </li>
 <li>This should puts in the terminal a string representing each review for this product</li>
 <li>Each review should be formatted as follows: Review for {insert product name} by {insert user name}: {insert review star_rating}. {insert review   comment}</li>
 
 <li>Product#average_rating
  <ul>
   <li>Returns a float representing the average star rating for all reviews for this product</li>
  </ul>
 </li>
</ul>


<ul>
 <li>User
  <ul>
   <li>User#favorite_product
    <ul>
     <li>Returns the product instance that has the highest star rating from this user</li>
    </ul>
   </li>
   <li>User#remove_reviews(product)
    <ul>
     <li>Takes a Product (an instance of the Product class) and removes all of this user's reviews for that product</li>
     <li>You will have to delete any rows from the reviews table associated with this user and the product</li>
    </ul>
   </li>
  </ul>
 </li>
</ul>
