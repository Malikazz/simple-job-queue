# simple-job-queue
A job que intended for use for API communication. Can be used with or without a in memory database.

## Why 
I have a use case currently where their is no usable memory data base on the server but we require a job que. So building a job que that can funciton by reserving it own little memory db. With the ability to later use a memory database. Sure theres a solve out there I could just use but whats the fun in that. 

## General use
The system will rely on a toml file `settings.toml` to supply the apps setup. Basic setup will include the following settings.
```toml
host = "localhost"
max_queue_time_ms = 600000
max_db_size = 2147483648

# Only required if your connecting to an external db
[database]
enabled = false
port = 0000
ip = 127.0.0.1
```
