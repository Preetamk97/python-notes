```PY
# **********************************************************
# Python daemon threads
# **********************************************************

# daemon thread =  daemon threads are a type of thread that runs in the background, providing support to the main program but not preventing the program from exiting. 
#
# The program does not exit until and unless execution of all the non-daemon threads is complete. When all non-daemon threads complete their execution, the program exits, terminating any remaining daemon threads abruptly.
#
# ex. background tasks, garbage collection, waiting for input, long running processes

import threading
import time


# Function for daemon thread
def timer():
    count = 0
    while True:
        time.sleep(1)
        count += 1
        print("logged in for: ", count, "seconds")

x = threading.Thread(target=timer, daemon=True)     # Creating a deamon thread
x.start()                                           # Staring the thread


# Function for main(non-daemon) thread
def hello():
    for x in range(1,11):
        time.sleep(2)
        print("Hello World")

y = threading.Thread(target=hello)
# y.setDaemon(True)                                 # Converting a non-deamon thread to daemon thread
                                                    # However, this can be done only BEFORE starting the thread .
y.start()
 

# As soon as the non-daemon thread (y) completes its execution, 
# the program exits, terminating the remaining daemon thread (x) abruptly.


# Output:
#########
# logged in for:  1 seconds
# Hello World
# logged in for:  2 seconds
# logged in for:  3 seconds
# Hello World
# logged in for:  4 seconds
# logged in for:  5 seconds
# Hello World
# logged in for:  6 seconds
# logged in for:  7 seconds
# Hello World
# logged in for:  8 seconds
# logged in for:  9 seconds
# Hello World
# logged in for:  10 seconds
# logged in for:  11 seconds
# Hello World
# logged in for:  12 seconds
# logged in for:  13 seconds
# Hello World
# logged in for:  14 seconds
# logged in for:  15 seconds
# Hello World
# logged in for:  16 seconds
# logged in for:  17 seconds
# Hello World
# logged in for:  18 seconds
# logged in for:  19 seconds
# Hello World
#
# <program exits>
# *******************************************************************************************************
```