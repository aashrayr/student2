# Input and greet
name = input("Enter your name: ")
print(f"Greetings, {name}!")

# Fruits list
fruits = [
    "apple",
    "banana",
    "cherry"
]
print("Fruit List:")
for fruit in fruits:
    print(f"- {fruit}")

# Student information
student = {
    "name": "John",
    "age": 20,
    "grade": "A"
}
print("\nStudent Information:")
for key, value in student.items():
    print(f"{key.capitalize()}: {value}")

# Iteration with range
print("\nIteration:")
for i in range(1, 6):
    print(f"Iteration {i}")

# Function to calculate average
def calculate_average(numbers):
    return sum(numbers) / len(numbers)

numbers = [12, 24, 36, 48, 60]
average = calculate_average(numbers)
print("\nAverage:", average)

# Check if number is even or odd
num = int(input("\nEnter a number: "))
parity = "even" if num % 2 == 0 else "odd"
print(f"{num} is {parity}.")

# Function to calculate factorial
def factorial(n):
    return 1 if n == 0 else n * factorial(n - 1)

number = int(input("\nEnter a number to calculate its factorial: "))
result = factorial(number)
print(f"Factorial of {number} is {result}.")


```python
def get_student_info():
    students = []
    ages = []
    
    while True:
        student_name = input("Enter student name: ").capitalize()
        student_age = int(input("Enter student age: "))
        students.append(student_name)
        ages.append(student_age)
        
        add_another = input('Would you like to add another student? [Y/N]').lower()
        if add_another != 'y':
            break
            
    return students, ages

def get_student_grades(students):
    grades = {}
    
    for student in students:
        grades[student] = []
        
        while True:
            grade = int(input(f"Enter {student}'s grade: "))
            grades[student].append(grade)
            
            add_another = input('Would you like to add another grade? [Y/N]').lower()
            if add_another != 'y':
                break
                
    return grades

def calculate_average(grades):
    total = sum(sum(scores) for scores in grades.values())
    num_students = sum(len(scores) for scores in grades.values())
    
    if num_students == 0:
        return 0
    
    return total / num_students

def assess_performance(average_grade):
    if average_grade >= 90:
        return "Excellent"
    elif average_grade >= 80:
        return "Good"
    elif average_grade >= 70:
        return "Satisfactory"
    else:
        return "Needs Improvement"

def print_student_details(students, grades, ages):
    for student, age in zip(students, ages):
        avg_grade = sum(grades[student]) / len(grades[student])
        print(f"{student}: Age - {age}, Average Grade - {avg_grade:.2f}")

def main():
    print("Welcome to the Student Performance Evaluation System\n")
    
    students, ages = get_student_info()
    grades = get_student_grades(students)
    
    print("\nStudent Details:")
    print_student_details(students, grades, ages)
    
    average_grade = calculate_average(grades)
    print(f"\nClass Average Grade: {average_grade:.2f}")
    
    performance = assess_performance(average_grade)
    print(f"\nPerformance: {performance}")

if __name__ == "__main__":
    main()
```



CORRECTIONS: 
62: Correct ANswer C... Mine:B

Incorrect. Any user with a basic account can receive targeted advertisements, regardless of whether they are interested in health and fitness.

Correct. Users with a premium account do not receive advertisements.

63: Correct A and D.. Mine A and C

Correct. When input1 and input2 are both true, the expressions (NOT input1) and (NOT input2) are both false, so (NOT input1) OR (NOT input2) will evaluate to false. In all other cases, either (NOT input1) or (NOT input2) (or both) will evaluate to true, so (NOT input1) OR (NOT input2) will evaluate to true.

Correct. When input1 and input2 are both true, the expression (input1 AND input2) is true, so NOT (input1 AND input2) will evaluate to false. In all other cases, (input1 AND input2) will evaluate to false, so NOT (input1 AND input2) will evaluate to true.


66: Correct A Mine B

Incorrect. This code segment does not work as intended. For example, if timer is greater than 60, bonus will be initially assigned 1500, then decreased to 1000 in the first IF block. As a result, bonus will be assigned 1000 instead of the intended 1500.

Correct. In this code segment, if timer is greater than 60, bonus is assigned 1500 in the first IF block. If timer is between 30 and 60, inclusive, bonus is assigned 1000 in the second IF block. If timer is less than 30, bonus is assigned 500 in the third IF block. The correct number of bonus points is assigned to bonus for all possible values of timer.

68: Correct     AC Mine AD

Correct. The code segment will iterate over myList from right to left, removing each element that is equal in value to the element immediately preceding it. For this list, the code segment will remove the sixth element (10), the fourth element (20), and the second element (10). This results in the list [10, 20, 10], which still contains duplicates.

Incorrect. The code segment will iterate over myList from right to left, removing the all elements but the first. This results in the list [50], which contains no duplicates, as intended.

69 Mine BC Correct AD

Correct. The location and date that a photo is taken is considered metadata about the image. This information can be used to determine whether two pictures were taken at the same location on different dates.

Correct. The time and date that a photo is taken is considered metadata about the image. This information can be used to determine the chronological order of the images.


55: Mine: A Correct : D

Incorrect. This code segment assigns the value of the last element of the list to the variable temp, then removes the last element of the list, then appends temp to the end of the list. The resulting list is the same as the original list.

Correct. This code segment assigns the value of the last element of the list to the variable temp, then removes the last element of the list, then inserts temp as the first element of the list.

