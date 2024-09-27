# Queuing System in JavaScript by lmg 

This project implements a queuing system in JavaScript using Redis as the backend data store. Below is the README file detailing how to set up and run the project, along with descriptions of each task:

## Project Setup

### Installing Redis
1. Download, extract, and compile the latest stable Redis version (higher than 5.0.7) from [Redis Downloads](https://redis.io/downloads/):

```bash
$ wget http://download.redis.io/releases/redis-6.0.10.tar.gz
$ tar xzf redis-6.0.10.tar.gz
$ cd redis-6.0.10
$ make
```

2. Start Redis in the background with `src/redis-server`:

```bash
$ src/redis-server &
```

3. Make sure the server is working with:

```bash
$ src/redis-cli ping
PONG
```

4. Using the Redis client, set the value of a key:

```bash
$ src/redis-cli set Holberton School
OK
$ src/redis-cli get Holberton
"School"
```

5. Kill the server with the process ID of the `redis-server`:

```bash
$ kill [PID_OF_Redis_Server]
```

6. Copy the `dump.rdb` from the `redis-5.0.7` directory into the root of the Queuing project.

### Requirements

- Node.js and npm should be installed on your system.
- Clone the GitHub repository: `alx-backend`
- Navigate to the directory `0x03-queuing_system_in_js`.

## Tasks

1. **Node Redis Client**: Connect to the Redis server and log connection status.
2. **Node Redis client and basic operations**: Perform basic Redis operations like setting and retrieving values.
3. **Node Redis client and async operations**: Perform Redis operations asynchronously using `promisify`.
4. **Node Redis client and advanced operations**: Store hash values in Redis and retrieve them.
5. **Node Redis client publisher and subscriber**: Create Redis publisher and subscriber clients.
6. **Create the Job creator**: Create a queue with Kue and add jobs to it.
7. **Create the Job processor**: Process jobs from the queue using Kue.
8. **Track progress and errors with Kue: Create the Job creator**: Track job creation progress and errors.
9. **Track progress and errors with Kue: Create the Job processor**: Track job processing progress and errors.
10. **Writing the job creation function**: Create jobs and add them to the queue.
11. **Writing the test for job creation**: Write tests for the job creation function.
12. **In stock?**: Implement a web application to manage product stock using Redis.
13. **Can I have a seat?**: Implement a seat reservation system using Redis and Kue.

## Running the Project

- Each task has its own JavaScript file (e.g., `0-redis_client.js` for Task 1).
- Run each file using `npm run dev <filename>` (e.g., `npm run dev 0-redis_client.js`).

## Testing

- Run tests for the job creation function using `npm test 8-job.test.js`.

## Notes

- Make sure to have Redis running before executing any of the tasks.
- Ensure the correct Redis server configuration in each file where Redis is used.
