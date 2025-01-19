# Prime Number Checker
# MIT License

def is_prime(n):
    """
    Check if a given number is a prime number.

    Parameters:
        n (int): The number to check.

    Returns:
        bool: True if n is prime, False otherwise.
    """
    if n <= 1:
        return False  # Numbers less than or equal to 1 are not prime
    if n == 2:
        return True  # 2 is a prime number

    # Check divisibility from 2 to the square root of n
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return False  # n is divisible by i, so it is not prime

    return True  # n is prime

# Example usage
if __name__ == "__main__":
    number = int(input("Enter a number to check if it is prime: "))
    if is_prime(number):
        print(f"{number} is a prime number.")
    else:
        print(f"{number} is not a prime number.")

