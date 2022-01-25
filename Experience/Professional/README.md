# Professional Experience

## Cyber Black Friday

This project is a dummy online shopping system. 
Before conducting this project, I was curious how a shopping system should be designed 
so that it won't crash or perform poorly when lots of people make orders at the same time.
As we know, we could not interact with database frequently since it is time-consuming.
After conducting some research, I found that integrating Redis into the system is a good solution. 
Redis is a NoSQL database which stores its data into memory instead of disk, which means reading and writing data would be much faster compared with traditional database.
In my project, first I store all the orders into Redis. 
When the system notices that the stock is empty, it would save all the orders from Redis to MySQL

to be continued