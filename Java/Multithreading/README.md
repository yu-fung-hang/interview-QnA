# Multithreading

the ability of a CPU to provide multiple threads of execution concurrently

## Thread & Process

**Process**: an executing program

**Thread**: a component of a process, the smallest sequence of programmed instructions that can be managed independently by a scheduler. Multiple threads share resources such as memory.

## synchronous & asynchronous

When you execute something **synchronously**, you wait for it to finish before moving on to another task. 

When you execute something **asynchronously**, you can move on to another task before it finishes. 

## Ways of implementing multithreading

1. Inherit from `Thread` class and override `run()`;

2. Implement `Runnable` interface and implement `run()`;

3. **(not common)** Implement `Callable` interface and implement `call()`;

## run() & start()

**start()**: a new thread is created and code inside run() method is executed in that new thread;

**run()**: no new thread is created and code inside run() method will execute on the current thread and no multi-threading will take place.

## notify() & notifyAll()

**notify()**: wakes up a single thread that is waiting on this object's monitor arbitrarily. 

**notifyAll()**: wakes up all threads that are waiting on this object's monitor. 

Both methods should only be called by a thread that is the owner of this object's monitor.

## sleep() & wait()

**sleep()**:
 
1. A method of Class `Thread`;

2. The thread does not lose ownership of any monitors.

3. Sends the current thread into the ¡°Not Runnable¡± state for some amount of time.

**wait()**:

1. A method of Class `Object`;

2. The thread releases ownership of this monitor and waits until another thread call the notify method or the notifyAll method.

3. Can only be called from a synchronized block.

## stop() & suspend()

**stop()**: unlock all the monitors that it has locked, which might cause inconsistency.

**suspend()**: does not release locks, might cause dead-lock.

## interrupt()

An interrupt is an indication to a thread that it should stop what it is doing and do something else. It's up to the programmer to decide exactly how a thread responds to an interrupt, but it is very common for the thread to terminate.

**How to handle interruption**:

1. If the thread is frequently invoking methods that throw InterruptedException, it simply returns from the run method after it catches that exception.

2. If a thread goes a long time without invoking a method that throws InterruptedException, then it should periodically invoke Thread.interrupted, and terminate the thread if it returns true.

## join()

to be continued

## Ways of implementing synchronization

to be continued

## daemon threads & user threads

**daemon threads**: low-priority threads whose only role is to provide services to user threads (example: garbage collector thread);

**user threads**: high-priority threads. JVM exits once all user threads have finished their execution.