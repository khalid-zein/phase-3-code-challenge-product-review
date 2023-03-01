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
