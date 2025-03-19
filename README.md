[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/bM-dlu9L)
import java.util.*;
import java.util.stream.*;

class Student {
    String name;
    int marks;

    public Student(String name, int marks) {
        this.name = name;
        this.marks = marks;
    }

    public String getName() {
        return name;
    }

    public int getMarks() {
        return marks;
    }
}

public class StudentStreamExample {
    public static void main(String[] args) {
        // Creating a list of students
        List<Student> students = Arrays.asList(
                new Student("John", 80),
                new Student("Alice", 90),
                new Student("Bob", 60),
                new Student("David", 85),
                new Student("Eva", 70)
        );

        // Using lambda expressions and stream operations to filter, sort, and display student names
        students.stream()
                .filter(student -> student.getMarks() > 75)  // Filter students scoring above 75%
                .sorted(Comparator.comparingInt(Student::getMarks))  // Sort students by marks
                .forEach(student -> System.out.println(student.getName()));  // Display their names
    }
}

