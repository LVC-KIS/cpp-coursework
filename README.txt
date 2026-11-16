STUDENT RESULTS REGISTER
BCS 2204 - DATA STRUCTURES AND ALGORITHMS
Scenario 6: Student Results Register

Student: Kisige Elvis
Registration Number: VU-BCS-2507-0971

1. PROJECT DESCRIPTION
This is a C++17 console application that manages student result records using a
templated dynamic array. The dynamic array increases its capacity by doubling
when more space is required.

Each student record contains:
- Student ID
- Student name
- Course
- Score

The program loads student records from students.txt, sorts and searches the
records, saves the updated records to students_out.txt, and runs a timing
comparison between insertion sort and randomised-pivot quicksort.

2. FILES
The project folder should contain:

StudentResultsRegister.cpp
students.txt
README.txt

When the coursework source is reorganised to meet the requirement for the
dynamic-array class template in a header file, the header file (for example,
DynamicArray.h) should also be included in the project folder and ZIP file.

3. REQUIREMENTS
- A C++ compiler that supports C++17 (for example, g++).
- A terminal such as the Ubuntu terminal in WSL.
- The input file students.txt in the same working directory as the executable.

4. INPUT FILE FORMAT
The program reads comma-separated records from students.txt.
Each line must contain four fields in this order:

student_id,name,course,score

Example:
1001,John,MATHEMATICS,85
1002,Mary,COMPUTER SCIENCE,75
1003,Peter,INFORMATION TECHNOLOGY,68

Do not add a heading row. Use at least 10 valid records for the coursework.
Avoid commas inside names or course names because commas separate the fields.

5. HOW TO COMPILE
Open a terminal in the project directory and run:

g++ -std=c++17 -Wall -Wextra StudentResultsRegister.cpp -o register

6. HOW TO RUN
Run the following command from the same directory:

./register

The program expects students.txt to be in the current working directory.
It displays the loaded records, sorts them by score using insertion sort,
searches for scores 75 and 999, applies the registration-number-based
O(n log n) sorting algorithm, saves the records, and performs the timing
experiment.

The final digit of registration number 25070971 is 1 (odd), so the selected
O(n log n) algorithm is randomised-pivot quicksort.

7. OUTPUT FILE
After a successful run, the program writes the updated records to:

students_out.txt

The output file contains comma-separated student records in the order
produced by the selected sorting operation.

8. MEMORY-SAFETY BUILD (ADDRESSSANITIZER)
To compile with AddressSanitizer, run:

g++ -std=c++17 -Wall -Wextra -g -fsanitize=address StudentResultsRegister.cpp -o register_asan

Then run:

./register_asan

If AddressSanitizer reports an error, investigate and correct it before
claiming that the program passed the memory-safety check. A successful
ordinary run alone does not prove that AddressSanitizer passed.

9. TIMING EXPERIMENT
The program compares insertion sort with the selected O(n log n) algorithm
for input sizes of 1,000, 2,000, 4,000, 8,000, 16,000, 32,000 and 64,000.
Each size is tested three times, and the average execution time is displayed.
The timing values depend on the computer and system conditions.

10. NOTES
- Run the program from the project directory so that students.txt can be found.
- Keep a backup of students.txt before testing if you do not want to risk
  changing or replacing input data.
- The program creates or overwrites students_out.txt when it saves results.
- The source file and input data should be included in the coursework ZIP.
- Ensure the final submission also includes the required header file,
  source file(s), report, public GitHub repository link and AI Use Declaration.
