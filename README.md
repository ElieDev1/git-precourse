def find_smallest_factors(number):
    smallest_factor = None

    for i in range(2, int(number**0.5) + 1):
        if number % i == 0:
            smallest_factor = i
            break

    if smallest_factor is not None:
        second_factor = number // smallest_factor
        return smallest_factor, second_factor
    else:
        return None

user_input = int(input("Enter a number: "))

factors = find_smallest_factors(user_input)

if factors is not None:
    smallest_factor, second_factor = factors
    print(f"The smallest two numbers that can be multiplied to get {user_input} are {smallest_factor} and {second_factor}.")
else:
    print(f"{user_input} is a prime number or 1, and it cannot be factored into two smaller numbers.")