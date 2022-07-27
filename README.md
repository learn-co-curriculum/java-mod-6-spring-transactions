# Spring Transactions

## Learning Goals

- Explain how to use transactions in Spring Data

## Introduction

A SQL transaction is a series of operations that are each a logical unit of data
creation and manipulation. When a transaction fails all of the operations in the
transaction are rolled back, i.e., a failed transaction prevents any data
creation, modification, and deletion.

Spring provides a declarative way to manage transactions which means Spring can
automatically create transactions for operations if we mark methods with an
`@Transactional` annotation. We will be looking at the following annotations in
this lesson:

- `[@EnableTransactionManagement](https://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/transaction/annotation/EnableTransactionManagement.html)`
- `[@Transactional](https://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/transaction/annotation/Transactional.html)`

## `@EnableTransactionManagment`

This enables the annotation based transaction management in Spring. An
application requires this in order for the `@Transactional` annotation to work.
Spring Data repositories are contained within transactions by default so there
is no need to add this to the project if you are using Spring Data.

## `@Transactional`

We can put the `@Transactional` annotation over method, class, or interface
definitions to make all operations inside the annotated unit execute within a
transaction. Only public methods can be made to work with this annotation. All
transactions are cancelled when there is an exception during any operation that
are within an annotated unit.

## Conclusion

We learned about the annotations available in Spring for transactions. If you
use Spring Data in your project then it will automatically handle transactions.

## References

- `[@EnableTransactionManagement`
  docs](https://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/transaction/annotation/EnableTransactionManagement.html)
- `[@Transactional`
  docs](https://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/transaction/annotation/Transactional.html)
