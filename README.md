# Carriot-learning resources
In The course tutorial you'll get familiar with [carriot](https://carriot.ir/)'s back-end technological stack. At the end we expect you to become a qualified software engineer, able to quickly and creatively solve the tasks that are assigned to you.  

The general goals of this program are as follows:

 - Learn how to write code in [Go](https://golang.org/) in an [effective](https://golang.org/doc/effective_go.html) manner
 - Learn about RDMS & NoSQL databases 
 - Learn about git & version control
 - Learn about micro-services 
 - Learn about virtualization and docker
 - Learn about infrastructure as a service & Linux systems & network concepts
 - Learn about API end point's, RESTful services and Protocol Buffers
 - Learn about software architecture ( specially DDD and clean architecture) 
 - Learn about clean code, TDD and best practices in software development 

This program consists of the following seven parts:

**Part 1:** We start with some prerequisites to set up your system.

**Part 2:** We learn how to program and code with GO.

**Part 3:** We learn how to to use GRPC and Protocol buffers by implementing a simple client and server application.

**Part 4:** We learn about Databases(specially the ones used int *carriot*) and connect one to the application we created int the previous part.

**Part 5:** We use [Docker](https://www.docker.com/)  to wrap our codes in an some images and deploy them on a virtual machine. 

**Part 6:** We talk about micro-services and software architecture and introduce some useful resources for you to continue learning. 

**Part 7:** Finally we talk about clean code, TDD and coding style and guide lines which you should uses whiles your coding on *carriot's* back-end services source code.

All through the course many resources, books,articles, videos etc are introduced. The ones in **bold**  text are mandatory and the other ones are *highly recommended*. Also there are some assignment's for you in each part which you should complete before moving  to the next part. 

Until you finish this program you **one of our team members is assigned to you as a mentor**. You can ask question or seek help from your mentor if you faced any trouble.

## Prerequisites 
It's recommended to develop all your code in a [UNIX](https://en.wikipedia.org/wiki/Unix)  based operating system e.g. MAC OS X , Ubuntu, etc.

Install the following on your system:

 1. [Git](https://git-scm.com/downloads)
 2.  [Go](https://golang.org/dl/) (you can also use [snap ](https://snapcraft.io/install/go/ubuntu) to install it)
 3.  Your desired IDE or code editor([GoLand](https://www.jetbrains.com/go/promo/?gclid=CjwKCAiAirb_BRBNEiwALHlnD1Tf_ZqPpDoYkqtfZyANhUD-U0XHtDzGpKP_XUupjBfRqfauehwEehoC6wgQAvD_BwE) or [Visual studio code](https://code.visualstudio.com/) are recommended)
 4. [Protocol buffer](https://developers.google.com/protocol-buffers) 
 5. [GRPC](https://grpc.io/docs/languages/go/quickstart/)
 6. [PostgreSQL](https://www.postgresql.org/)

##  Golang
Go is a statically typed, compiled programming language designed at Google. 

You can find a complete set of books [here](https://github.com/dariubs/GoBooks), but for now your tasks are:

 - [ ] **complete the [tour of go](https://tour.golang.org/)**
 - [ ] **watch this video: [Learn Go Programming](https://youtu.be/YS4e4q9oBaU)**
 - [ ] [Rob Pike - Simplicity is Complicated](https://www.youtube.com/watch?v=rFejpH_tAHM&list=PL3NQHgGj2vtsJkK6ZyTzogNUTqe4nFSWd)
 - [ ] read this book: [Go in Action](https://www.manning.com/books/go-in-action)

There are many other resources online, try to find some that are good for you and learn more about *Golang*. While learning *Go* keep in mind that ***Go* is neither a completely procedural nor a completely object oriented language, go is a multi-paradigm language with its own style of programming**, so don't try to code like *Java, C++, Python etc. in Go*

###  Assignment 1
 Write a simple web-server in Go, your web server should handle **HTTP GET** requests from a browser. Here are the details:

 - Create a `server.go` file.
 - Create a `http server` in your file.
 - Create two routes: `/vehicles` and `/drivers`
 - When the client give a request to your server: `http://localhost:8080/vehicles` or `http://localhost:8080/drivers`, you should return a list of vehicles or drivers 

Vehicle is an object with `VehicleID`, `DriverID`, `VehicleName` as fields.
Driver is an object with `DriverID`, `DriverName` as fields.
Each vehicle is assigned to some driver. For now you can mock some instances of these two objects in memory. 


##  Protocol buffers and GRPC 
**Protocol buffers** are a mechanism for serializing structured data (although it can be used with other data formats such as JSON). We use Protocol buffers in *carriot* because it uses less bandwidth and is much more faster than JSON based communication. **GRPC**   uses HTTP/2 for transport, Protocol Buffers as the interface description language. With *GRPC* we can remotely call methods from  back-end or front-end  services. We use *GRPC* because it gives us much more flexibility, speed, etc.  

First of all please do the following tasks:

 - [ ] **read [overview of protocol buffers](https://developers.google.com/protocol-buffers/docs/overview)**
 - [ ] **read [introduction to grpc](https://www.grpc.io/docs/what-is-grpc/introduction/)**
 - [ ]  **read [grpc core concepts](https://www.grpc.io/docs/what-is-grpc/introduction/)**
 - [ ] **watch this video: [Introduction to grpc](https://www.youtube.com/watch?v=RoXT_Rkg8LA)**
 - [ ]   **watch this video: [grpc and Go](https://www.youtube.com/watch?v=J-NTfvYL_OE)**

There are many other resources online, feel free to uses any of them if still haven't understood the concept or want to learn more.

###  Assignment 2
In the last assignment you created a simple web server in go. Now you have to write a client and modify the server to use `protocol buffers + grpc` .

 - Create a `client.go` file.
 - Create a `.proto` file
 - It is expected that your client requests information about vehicles or drivers via `grpc` and `protocol buffer`
 - Your server should respond to the clients requests, so you have to modify the your server

You can use these two tutorials for help:

 - [ ] [Building an Basic API with gRPC and Protobuf](https://www.youtube.com/watch?v=Y92WWaZJl24)
 - [ ] [Protocol buffers and go](https://developers.google.com/protocol-buffers/docs/gotutorial)


## Databases 
In carriot we use a wide variety of Database Management Systems (DBMS), such as:

 - [PostgreSQL](https://www.postgresql.org/)
 - [Elastic search](https://www.elastic.co/)
 - [ClickHouse](https://clickhouse.tech/)
 - [Redis](https://redis.io/)

For now we focus on **PostgreSQL**, you can learn about other databases later if you encountered any task that needs them. 

If you're already familiar with **SQL** and **PostgreSQL** you can skip some of the task. here are these sections tasks:

 - [ ] **read: [SQL tutorial](https://www.w3schools.com/sql/)**
 - [ ]  **watch: [SQL tutorial](https://www.youtube.com/watch?v=HXV3zeQKqGY)**
 - [ ] **read: [about PostgreSQL](https://www.postgresql.org/about/)**
 - [ ] **watch: [Learn PostgreSQL](https://www.youtube.com/watch?v=qw--VYLpxG4)**

Also the [Intro to Database systems](https://www.youtube.com/playlist?list=PLSE8ODhjZXjbohkNBWQs_otTrBTrjyohi) from the `CMU Database Graoup` is a great course for learning about databases in detail. 

### Assignment 3
Use the server and client that you previously created and add the following functionality:

 - Setup and Deploy an instance of `PostgreSQL` on your local system.
 - Create a table for `drivers` and `vehicles` 
 - Create appropriate indexes, foreign keys, etc.
 - Connect you `server.go` application to the database instance
 - Your server should now uses the database to get the records and pass them to the client
You can directly connect to the database in your code and to a `plain text query` or you can use [gorm](https://gorm.io/index.html) as an `ORM`. 

 
## Docker
Docker is a container and virtualization technology. We use many of docker's technologies like `docker compose`, `docker container`, etc. You can learn docker by following these tasks:

 - [ ] **watch: [Docker tutorial](https://www.youtube.com/watch?v=fqMOX6JJhGo)**
 - [ ] **read first part of : [Docker in Action](https://www.manning.com/books/docker-in-action-second-edition)**

You can uses other resources too. 

  ### Assignment 4

 - Create two `Docker files`( for the client and server applications)
	 - These files should take care of building and exposing your application
	
 - Create a `Docker compose` file  to load an instance of `PostgreSQL` and run the `server` and `client` applications

note that when loading a database with `docker compose`, you have to also run a `migrate script` to create some tables in you database and fill them with data. ask your mentor for more details on this task If you faced any problem.    

 
## Software architecture & Micro-services
In carriot we have divided our services to multiple **Micro-services**. You can search more about micro-services your self, it's quite an easy concept to understand but much harder to implement. We recommend reading [Micro-services in action ](https://www.manning.com/books/microservices-in-action) if you want to learn more. 

We try to follow an architecture called `Ports & Adapters` which is closely related to the `Hexagonal architecture`, ` Onion architecture` and `Clean architecture`. Also while designing and developing our services we try to keep **Domain Driven Design or DDD**'s guidelines in mind. 

This concepts might be new to you and usually take time and practice to understand and master. Follow this tutorials and resources to get a better understanding of these concepts:

 - [ ] **watch: [What is DDD?](https://www.youtube.com/watch?v=pMuiVlnGqjk)**
 - [ ] **read: [DDD, Hexagonal, Onion, Clean, CQRS](https://herbertograca.com/2017/11/16/explicit-architecture-01-ddd-hexagonal-onion-clean-cqrs-how-i-put-it-all-together/)**
 - [ ] read: [Strategic Domain-Driven Design](https://vaadin.com/learn/tutorials/ddd/strategic_domain_driven_design)
 - [ ] read: [Tactical Domain-Driven Design](https://vaadin.com/learn/tutorials/ddd/tactical_domain_driven_design)
 - [ ]  read: [DDD & Hexagonal](https://vaadin.com/learn/tutorials/ddd/ddd_and_hexagonal)
 - [ ]  **watch: [Micro-service architecture and Go](https://www.youtube.com/watch?v=dVnMLtdJzn4)**
 
 We also highly recommend to read the following books:
 - [Clean architecture](https://www.amazon.co.uk/Clean-Architecture-Craftsmans-Software-Structure/dp/0134494164)
 - [Patterns, Principles, and Practices of Domain-Driven Design](https://www.wiley.com/en-gb/Patterns%2C+Principles%2C+and+Practices+of+Domain+Driven+Design-p-9781118714706)

Learning and implementing good software architecture need knowledge, skill, time, practice, talking to your teammates, trail and error etc. so be patient.   

## Clean code & Coding style

Clean code and Coding style might not seem very important at first glance but over time can play a very important role in the development process.

 - [ ] **read the first 10 chapters of this book: [Clean code](https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882)**
 - [ ] **read this article and related links : [S.O.L.I.D](https://en.wikipedia.org/wiki/SOLID)**

In coding and designing keep these simple rules in mind:

 1. Your code should run all the tests
 2. Your code should not contain duplication
 3. Your design should express the intent of the program
 4. You should generally try to minimize the number of entities and methods

### Testing 

We use **TDD** or **Test Driven Development** methodology to test our codes, *you can only submit merge request when all the test are passed* . Also writing **Unit test**, **Acceptance tests**, etc. are really important for new features,


