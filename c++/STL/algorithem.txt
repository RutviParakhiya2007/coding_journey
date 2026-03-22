#_Algorithms_#
there are 7 types of algorithems

1. Non-modifying algorithems:-
    (i) find() - it searches through a sequence and returns the position (or reference) of the first element that matches a   
                 given value. [https://github.com/RutviParakhiya2007/CGxSU_Semester_1/blob/main/cpp_language(sem_02)/24.stl_algorithms.md#1-find---searching-for-an-element]

    (ii) count() - it is a non-modifying algorithm used to count how many times a specific value appears in a given range        
                   of elements.    
                   e.g. -   #include <iostream>
                            #include <algorithm>
                            using namespace std;
                            int main() {
                                int arr[] = {1, 1, 2, 3, 1};
                                int total = count(arr, arr + 5, 1);
                                cout << total;
                            return 0;    
                            }

    (iii) equal() - it is a non-modifying algorithm used to compare two sequences of elements. 
                    [https://github.com/RutviParakhiya2007/CGxSU_Semester_1/blob/main/cpp_language(sem_02)/24.stl_algorithms.md#14-equal---checking-equality-between-two-ranges]              

2. Modifying algorithems:-
    (i) sort() - it sorts the elements of a container in ascending order by default.
                 [https://github.com/RutviParakhiya2007/CGxSU_Semester_1/blob/main/cpp_language(sem_02)/24.stl_algorithms.md#2-sort---sorting-elements]

    (ii) reverse() - it reverses the order of elements in a container. 
                     [https://github.com/RutviParakhiya2007/CGxSU_Semester_1/blob/main/cpp_language(sem_02)/24.stl_algorithms.md#3-reverse---reversing-the-container] 

    (iii) transform() - it is converting data or a problem from one form into another form so it can be solved more easily.
                        [https://github.com/RutviParakhiya2007/CGxSU_Semester_1/blob/main/cpp_language(sem_02)/24.stl_algorithms.md#13-transform---modifying-elements-using-a-unary-function]

3. Sorting algorithems:-
    (i) sort() - it means to arrange items in a specific order, such as ascending or descending.
                 [https://github.com/RutviParakhiya2007/CGxSU_Semester_1/blob/main/cpp_language(sem_02)/24.stl_algorithms.md#2-sort---sorting-elements]

    (ii) stable_sort() - it keeps the original order of equal elements the same after sorting.  
                         e.g. - #include <iostream>
                                #include <algorithm>
                                using namespace std;
                                struct Student {
                                    string name;
                                    int marks;
                                };
                                int main() {
                                    Student s[] = {{"A", 90}, {"B", 80}, {"C", 90}, {"D", 70}};
                                    int n = 4;
                                    stable_sort(s, s + n, [](Student a, Student b) {
                                    return a.marks < b.marks;
                                    });
                                    for(int i = 0; i < n; i++) {
                                        cout << s[i].name << " " << s[i].marks << endl;
                                    }
                                return 0;
                                }       

    (iii) partialsort() - it is a sorting process where only a part of the data is sorted not the entire list.
                          [https://github.com/RutviParakhiya2007/CGxSU_Semester_1/blob/main/cpp_language(sem_02)/24.stl_algorithms.md#7-partial_sort---partially-sorting-a-container]

4. Searching algorithems:-
    (i) find() - It is a function used to search for a specific value in a collection of data.
                 [https://github.com/RutviParakhiya2007/CGxSU_Semester_1/blob/main/cpp_language(sem_02)/24.stl_algorithms.md#1-find---searching-for-an-element]

    (ii) binary-search() - it is a algorithm that finds an element in a sorted list by repeatedly dividing the list into 2 halves.
                           [https://github.com/RutviParakhiya2007/CGxSU_Semester_1/blob/main/cpp_language(sem_02)/24.stl_algorithms.md#5-binary_search---searching-for-an-element-in-a-sorted-range]

    (iii) lower_bound() - It is a function used on a sorted list to find the first element that is greater than or equal to given value.    e.g. -    #include <iostream>
                        #include <algorithm>
                        using namespace std;
                        int main() {
                            int arr[] = {10, 20, 30, 40, 50};
                            int n = 5;
                            int* ptr = lower_bound(arr, arr + n, 30);
                            cout << "Position: " << (ptr - arr) << endl;
                            cout << "Value: " << *ptr << endl;
                        return 0;
                        } 

5. Numeric algorithems:-

    (i) accumulate() - It is a function used to calculate the sum of elements in a range of values (like an array or list).
    [https://github.com/RutviParakhiya2007/CGxSU_Semester_1/blob/main/cpp_language(sem_02)/24.stl_algorithms.md#4-accumulate---summing-elements]

    (ii) inner_product() - It is a function that multiplies corresponding elements of two ranges and adds the results together.
        e.g. -  #include <iostream>
                #include <numeric>
                using namespace std;
                int main() {
                    int a[] = {1, 2, 3};
                    int b[] = {4, 5, 6};
                    int result = inner_product(a, a + 3, b, 0);
                    cout << "Result: " << result << endl;
                return 0;
                }

    (iii) partial_sum() - It is a function that calculates the cumulative sums of elements in a range.
        e.g. -  #include <iostream>
                #include <numeric>
                using namespace std;
                int main() {
                    int arr[] = {1, 2, 3, 4};
                    int result[4];
                    partial_sum(arr, arr + 4, result);
                    for(int i = 0; i < 4; i++) {
                        cout << result[i] << " ";
                    }
                return 0;
                }     

6. Heap-operations:-
                                            #_Max-heap :-
                                            1. Parent ≥ Children            
                                            2. Largest element top (root) ma hoy

                                            #_Min-heap :-
                                            1. Parent ≤ Children
                                            2. Smallest element top (root) ma hoy                           

    (i) make_heap() - It is a function that converts a range of elements into a heap.
                      [https://github.com/RutviParakhiya2007/CGxSU_Semester_1/blob/main/cpp_language(sem_02)/24.stl_algorithms.md#8-make_heap---creating-a-heap]

    (ii) push_heap() - it is a function that adds a new element to an existing heap and rearranges the elements to maintain the heap property. [https://github.com/RutviParakhiya2007/CGxSU_Semester_1/blob/main/cpp_language(sem_02)/24.stl_algorithms.md#10-push_heap---inserting-an-element-into-a-heap]

    (iii) pop_heap() - it is a function that removes the top element (largest in a max-heap) from a heap and rearranges the remaining elements to maintain the heap property.                                                           
    [https://github.com/RutviParakhiya2007/CGxSU_Semester_1/blob/main/cpp_language(sem_02)/24.stl_algorithms.md#9-pop_heap---removing-the-root-element-from-a-heap]

7. Partitioning algorithms:-
    
    (i) partition() - it is a function that rearranges elements in a range so that elements satisfying a given condition come before the others. 
        e.g. -  #include <iostream>
                #include <algorithm>
                #include <vector>
                using namespace std;
                int main() {
                    vector<int> v = {1, 4, 3, 6, 5, 2};
                    partition(v.begin(), v.end(), [](int n) {
                    return n % 2 == 0;   // even numbers first
                    });
                    for (int n : v)
                    {
                        cout << n << " ";
                    }
                return 0;
                }

    (ii) stable_partition() - It splits elements into two groups based on a condition, while keeping their original order the same. e.g. - #include <iostream>
                #include <algorithm>
                #include <vector>
                using namespace std;
                int main() {
                    vector<int> v = {5, 2, 4, 1};
                    stable_partition(v.begin(), v.end(), [](int n) {
                    return n % 2 == 0;   // even numbers first
                    });
                    for (int n : v)
                    {
                        cout << n << " ";
                    }
                return 0;
                }    
                        