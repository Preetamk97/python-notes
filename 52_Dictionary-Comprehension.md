```py
# dictionary comprehension = a programming technique of creating dictionaries using an expression
#                            can replace for loops and certain lambda functions
#
# dictionary = {key: expression for (key,value) in iterable}
# dictionary = {key: expression for (key,value) in iterable if conditional}
# dictionary = {key: (if/else) for (key,value) in iterable}
# dictionary = {key: function(value) for (key,value) in iterable}

# Example 1: 
# -------------------------------------------------------------------------
cities_vs_Fahrenheit = {'New York': 32, 'Boston': 75, 'Los Angeles': 100, 'Chicago': 50}

# Converting all the fahrenheit values to celsius values and creating a new dictionary
# C = 5/9 x (F-32)
# dictionary = {key: expression for (key,value) in iterable}
cities_vs_Celsius = {key: ((value-32)*(5/9)) for (key,value) in cities_vs_Fahrenheit.items()}

print(cities_vs_Celsius)
# {'New York': 0.0, 'Boston': 23.88888888888889, 'Los Angeles': 37.77777777777778, 'Chicago': 10.0}


# Example 2:
# -------------------------------------------------------------------------
weather = {'New York': "snowing", 'Boston': "sunny", 'Los Angeles': "sunny", 'Chicago': "cloudy"}

# creating a dictionary of only those "key":"value" pairs from weather dictionary where value = "sunny"
# dictionary = {key: expression for (key,value) in iterable if conditional}
sunny_weather = {key: value for (key,value) in weather.items() if value == "sunny"}

print(sunny_weather)
# {'Boston': 'sunny', 'Los Angeles': 'sunny'}

# Example 3
# -------------------------------------------------------------------------
cities = {'New York': 32, 'Boston': 75, 'Los Angeles': 100, 'Chicago': 50}

# dictionary = {key: (if/else) for (key,value) in iterable}
city_descriptions = {key: ("WARM" if value >= 40 else "COLD") for (key,value) in cities.items()}

print(city_descriptions)
# {'New York': 'COLD', 'Boston': 'WARM', 'Los Angeles': 'WARM', 'Chicago': 'WARM'}

# Example 4
# -------------------------------------------------------------------------
def check_temp(value):
    if value >= 70:
        return "HOT"
    elif 69 >= value >= 40:
        return "WARM"
    else:
        return "COLD"


cities = {'New York': 32, 'Boston': 75, 'Los Angeles': 100, 'Chicago': 50}

# dictionary = {key: function(value) for (key,value) in iterable}
city_descriptions = {key: check_temp(value) for (key,value) in cities.items()}

print(city_descriptions)
# {'New York': 'COLD', 'Boston': 'HOT', 'Los Angeles': 'HOT', 'Chicago': 'WARM'} 

# -------------------------------------------------------------------------
```