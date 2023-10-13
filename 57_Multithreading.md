```py
# ****************************************************
# Python Multithreading Tutorial
# ****************************************************
# thread =  A flow of execution. Like a separate new program with its own set of instructions..
# Concurrency - the ability to have multiple threads or tasks making progress simultaneously.
# When multiple threads are running at the same time, each thread takes a turn in running to achieve concurrency.
# GIL = (global interpreter lock) = allows only one thread to hold the control of the Python interpreter at any one time.
# In Python, when multiple threads are running at the same time, the concept of concurrency is achieved through time slicing or context switching. Time slicing is the process by which the operating system allocates a certain amount of time for each thread to execute before switching to another thread. This gives the illusion of parallelism, as each thread appears to be running simultaneously.
# The operating system divides the available CPU time into small time slices and assigns each thread a slice to execute its instructions. Once a thread's time slice is up, the operating system pauses its execution and switches to another thread, allowing it to execute for its allocated time slice. This process continues, giving the appearance of multiple threads executing concurrently.
# By using threads, you can divide a program into smaller units of work that can run concurrently. Each thread can perform its tasks independently and make progress while other threads are running.

# There are two types of programs:
#
# cpu bound programs = program/task that spends most of it's time waiting for internal events (CPU intensive).
#                      These programs can benifit from multiprocessing.
#
# io bound programs = program/task that spends most of it's time waiting for external events (user input, web-  
#                     scraping). 
#                     These programs can benifit from multithreading.

# Code Demo:
#################################################################################################################
#################################################################################################################

import threading        # Importing threading module
import time             # Importing time module

start_time = time.perf_counter()        # Records the current time on monotonic clock

def eat_breakfast():
    time.sleep(3)               # Stops the program for 3 seconds    
    print("You eat breakfast")


def drink_coffee():
    time.sleep(4)               # Stops the program for 4 seconds
    print("You drank coffee")


def study():
    time.sleep(5)               # Stops the program for 5 seconds
    print("You finish studying")


# Creating a thread for executing the eat_breakfast() func. Any arguments must be passed to the args=() attribute.
x = threading.Thread(target=eat_breakfast, args=())
x.start()   # Starting the thread

# Creating a thread for executing the drink_coffee() func. Any arguments must be passed to the args=() attribute.
y = threading.Thread(target=drink_coffee, args=())
y.start()   # Starting the thread

# Creating a thread for executing the study() func. Any arguments must be passed to the args=() attribute.
z = threading.Thread(target=study, args=())
z.start()   # Starting the thread

# x.join()    # Before proceeding further, wait till the execution of thread x completes.
# y.join()    # Before proceeding further, wait till the execution of thread y completes.
# z.join()    # Before proceeding further, wait till the execution of thread z completes.

print(threading.active_count())     # gives the active number of threads running.   
print(threading.enumerate())        # returns a list of currently active threads   

end_time = time.perf_counter()      # Records the current time on monotonic clock   
# The time.perf_counter() function in Python is used to measure the elapsed time in seconds with the highest available resolution. It returns a floating-point number representing a monotonic clock, meaning it cannot go backward and is unaffected by system clock adjustments.
# The perf_counter() function is commonly used for performance testing, benchmarking, and timing operations in Python code. By measuring the time before and after a particular section of code, you can calculate the elapsed time and evaluate the efficiency or speed of that code.
time_taken_to_finish_the_main_thread = end_time-start_time
print(time_taken_to_finish_the_main_thread)


# Output on un-commenting  x.join(), y.join(), z.join()  lines of code: Threads run one by one
# ############################################################################################
# You eat breakfast
# You drank coffee
# You finish studying
# 1
# [<_MainThread(MainThread, started 13060)>]
# 5.006935699988389


# Output on keeping the  x.join(), y.join(), z.join()  lines of code commented: Threads run concurrently
# ########################################################################################################
# 4
# [<_MainThread(MainThread, started 15340)>, <Thread(Thread-1 (eat_breakfast), started 18360)>, <Thread(Thread-2 (drink_coffee), started 17740)>, <Thread(Thread-3 (study), started 9684)>]
# 0.0030692000000271946
# You eat breakfast
# You drank coffee
# You finish studying

# ***********************************************************************************************************
```