# Subscriber-gradle-Springboot
We're going to create a new Spring Boot app, adding on the addition of Thyme Templates.
We'll create a project that allows users to Subscribe to an online site.
We'll build out a form that will allow users to sign-up and display their entry on a separate page.
We'll create more views for performing CRUD actions with our Subscribers database.
SubscriberList
Fill out the following fields on the project page:


Name: SubscriberList
Group: com.tts
Artifact: SubscriberList
Description: Subscriber Sign up using JPA, H2, and Thymeleaf
Package name: com.tts.subscriberlist

Subscriber
The Subscriber class will have 5 attributes:

Id (Primary Key)
First Name
Last Name
Username
Sign-up Date
 
 We will set-up our class so that the ID and Sign-up date are automatically generated by Spring Boot.
Create a Subscriber Directory
The Subscriber directory will hold all the files associated with our subscriber, beginning with the class file Subscriber.java. We will add more files as we build out the project.

Create a Subscriber Class 
        public Subscriber(String firstName, String lastName, String userName, Date signedUp){
		this.firstName = firstName;
		this.lastName = lastName;
		this.userName = userName;
		this.signedUp = signedUp;
	}	

        
Create a constructor that requires that a Subscriber must be created with a first name, a last name, username, and the date the subscriber signs up (populated by the system).

Create a Subscriber Class 
The fields "Id" and "signedUp"  should be set to be automatically generated by the system. The annotations @Entity, @Id, @GeneratedValue, @Column, and @CreationTimestamp help us with that.

@Entity - We use this annotation to designate a plain old Java object (POJO) class as an entity so that we can use it with JPA services.

@Id - JPA will recognize it as the object’s ID and primary key

@GeneratedValue - Allows the underlying database to set the value for the field.

@Column -   attribute is stored in a database table column whose name matches that of the persistent field or property

@CreationTimestamp - sets the value of the date field to the current time and date exactly once during creation.

