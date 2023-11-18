# Design Document

By `Sandeep Sanjay Kulkarni`

Video overview: <URL HERE>

## Scope

In this section you should answer the following questions:

* What is the purpose of your database?

    This database is created inspired by a Personal Finances Tracker Application. A user can connect to their bank account, keep a track of financial transactions happening through the bank account. And set limit notifications.

* Which people, places, things, etc. are you including in the scope of your database?

    The database is restricted to individuals, who have an active bank account.

* Which people, places, things, etc. are *outside* the scope of your database?

    Anything which is not related to finances are not a part of this database.

## Functional Requirements

In this section you should answer the following questions:

* What should a user be able to do with your database?

    Create entries for:
    - A Bank. e.g., Bank of America, State Bank of India.
    - A User.
    - User's Bank Accounts.
    - Deposit & Withdraw Money from Bank Accounts.
    - Set Notifications for Balance Threshold Alerts.

* What's beyond the scope of what a user should be able to do with your database?

    Anything which isn't mentioned above is beyond the scope of the user.

## Representation

### Entities

In this section you should answer the following questions:

* Which entities will you choose to represent in your database?

    ### User
    - User's First Name and Last Name
    - User's Government Provided Unique Id Number
    - User's Username Password
    - User's Bank Account Number

    ### Bank
    - Bank's Name

    ### Transactions
    - Bank Account Number from which transaction is carried out
    - Amount involved in transaction
    - Action (Deposit / Withdraw)

    ### Alerts
    - Bank Account Number
    - Threshold Percentage

* What attributes will those entities have?

    Mentioned above.

* Why did you choose the types you did?

    Mostly TEXT, INTEGER and DECIMALs. DATETIME (if MySQL) would be used for storing the timestamp of transaction.

* Why did you choose the constraints you did?

    FOREIGN KEY CONSTRAINTS would be used for relating the entities.

### Relationships

In this section you should include your entity relationship diagram and describe the relationships between the entities in your database.



## Optimizations

In this section you should answer the following questions:

* Which optimizations (e.g., indexes, views) did you create? Why?

    VIEWS have been created to show the transaction history of the users. Also, INDEX has been created on the same table as it will speed up the user to search his transactions.

## Limitations

In this section you should answer the following questions:

* What are the limitations of your design?

    Current design might need slight changes if there's any new feature additions happening in the later stage of the application development.

* What might your database not be able to represent very well?

    Anything that may be added new and hasn't been currently included.
