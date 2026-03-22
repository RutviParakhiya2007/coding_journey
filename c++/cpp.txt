                                                                c++

#_Libraries :-

    library/header | Purpose/use
    ---------------+-------------
    <iostream>     | Input & Output
    <ifstream>     | open file for read
    <ofstream>     | open file for write
    <fstream>      | open file for read & write      
    <vector>       | Dynamic array (vector)


#_Baisic Skeleton of cpp :-

    #include <iostream>  // 1. Preprocessor Directive
    using namespace std; // 2. Namespace Declaration
                         // 3. Function Definition
    int main() {
        cout << "Hello, World!" << endl; // 4. Statement
        return 0; // 5. Return Statement
    }

#file_handling :-
1. create a file and write and close the file (ofstream)
-> [https://github.com/RutviParakhiya2007/CGxSU_Semester_1/blob/main/cpp_language(sem_02)/21.file_handling_in_cpp.md#writing-data-to-a-file]

2. Reading data from a file into terminal if it not existing then throw Error (ifstream)
-> [https://github.com/RutviParakhiya2007/CGxSU_Semester_1/blob/main/cpp_language(sem_02)/21.file_handling_in_cpp.md#reading-data-from-a-file]

3. read the file for particular character at the file if file is not existing throw error in terminal (fstream)
-> [https://github.com/RutviParakhiya2007/CGxSU_Semester_1/blob/main/cpp_language(sem_02)/21.file_handling_in_cpp.md#example-random-access-read]

4. Binary files
    (i) write to a binary file (ofstream(..., ios::binary))
    -> [https://github.com/RutviParakhiya2007/CGxSU_Semester_1/blob/main/cpp_language(sem_02)/21.file_handling_in_cpp.   md#writing-to-a-binary-file]
    (ii) read to a binary file (ifstream(..., ios::binary))
    -> [https://github.com/RutviParakhiya2007/CGxSU_Semester_1/blob/main/cpp_language(sem_02)/21.file_handling_in_cpp.md#reading-from-a-binary-file]

5. error handling in file operations if(!file) cout << 
-> [https://github.com/RutviParakhiya2007/CGxSU_Semester_1/blob/main/cpp_language(sem_02)/21.file_handling_in_cpp.md#5-error-handling-in-file-operations]

#_STL :-
STL Container is a ready-made data structure in C++ used to store and manage multiple values easily and efficiently.
-> There are three types of stl - 1. container, 2. itrator, 3. algorithem                

      





