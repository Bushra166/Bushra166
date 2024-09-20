class Student:
    def __init__(self, rollno, name, age, gender):
        self.rollno = rollno
        self.name = name
        self.age = age
        self.gender = gender

    def display(self):
        print(f"Roll No: {self.rollno}")
        print(f"Name: {self.name}")
        print(f"Age: {self.age}")
        print(f"Gender: {self.gender}")


class Test(Student):
    def __init__(self, rollno, name, age, gender, marks1, marks2, marks3):
        super().__init__(rollno, name, age, gender)
        self.marks1 = marks1
        self.marks2 = marks2
        self.marks3 = marks3
        self.total_marks = marks1 + marks2 + marks3

    def display(self):
        super().display()
        print(f"Marks 1: {self.marks1}")
        print(f"Marks 2: {self.marks2}")
        print(f"Marks 3: {self.marks3}")
        print(f"Total Marks: {self.total_marks}")


def main():
    n = int(input("Enter the number of students: "))

    students = []

    for i in range(n):
        rollno = input(f"Enter roll no of student {i+1}: ")
        name = input(f"Enter name of student {i+1}: ")
        age = int(input(f"Enter age of student {i+1}: "))
        gender = input(f"Enter gender of student {i+1}: ")
        marks1 = int(input(f"Enter marks 1 of student {i+1}: "))
        marks2 = int(input(f"Enter marks 2 of student {i+1}: "))
        marks3 = int(input(f"Enter marks 3 of student {i+1}: "))

        student = Test(rollno, name, age, gender, marks1, marks2, marks3)
        students.append(student)

    print("\nStudent Details:")

    for i, student in enumerate(students):
        print(f"\nStudent {i+1}:")
        student.display()


if __name__ == "__main__":
    main()
