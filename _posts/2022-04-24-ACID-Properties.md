---
layout: post
title:  "ACID Properties"
categories: [ DBMS ]
image: assets/images/demo1.jpg
author: Aaditya
---
ACID Properties is the property of database transactions intended to guarentee validity even in the event of power failure, errors, etc. 
This has 4 properties
	1. Atomicity
	2. Consistency
	3. Isolation
	4. Durability

### ACID Properties in Detail
-   **Atomicity:** The whole transaction is processed or nothing is processed. A commonly cited example of an atomic transaction is money transactions between two bank accounts. The transaction of transferring money from one account to the other is made up of two operations. First, you have to withdraw money in one account, and second you have to save the withdrawn money to the second account. An atomic transaction, i.e., when either all operations occur or nothing occurs, keeps the database in a consistent state. This ensures that if either of those two operations (withdrawing money from the 1st account or saving the money to the 2nd account) fail, the money is neither lost nor created. Source [Wikipedia](https://en.wikipedia.org/wiki/Atomicity_(database_systems)). for a detailed description of this example.  
      
      
    
-   **Consistency:** Only transactions that abide by constraints and rules are written into the database, otherwise the database keeps the previous state. The data should be correct across all rows and tables. Check out additional information about consistency on [Wikipedia](https://en.wikipedia.org/wiki/Consistency_(database_systems)).  
      
    
-   **Isolation:** Transactions are processed independently and securely, order does not matter. A low level of isolation enables many users to access the data simultaneously, however this also increases the possibilities of concurrency effects (e.g., dirty reads or lost updates). On the other hand, a high level of isolation reduces these chances of concurrency effects, but also uses more system resources and transactions blocking each other. Source: [Wikipedia](https://en.wikipedia.org/wiki/Isolation_(database_systems)).
    
-   **Durability:** Completed transactions are saved to database even in cases of system failure. A commonly cited example includes tracking flight seat bookings. So once the flight booking records a confirmed seat booking, the seat remains booked even if a system failure occurs.  
    Source: [Wikipedia](https://en.wikipedia.org/wiki/ACID).