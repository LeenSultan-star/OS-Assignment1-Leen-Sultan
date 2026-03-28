# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

[A process is an independent program with its own memory space, while a thread is a smaller unit of a process that shares memory with other threads. Threads are faster to create and require less overhead compared to processes. In this assignment, we used threads because they allow better performance and easier communication. Also, threads share the same memory, making data access faster.]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

[In Round-Robin scheduling, if a process does not finish within its time quantum, it is placed back in the ready queue.  ]

Example from my output:
```
[For example, in my output, process P1 ran for a short time and then returned to the queue.]
```

**Explanation of example:**
[This ensures fairness because every process gets a chance to execute. This behavior prevents any process from monopolizing the CPU.]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**: [P1 is in the New state when it is first created at the beginning of the simulation, before being added to the ready queue.
]

1. **Runnable**: [P1 becomes Runnable when it is added to the ready queue, as shown in the output: "P1 added to ready queue". At this point, it is ready to execute but waiting for CPU time.]

2. **Running**: [P1 is in the Running state when it starts executing on the CPU, as shown in the output: "P1 executing quantum [2645ms]".
]

1. **Waiting**: [P1 does not enter the Waiting state in this simulation because its burst time (2645ms) is less than the time quantum (4000ms). Therefore, it completes execution without being interrupted or waiting.]

2. **Terminated**: [P1 enters the Terminated state when it finishes execution completely, as shown in the output: "P1 finished execution!" and "Remaining time: 0ms".]

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [ Operating Systems (Time-Sharing Systems)]

**Description**: 
[Operating systems like Windows or Linux run multiple programs at the same time, such as browsers, editors, and background processes.]

**Why Round-Robin works well here**: 
[Round-Robin scheduling ensures fairness by giving each process a fixed time slice. It improves responsiveness and prevents any single process from monopolizing the CPU.]

### Example 2: [ Web Servers]

**Description**: 
[Web servers handle multiple client requests simultaneously when users access websites.]

**Why Round-Robin works well here**: 
[Round-Robin scheduling distributes CPU time evenly among requests, ensuring fast response times and preventing delays caused by long-running requests.]

---

## Summary

**Key concepts I understood through these questions:**
1. The lifecycle of a process (New, Runnable, Running, Terminated)
2. How Round-Robin scheduling works using time quantum 
3. The concept of context switching between processes

**Concepts I need to study more:**
1. The Waiting state and when it occurs (especially with I/O operations)
2. The difference between process scheduling and thread scheduling
