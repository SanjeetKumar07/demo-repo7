# Messaging Queue

A messaging queue helps different parts of a system talk to each other without waiting for an immediate answer. It stores messages until the receiver is ready to handle them. This makes the system more flexible and reliable because services don’t have to be connected all the time.

## Understanding Messaging Queue Through an Example

Imagine an online shopping website where a customer places an order. Many tasks need to happen, such as:

* Updating the inventory  
* Processing the payment  
* Sending a confirmation email  
* Notifying the delivery team  

If all these tasks ran one after another in the same system, the customer might have to wait a long time before getting the order confirmation.

## How Messaging Queue Helps

Instead of performing all tasks immediately, the system sends messages to a queue. Each message represents a task, like “update inventory” or “send email.” These messages stay in the queue until the right service is ready to handle them. For example:

* The email service reads messages from the queue and sends emails one by one.  
* This happens without slowing down the rest of the system.

## Benefits of Messaging Queues

* **Reliability:** If a service crashes (like the email service), messages remain safe in the queue until it comes back online, so no task gets lost.  
* **Scalability:** The system can handle many orders by distributing tasks to multiple services that read from the same queue, improving performance.  
* **Flexibility:** Services don’t need to be connected or work at the same time.




## Key Features of Messaging Queues

* **Message Durability:** Messages are saved safely until delivered, even if the system crashes.  
* **Multiple Consumers:** More than one consumer can read from the same queue, sharing the workload.  
* This makes the system able to handle more users or tasks easily.

## Summary of the paper 

* **How to Use Messaging Queues**  
Send messages to a queue and let services consume them asynchronously when ready.

* **Why Use Messaging Queues**  
To make systems reliable, scalable, and loosely coupled.

* **When to Use Messaging Queues**  
When different parts of a system need to work independently or handle varying loads without blocking each other.


## References

* [Messaging Queue Basics - GeeksforGeeks](https://www.geeksforgeeks.org/introduction-to-messaging-queues-in-spring-boot-microservices/)
* [A Simple Guide to Using IBM MQ with Java Messaging Service - Levio](https://levioconsulting.com/insights/a-simple-guide-to-using-ibm-mq-with-java-messaging-service/)



