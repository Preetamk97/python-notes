```py
# recursion = a function that calls itself from within.
#             helps to visualize a complex problem into basic steps.
#             problems can be solved more easily.
#             iterative = faster, complex
#             recursive = slower, simpler

# ---- EXAMPLE 1 : Walking 100 Steps ----

# ITERATIVE APPROACH
# def walk(steps):
#     for step in range(1, steps+1):
#         print(f"You take step #{step}")


# RECURSIVE APPROACH
def walk(steps):
    if steps == 0:
        return      # return nothing means stop the function
    walk(steps - 1)
    print(f"You take step #{steps}")

walk(100)


# ---- EXAMPLE 2 : Finding Factorial -------

# ITERATIVE APPROACH
# def factorial(num):
#     result = 1
#     for i in range (1, num+1):
#         result = result * i
#     return result


# RECURSIVE APPROACH
def factorial(num):
    if num == 1:
        return 1
    result = num * factorial(num-1)
    return result

result = factorial(5)
print(result)
```