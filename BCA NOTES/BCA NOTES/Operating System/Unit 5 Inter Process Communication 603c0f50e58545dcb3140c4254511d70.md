# Unit 5 : Inter Process Communication

## The Producer-Consumer Problems

- The Producer-Consumer problem is a classic problem that is used for multi-process synchronization.
- Synchronization between more than one processes In the producer-consumer problem, there is one Producer that is producing something and there is one Consumer that is consuming the products produced by the Producer.
- The producer consumers share the same memory buffer that is of fixed size.

<aside>
💡 The job of the Producer is to generate the data, put it into the buffer, and again start generating data. While the job of the consumer is to consume the data from the buffer.

</aside>

---

### *What’s the problem?*

- The producer should only produce data when the buffer is not full. If the buffer is full, then the producer shouldn’t be allowed to put any data into the buffer.
- The Consumer should consume data only when the buffer is not empty. If the buffer is empty, then the consumer shouldn’t be allowed to take any data from the buffer.
- The producer and Consumer should not access the buffer at the same time.

### *Solution* ➖

- **Semaphore S**: This semaphore variable is used to achieve mutual exclusion between processes. By using this variable, either producer or consumer will be allowed to use or access the shared buffer at a particular time. This variable is initially set to 1.
- **Semaphore E**: This semaphore variable is used to define the empty space in the buffer. Initially, it is set to the whole space of the buffer i.e. “n” because the buffer is initially empty.
- **Semaphore F**: The semaphore variable is used to define the space that is filled by the producer. Initially, it is set to 0 because there is no space filled by the producer initially.

<aside>
💡 By using the above three semaphore variables and by using the wait() and signal() function,
we can solve our problem(the wait() function decreases the semaphore variable by 1 and the
signal() function increases the semaphore variable by 1)

</aside>

- Psuedo-code for the producer :
    
    ```jsx
    void producer() {
    while(T) {                          //while is used to produce data again and again 
    produce()                           //produce function is called to produce data by the producer
    wait(E)                             //wait(E) will reduce the semaphore "E" by 1 
    wait(S)                             //wait(S) will set the semphore S to 0
    append()                            //append() function is used to append the newly produced data in the buffer
    signal(S)                           //signal(s) is used to set the semaphore variable to 1
    signal(F)                           //signal(F) is used to increase the semaphore F to 1
    }
    }
    ```
    
- Code Explanation ➖
    - `while()` is used to produce data, again and again, if it wishes to produce, again and
    again.
    - `produce()` function is called to produce data by the producer.
    - `wait(E)` will reduce the value of the semaphore variable "E" by one i.e. when the
    producer produces something then there is a decrease in the value of the empty space
    in the buffer. If the buffer is full i.e. the vale of the semaphore variable "E" is "0",
    then the program will stop its execution and no production will be done.
    - `wait(S)` is used to set the semaphore variable "S" to "0" so that no other process can
    enter into the critical section.
    - `append()` function is used to append the newly produced data in the buffer.
    - `signal(s)` is used to set the semaphore variable "S" to "1" so that other processes can
    come into the critical section now because the production is done and the append
    operation is also done.
    - `signal(F)` is used to increase the semaphore variable "F" by one because after adding
    the data into the buffer, one space is filled in the buffer and the variable "F" must be
    updated.
    
- Pseudo-code for the consumer :
    
    ```jsx
    while(T){
    wait(F)
    wait(S)
    take()
    signal(S)
    signal(E)
    use()
    }
    ```
    
    - Code Explanation➖
        - `while()` is used to consume data, again and again, if it wishes to consume, again and
        again.
        - `wait(F)` is used to decrease the semaphore variable "F" by one because if some data is
        consumed by the consumer then the variable "F" must be decreased by one.
        - `wait(S)` is used to set the semaphore variable "S" to "0" so that no other process can
        enter into the critical section.
        - take() function is used to take the data from the buffer by the consumer.
        - `signal(S)` is used to set the semaphore variable "S" to "1" so that other processes can
        come into the critical section now because the consumption is done and the take
        operation is also done.
        - `signal(E)` is used to increase the semaphore variable "E" by one because after taking
        the data from the buffer, one space is freed from the buffer and the variable "E" must
        be increased.
        - `use()` is a function that is used to use the data taken from the buffer by the process to
        do some operation
        

