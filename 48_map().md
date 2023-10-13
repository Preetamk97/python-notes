# Example 1:

```py
# map() =   applies a function to each item in an iterable (list, tuple, etc.)
#
# map(function,iterable)


# Consider a list which contains some items and their prices in USD
store = [("shirt",20.00),
         ("pants",25.00),
         ("jacket",50.00),
         ("socks",10.00)]

to_euros = lambda item: (item[0],item[1]*0.92)      # This lambda function takes an item from the list, 
                                                    # keeps the item name (item[0]) as it is and,
                                                    # converts the item price from USD to Euros
                                                    # 1 US Dollar = 0.92 Euro

store_euros = list(map(to_euros, store))            # map() function applies the to_euros() function 
                                                    # to every item of the store[] list
                                                    # and returns a map object as result
                                                    # This map object can be then typecasted to any iterable type (list, set, tuple)
                                                    # Here, we are type casting the map object as a list

for i in store_euros:
    print(i)
# ('shirt', 18.400000000000002)
# ('pants', 23.0)
# ('jacket', 46.0)
# ('socks', 9.200000000000001)
```

# Example 2:

```py
def double(x):
    return x*2

num_list = [1, 2, 3, 4, 5, 6, 7]

doubled_num_list = list(map(double, num_list))

print(doubled_num_list)
# [2, 4, 6, 8, 10, 12, 14]
``` 