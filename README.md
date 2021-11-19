
CS419 Project 3: Simulation of a Call Center
You can team up with another student or work alone. Each team must have no more than two students.
When it is due:
Friday November 19, at 11:59pm.
What to submit:
1. Please submit the completed CallCenter.java file.
2. Please submit a screenshot of the output from running the program.
3. For a two-person team, you will just need to submit once. Please be sure to submit a
note stating that it was a team submission and including the names of both team members.
Objectives:
1. Practice the use of the Java Executor framework for multi-threading.
2. Reinforce the concepts of critical section and synchronization.
3. Practice the use of the synchronization primitives provided by Java thread library.
Instructions:
0. Special instruction: for this project, you are NOT allowed to use any synchronized data structure provided by Java. You must implement any synchronization yourself.
1. This project requires you to implement a Java program that simulates a call center. The Java program has the following four classes:
a. the Agent class that simulates a customer service agent who answers customer calls.
i. Each agent has a unique ID.
b. the Greeter class that simulates the automated greeting service.
c. the Customer class that simulates a customer call.
i. Each customer has a unique ID.
d. the CallCenter class that drives the simulation.
2. The simulation uses multiple agents, multiple customers, and a single greeter, each running as a separate thread.
3. Upon arrival a customer call places itself in a wait queue.
4. The Greeter removes a customer from the wait queue, greet the customer, and then place the customer into the dispatch queue; it repeats this process.
a. The greeter must call the provided greet method to greet each customer.
b. The greeter should exit after it has served NUMBER_OF_CUSTOMERS customers.
c. Please note that the wait queue and dispatch queue are two separate queues.
5. An agent removes a customer from the dispatch queue and serve the customer; it repeats this process.
a. An agent must call the provided serve method to serve each customer.
b. An agent should exit after it has served CUSTOMERS_PER_AGENT customers.
Sample Output:
1. The output is produced by the serve method of the Agent class and the greet method of the Greeter class. We provided those two methods, and you should not modify them.
2. It is OK if the messages are printed out in different order (There is some randomness in this simulation). Please make sure that:
a. Each agent serves the exact number of customers as specified by CUSTOMERS_PER_AGENT.
b. Each customer is served by a single agent.
c. The program exits and does not hang. (Program hanging is usually a symptom of
synchronization issues.)
 
Grading:
This project carries 100 points. You will receive 80 points for correctly implementing all four classes (CallCenter, Agent, Greeter, and Customer), and another 20 points for submitting the screenshot of the output.
