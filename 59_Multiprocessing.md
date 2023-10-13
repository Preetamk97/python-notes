```py
# *********************************
# Python multiprocessing
# *********************************
# multiprocessing = running tasks in parallel on different cpu cores. 
#                   bypasses GIL used for threading.

# multiprocessing = better for cpu bound tasks (heavy cpu usage)
# multithreading = better for io bound tasks (waiting around)
# ******************************************************************************************************

import multiprocessing
import threading
import time

# We will create threads and processes from the below function
def counter(num):
    count = 0
    while count<num:
        count += 1
    print("My count has reached to ",count)


def main():
    #*******************************************************************************************************
    # Creating Processes for running the counter(num) function where num = 500 million => CPU Intensive task. 
    # Very similar to creaating a Thread
    a = multiprocessing.Process(target=counter, args=(500000000,))  # Process a for counting to 500 Million
    b = multiprocessing.Process(target=counter, args=(500000000,))  # Process b for counting to 500 Million

    # target=counter, args=(500000000,)  ==> counter(500000000,)
    # The comma in args=(500000000,) is neccessary to differentiate it from a variable (500000000-->integer).

    # Creating a performance counter - To record the start time of the processes
    start_time = time.perf_counter()

    # # Starting the processes
    # a.start()
    # b.start()

    # # Wait till the process a finishes - before proceeding further
    # a.join()
    # b.join()

    # Creating a performance counter - To record the end time of the processes
    end_time = time.perf_counter()

    time_taken = end_time-start_time
    print(f"Total time taken by processes 'a' and 'b' to complete execution : {time_taken} seconds")
    # My count has reached to  500000000
    # My count has reached to  500000000
    # Total time taken by processes 'a' and 'b' to complete execution : 44.7392490000002 seconds

    #*******************************************************************************************************

    # Now lets us create two threads x & y and repeat the same code as above - this time using Multithreading.
    x = threading.Thread(target=counter, args=(500000000,))     # Thread a for counting to 500 Million
    y = threading.Thread(target=counter, args=(500000000,))     # Thread b for counting to 500 Million

    # Creating a performance counter - To record the start time of the threads
    start_time = time.perf_counter()

    # # Starting the threads
    # x.start()
    # y.start()

    # # Wait till the process a finishes - before proceeding further
    # x.join()
    # y.join()

    # Creating a performance counter - To record the end time of the processes
    end_time = time.perf_counter()

    time_taken = end_time-start_time
    print(f"Total time taken by threads 'x' and 'y' to complete execution : {time_taken} seconds")
    # My count has reached to  500000000
    # My count has reached to  500000000
    # Total time taken by threads 'x' and 'y' to complete execution : 73.34747360000028 seconds

    #*******************************************************************************************************
    # Important Observation:
        # 1. time taken by processes a & b to complete (44 seconds) was almost half of the time taken by threads x & y to complete (73 seconds).

        # Explanation:
        # ------------ 
            # In Multithreading:
            # """"""""""""""""""

            #===Thread x===|===Thread y===|===Thread x===|===Thread y=====|=> Running Concurrently. 
            #                                                                Only 1 Thread at a time.
            #                                                                Python interpreter uses  
            #                                                                only 1 CPU core.

            # In Multiprocessing:
            # """""""""""""""""""

            #==================================== Process a ==========================|=> Multiple processes 
            #==================================== Process b ==========================|=> run parallely.
            #                                                                             Python interpreter   
            #                                                                             uses multiple CPU cores.
    #*************************************************************************************************************

    print(multiprocessing.cpu_count())  # 4    # Prints the number of cpu cores available in our system.


if __name__ == "__main__":
    main()
```