# Mycode
```py
def div_mult_approx_numbers(numbers):
    x = min(numbers, key=lambda x: len(str(x).rstrip('0')))
    y = int(str(x).split('.')[1] if '.' in str(x) else '')
    print(x,y)

    rounded_numbers = [round(num, y + 1) for num in numbers]
    print(rounded_numbers)
    result = rounded_numbers[0]
    result_2 = rounded_numbers[0]
    for num in rounded_numbers[1:]:
        result *= num

    for num in rounded_numbers[1:]:
        result_2 = result_2 / num

    result_str = format(result, f".{y}f")
    result_str_2 = format(result_2, f".{y}f")


    return float(result_str), float(result_str_2)

numbers = [3.28, 2.71828, 1.2]
result = div_mult_approx_numbers(numbers)
print(result)
```
