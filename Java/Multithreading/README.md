# Multithreading

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

## Difference between run() and start()

**start()**: a new thread is created and code inside run() method is executed in that new thread;

**run()**: no new thread is created and code inside run() method will execute on the current thread and no multi-threading will take place.

## Difference between notify() and notifyAll()

**notify()**: wakes up a single thread that is waiting on this object's monitor arbitrarily. 

**notifyAll()**: wakes up all threads that are waiting on this object's monitor. 

Both methods should only be called by a thread that is the owner of this object's monitor.

## Difference between sleep() and wait()

**sleep()**:
 
1. A method of Class `Thread`;

2. The thread does not lose ownership of any monitors.

3. Sends the current thread into the ¡°Not Runnable¡± state for some amount of time.

**wait()**:

1. A method of Class `Object`;

2. The thread releases ownership of this monitor and waits until another thread call the notify method or the notifyAll method.

3. Can only be called from a synchronized block.

## stop() and suspend() are deprecated

**stop()**: unlock all the monitors that it has locked, which might cause inconsistency.

**suspend()**: does not release locks, might cause dead-lock.

## interrupt()

to be continued

## Ways of implementing synchronization

to be continued

## Daemon 