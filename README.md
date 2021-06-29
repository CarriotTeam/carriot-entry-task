# Carriot-learning resources
Here are some learning resources to get familiar with [carriot](https://carriot.ir/)'s back-end technological stack. 

Here are the general topics:

 - Learn how to write code in [Go](https://golang.org/) in an [effective](https://golang.org/doc/effective_go.html) manner
 - Learn about RDBMS & NoSQL databases 
 - Learn about Git & Version control
 - Learn about micro-services 
 - Learn about virtualization and docker
 - Learn about infrastructure as a service & Linux systems & network concepts
 - Learn about API end point's, RESTful services and Protocol Buffers
 - Learn about software architecture ( specially DDD and clean architecture) 
 - Learn about clean code, TDD and best practices in software development 

From the resources, books,articles, videos etc which are introduced, the ones in **bold**  text are mandatory and the other ones are *highly recommended*. 

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

You can find a complete set of books [here](https://github.com/dariubs/GoBooks), but here are some useful resources:

 - [ ] **complete the [tour of go](https://tour.golang.org/)**
 - [ ] **watch this video: [Learn Go Programming](https://youtu.be/YS4e4q9oBaU)**
 - [ ] [Rob Pike - Simplicity is Complicated](https://www.youtube.com/watch?v=rFejpH_tAHM&list=PL3NQHgGj2vtsJkK6ZyTzogNUTqe4nFSWd)
 - [ ] read this book: [Go in Action](https://www.manning.com/books/go-in-action)


##  Protocol buffers and GRPC 
**Protocol buffers** are a mechanism for serializing structured data (although it can be used with other data formats such as JSON). We use Protocol buffers in *carriot* because it uses less bandwidth and is much more faster than JSON based communication. **GRPC**   uses HTTP/2 for transport, Protocol Buffers as the interface description language. With *GRPC* we can remotely call methods from  back-end or front-end  services. We use *GRPC* because it gives us much more flexibility, speed, etc.  

Here are some resources to learn more about Protocol buffers and GRPC:

 - [ ] **read [overview of protocol buffers](https://developers.google.com/protocol-buffers/docs/overview)**
 - [ ] **read [introduction to grpc](https://www.grpc.io/docs/what-is-grpc/introduction/)**
 - [ ]  **read [grpc core concepts](https://www.grpc.io/docs/what-is-grpc/introduction/)**
 - [ ] **watch this video: [Introduction to grpc](https://www.youtube.com/watch?v=RoXT_Rkg8LA)**
 - [ ]   **watch this video: [grpc and Go](https://www.youtube.com/watch?v=J-NTfvYL_OE)**


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
 - [ ] watch: [Introducing ClickHouse -- The Fastest Data Warehouse You've Never Heard Of ](https://www.youtube.com/watch?v=fGG9dApIhDU)
 - [ ] read: [Redis](https://redis.io/)

Also the [Intro to Database systems](https://www.youtube.com/playlist?list=PLSE8ODhjZXjbohkNBWQs_otTrBTrjyohi) from the `CMU Database Graoup` is a great course for learning about databases in detail. 

You can directly connect to the database in your code and use `plain text query`, but we prefer to use an [ORM](https://en.wikipedia.org/wiki/Object%E2%80%93relational_mapping) like [gorm](https://gorm.io/index.html).. 

 
## Docker
Docker is a container and virtualization technology. We use many of docker's technologies like `docker compose`, `docker container`, etc. You can learn docker by following these tasks:

 - [ ] **watch: [Docker tutorial](https://www.youtube.com/watch?v=fqMOX6JJhGo)**
 - [ ] read first part of : [Docker in Action](https://www.manning.com/books/docker-in-action-second-edition)

## Clean code & Coding style

Clean code and Coding style might not seem very important at first glance but over time can play a very important role in the development process.

 - [ ] **read the first 10 chapters of this book: [Clean code](https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882)**
 
## Software & System architecture 
In carriot we have divided our services to multiple **Micro-services**. You can search more about micro-services your self, it's quite an easy concept to understand but much harder to implement. We recommend reading [Micro-services in action ](https://www.manning.com/books/microservices-in-action) if you want to learn more. 

We try to follow an architecture called `Ports & Adapters` which is closely related to the `Hexagonal architecture`, ` Onion architecture` and `Clean architecture`. This architecures are designed based on **Domain Driven Design or DDD** so while designing and developing our services we try to keep **DDD**'s guidelines in mind too.

This concepts might be new to you and usually take time and practice to understand and master. Follow this tutorials and resources to get a better understanding of these concepts:

 - [ ] **read this article and related links : [S.O.L.I.D](https://en.wikipedia.org/wiki/SOLID)**
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


### Testing 

We use **TDD** or **Test Driven Development** methodology to test our codes, *you can only submit merge request when all the test are passed* . Also writing **Unit test**, **Acceptance tests**, etc. are really important for new features,