---

### Race Condition

- Two or more processes read and write some shared data, and the final result depends on the exact timing of the process, called race conditions.

**Race Condition in OS :**

- Race Condition in Multi Threading Scenario : A race condition is a situation that develops when many threads share a resource or execute the same piece of code in a multithreaded context. Inappropriate handling of this might result in an unfavorable scenario where the output state depends on the threads execution order.
- Race Condition in Multi Processing Scenario : When two computer program processes try to access the same resource simultaneously, they happen and disrupt the system.
- Race Condition in Critical Section Area Problem : A race condition is a potential scenario that might happen within a critical section area. This occurs when different results from the execution of numerous threads in a crucial region are obtained depending on the execution order of the threads.

---

### Mutual Exclusion and Critical Zone

- To avoid race condition, we need to use some means to ensure that when a process uses a shared variable or file, other processes cannot do the same thing. Basically Mutually Exclusive.
- **Critical Zone :** The critical section refers to the segment of code where processes access shared resources, such as common variables and files, and perform write operations on them
- **Mutual Exclusive Scheme :** The essence of mutual exclusion is to prevent multiple processes from entering the critical region at the same time.
- **Shielding Interruption** : If we allow process A to shield all interrupts immediately after entering the critical area and respond to interrupts only after leaving the critical area, then even if interrupts occur, the CPU will not switch to other processes, so process A can safely modify the file content at this time, without worrying that other processes will interfere with its work.
    - Drawbacks :
        1. First, if there are more than one CPU, then process A can not shield interruption to other CPUs, it can only shield the CPU that is dispatching it, so the process dispatched by other CPUs can still enter the critical area.
        2. Power : If the process masks the interrupt and no longer responds to the interrupt, then a process may
        hang up the entire operating system.
- **Lock Variables :** Perhaps by setting a lock flag bit and setting its initial value to 0, when a process wants to enter the critical zone, it first checks whether the lock value is 0, if 0, then it is set to 1, then it enters the critical zone, and after exiting the critical zone, it changes the lock value to 0; if the lock value is already 1 when checking, it means that other processes are already in the critical zone, so the process follows. The loop waits and constantly detects the value of the lock until it becomes zero.
    - Drawback : However, there are race conditions in this way, because when a process reads out a lock value of 0, before it sets its value to 1, another process is scheduled, and it reads the lock value of 0, so that both processes are in the critical zone at the same time.
- **Peterson’s Algorithm :**
    - Set turn to either 0 or 1, indicating which process can enter its critical section first.
    - Repeat Indefinitely
    - Set flag[i] to true, indicating that process i wants to enter its critical section
    - set turn to j , the other process index
    - While flag[j] is true and turns equals j, wait
    - Enter the critical section
    - set flag[i] to false, indicating that process i is done with its critical section
    - Remainder section

---

### Semaphores

- Semaphores are integer variables that are used to solve the critical section problem by using two atomic operations, wait and signal that are used for process synchronization.
    - `wait()` Function
    
    ```jsx
    wait(S) {
    while(S == 0); //there is ";" sign here
    S--;
    }
    ```
    
    - `signal()` Function
    
    ```jsx
    signal(S){
    S++;
    }
    ```
    
- There are two types of semaphores
    - **Binary Semaphores :** In Binary Semaphores, the value of the semaphore will be 0 or 1. Initially, the value of semaphore variable is set to 1 and if some process wants to use some resource then the *wait()* function is called and the value of the semaphore is changed to 0 from 1. The process then uses the resource and when it releases the resource then the *signal()* function is called and the value of the semaphore variable is increased to 1.
    - **Counting Semaphores :** In Counting semaphores, firstly, the semaphore variable is initialized with the number of resources available. After that, whenever a process needs some resource, then the wait() function is called and the value of the semaphore variable is decreased by one. The process then uses the resource and after using the resource, the signal() function is called and the value of the semaphore variable is increased by one. So, when the value of the semaphore variable goes to 0 i.e all the resources are taken by the process and there is no resource left to be used, then if some other process wants to use resources then that process has to wait for its turn. In this way, we achieve the process synchronization.