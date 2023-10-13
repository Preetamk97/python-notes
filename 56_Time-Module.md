```py
#mporting time module
import time 

#*****************************************************************************************************************

print(time.ctime(0))
# Thu Jan  1 05:30:00 1970
# time.ctime() -- converts a time expressed in seconds since epoch time to a readable string format
# time.ctime(0) -- gives the exact epoch time of the system in readable string format
# Epoch time is [the exact moment] from which the measurement of time begins in our system. 
# Epoch = (reference point) when your computer thinks time began 

print(time.ctime(100000))
# Fri Jan  2 09:16:40 1970
# time.ctime(100000) -- gives us the local time in string format for 100,000 seconds past the epoch time

print(time.time())
# 1684560594.860824
# time.time()  --  returns the numbers of seconds that have passed since epoch to current time.


print(time.ctime(time.time()))     # Gives the current date and time
# Sat May 20 11:04:54 2023

#*****************************************************************************************************************

# time.localtime(seconds) --- Converts the given seconds since Epoch time to a time tuple. 
# When 'seconds' is not passed in, converts the current system time (taken as seconds passed since epoch time) to a time tuple instead.
print(time.localtime())     
# time.localtime() -- is giving the time tuple of the current system time.
# time.struct_time(tm_year=2023, tm_mon=5, tm_mday=20, tm_hour=12, tm_min=16, tm_sec=2, tm_wday=5, tm_yday=140, tm_isdst=0)

#*****************************************************************************************************************

# converting the output of time.localtime() to a readable string time format 
# time.strftime("time_format", time_tuple) : Convert a time tuple to a string according to a format specification.
time_tuple = time.localtime()
formatted_time = time.strftime("%H:%M:%S  %I:%M:%S %p  %zGMT  %d/%m(%b/%B)/%Y  %a/%A  %c", time_tuple)

print(formatted_time)
# 12:16:02  12:16:02 PM  +0530GMT  20/05(May/May)/2023  Sat/Saturday  Sat May 20 12:16:02 2023
# time_format explained:
#************************
# "%H:%M:%S  %I:%M:%S %p  %zGMT  %d/%m(%b/%B)/%Y  %a/%A  %c"
#       %H = Hour (24-hour clock) as a decimal number [00,23]. 
#       %M = Minute as a decimal number [00,59]. 
#       %S = Second as a decimal number [00,61]. 
#       %I = Hour (12-hour clock) as a decimal number [01,12]. 
#       %p = AM or PM.
#       %z = Time zone offset from GMT. 
#       %d = Day of the month as a decimal number [01,31]. 
#       %m = Month as a decimal number [05,12]. 
#       %b = Abbreviated month name. 
#       %B = Full month name. 
#       %Y = Year as a decimal number [2023]. 
#       %a = Abbreviated weekday name. 
#       %A = Full weekday name. 
#       %c = Appropriate date and time representation.


#***************************************************************************************************************** 
# time.gmtime(seconds) -- Convert seconds since the Epoch to a time tuple expressing UTC (a.k.a. GMT - Greenwich Mean Time) at that exact moment. When 'seconds' is not passed in, convert the current time instead -> to GMT.
print(time.gmtime())
# time.struct_time(tm_year=2023, tm_mon=5, tm_mday=20, tm_hour=6, tm_min=59, tm_sec=24, tm_wday=5, tm_yday=140, tm_isdst=0)

# converting the output of time.gmtime() to a readable string time format
time_tuple = time.gmtime()
formatted_time = time.strftime("%H:%M:%S  %I:%M:%S %p  %zGMT  %d/%m(%b/%B)/%Y  %a/%A  %c", time_tuple)
print(formatted_time)
# 07:00:25  07:00:25 AM  +0530GMT  20/05(May/May)/2023  Sat/Saturday  Sat May 20 07:00:25 2023
# As of this moment, this is the current GMT - the current time of London,UK.

#*****************************************************************************************************************

# Converting a time string to a time tuple
# time.strptime("time_string", "time_format") : Parse a string to a time tuple according to a format specification.
# Here, "time_format" basically defines what is the structure of the "time_string" that is passed by us - so that interpreter can identify which one is what in our "time_string".
time_string = "10 May, 2011"
time_tuple = time.strptime(time_string, "%d %b, %Y")
print(time_tuple)
# time.struct_time(tm_year=2011, tm_mon=5, tm_mday=10, tm_hour=0, tm_min=0, tm_sec=0, tm_wday=1, tm_yday=130, tm_isdst=-1)

#*****************************************************************************************************************

# time.asctime(time_tuple) = Converts a time tuple (up to 9 elements) to a readable string, e.g. 'Sat Jun 06 16:26:11 1998'. When the time tuple is not present, current time tuple as returned by localtime() is used.
# time_tuple format : (year, month, day, hours, minutes, secs, day of the week, day of the year, dst)
time_tuple = (2020, 4, 20, 4, 20, 0, 0, 0, 0)
time_string = time.asctime(time_tuple)
print(time_string)
# Mon Apr 20 04:20:00 2020

#*****************************************************************************************************************

# time.mktime(time_tuple) = Converts a time tuple in local time to seconds since the Epoch.
# time_tuple format : (year, month, day, hours, minutes, secs, day of the week, day of the year, dst)
time_tuple = (2020, 4, 20, 4, 20, 0, 0, 0, 0)
time_string = time.mktime(time_tuple)
print(time_string)
# 1587336600.0

#*****************************************************************************************************************
```