#Data structure design

def binary_search(arr, target):
    low = 0
    high = len(arr) - 1

    while low <= high:
        mid = (low + high) // 2

        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            low = mid + 1
        else:
            high = mid - 1

    return -1

# Example usage
numbers = [2, 4, 7, 10, 14, 19, 22, 25, 29, 30]
target = 19
result = binary_search(numbers, target)

if result != -1:
    print(f"Element {target} found at index {result}.")
else:
    print("Element not found.")


