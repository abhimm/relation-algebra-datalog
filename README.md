Problem Set
===========
IMPLEMENT the following queries in a Datalog Database System called XSB. See XSB Instructions, input tables (i.e., the facts), and submission instructions. Please direct any queries related to XSB to the Class-TA. 

- Let us consider the following relations/predicates:
        Courses(number, quarter)
        Prereqs(course, prerequisite)
        Enrolls(studentID, course, quarter, grade)
    Note that courses are represented by their unique numbers in relations Prereqs and Enrolls; students are represented by their ID's. Prerequisites are immediate prerequisites only. For example, if CS101 is a prerequisite of CS200, and CS200 is a prerequisite of CS342, then only the pairs (CS200, CS101) and (CS342, CS200) would appear in Prereqs. We refer to CS101 as an indirect prerequisite of CS342. Write the following questions in Datalog:
        Find the prerequisites, including indirect prerequisites, of each course.
        A prerequisite is considered satisfied only if the students gets an A or A- grade in the course. Find all (student, course, quarter) pairs (x,y,q) such that x enrolls in y in quarter q but did not satisfy (i.e., didn't enrol or enrolled but got a B+ or lower grade) one or more of y's prerequisites in a prior quarter.


- Consider a database for the Paris Metro and Bus lines, consisting of two relations Metro(Station, Next) and Bus(Station, Next).
        Find pairs of stations (m,n), such that n can be reached from m only if both buses and metros are available (i.e., each path from m to n must require a bus as well as a metro).
        We say that the metro is useful in a bus-path from m to n if for all intermediate points k one can reach using a metro all subsequent intermediate stations (if any) along the path. Find the pair of stations (m,n) such that the metro is useful in all the bus paths connecting m and n. Read Slide #19 of Quantifiers.

