```py
# format specifiers = flags in {value:flags} = formats a value based on what flags are inserted while printing it.

pi = 3.14159    
e = 2.718281828459

# .(number)f = rounds to that many decimal places
# Below, rounding the value of 'pi' variable to 2 decimal places while printing it.
# Here, '.2f' is a 'format specifier flag' which formats the 'pi' value accordingly.
print(f"value of pi rounded to 2 decimal places: {pi:.2f}")
# Below, rounding the value of 'pi' variable to 3 decimal places while printing it.
print(f"value of pi rounded to 3 decimal places: {pi:.3f}")

# :(number) = allocate that many spaces while printing the value
print(f"value of pi is allocated 10 spaces to print :{pi:10}")
# value of pi is allocated spaces to print :   3.14159
print(f"value of e is allocated 20 spaces to print :{e:20}")
# value of e is allocated spaces to print :      2.718281828459

# :0(number) = allocate that many spaces while printing the value and fill the empty spaces with zero
print(f"value of pi is allocated 10 spaces to print with zero(0) padding :{pi:010}")
# value of pi is allocated 10 spaces to print with zero(0) padding :0003.14159
print(f"value of e is allocated 20 spaces to print with zero(0) padding :{e:020}")
# value of e is allocated 20 spaces to print with zero(0) padding :0000002.718281828459

# :< = left justify
print(f"value of pi is allocated 10 spaces to print and is left justified :{pi:<10}")
# value of pi is allocated 10 spaces to print and is left justified :3.14159
print(f"value of e is allocated 20 spaces to print and is left justified :{e:<20}")
# value of e is allocated 20 spaces to print and is left justified :2.718281828459

# :> = right justify
print(f"value of pi is allocated 10 spaces to print and is right justified :{pi:>10}")
# value of pi is allocated 10 spaces to print and is right justified :   3.14159
print(f"value of e is allocated 20 spaces to print and is right justified :{e:>20}")
# value of e is allocated 20 spaces to print and is right justified :      2.718281828459

# :^ = center align
print(f"value of pi is allocated 10 spaces to print and is center aligned :{pi:^10}")
# value of pi is allocated 10 spaces to print and is center aligned : 3.14159
print(f"value of e is allocated 20 spaces to print and is center aligned :{e:^20}")
# value of e is allocated 20 spaces to print and is center aligned :   2.718281828459

# :+ = indicates a positive value with a plus(+) sign
# :  = inserting a space in place of '+' also has the same effect
price1 = -80099.99
price2 = 300045899.46
print(f"price1 : {price1:+}")
print(f"price2 : {price2:+}")
# price1 : -80099.99
# price2 : +300045899.46

# :, = comma separator = adds commas to your number as per american convention
price1 = -80099.99
price2 = 300045899.46
print(f"price1 : {price1:,}")
print(f"price2 : {price2:,}")
# price1 : -80,099.99
# price2 : 300,045,899.46


# :% = percentage format
discount1 = 20/100
discount2 = 45/100
print(f"discount1 : {discount1:%}")
print(f"discount2 : {discount2:%}")
# discount1 : 20.000000%
# discount2 : 45.000000%


# Mix and Match Format Specifiers Excercise
# ******************************************

distance = 899999999999.5698450562002232

# Print the number such that it is
    #   rounded off to 2 decimal places
    #   separated by commmas
    #   preceded by a '+' sign if positive

print(f"distance = {distance:+,.2f}")
# distance = +899,999,999,999.57
```