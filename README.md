Download Link: https://assignmentchef.com/product/solved-pdp-assignment1-student-classroom-simulator
<br>
Please state the assessment criteria applied to this assignment, such as:

<ul>

 <li>Correctness of the work.</li>

 <li>Presentation, including compliance with the specified file format.</li>

 <li>Evidence of critical thinking and analysis.</li>

 <li>Originality, quality and thoroughness of the work.</li>

 <li>Research correct academic approach.</li>

 <li>Proper treatment of sources.</li>

</ul>

Upload the answer as java files ONLY.

<em>Academic Dishonesty: All of your assignments need to represent your own effort. Assignments should be done without consultation with other students and you should not share your source code with others. Any assignment submitted that is essentially the same, as someone else’s will not be accepted<strong>. ALL matching assignments will receive 0 credits.</strong> </em>

<strong>                 </strong>

Your task is to simulate of college and classrooms: There are four kinds of threads: students, visitors, monitor and a one Lecturer per classroom. students must wait to enter classroom if class is running, enter, and then sitDown. At some point, the Lecturer enters the classroom. When the Lecturer is in the classroom, no one may enter, and the students may not leave. visitors may leave. Once all students check in, the Lecturer can StartLecture. After some time, the Lecturer leaves and all students can leave.

To make these requirements more specific, let’s give the threads some functions to execute, and put constraints on those functions.

<ul>

 <li>students must invoke enter, sitDown, and leave.</li>

 <li>The Lecturer invokes enter, startLecture and leave.</li>

 <li>visitors invoke enter, sitDown and leave.</li>

 <li>While the Lecturer is in the classroom, no one may enter and students may not leave.</li>

 <li><u>The Lecturer cannot startLecture until all students who have entered have also sitDown.</u></li>

 <li>At any point of time any classroom may have only one lecturer.</li>

 <li>Classroom capacity should not exceed limit. Visitors are always low in count (less than 5).</li>

 <li>Add a monitor thread to keep printing the status of each class as follows</li>

</ul>

Simulate a college with few classrooms

{W201 (capacity 60), W202(capacity 60), W101 (Capacity 20), JS101 Capacity (30)} and lecturers {Osama, Barry, Faheem, Alex, Aqeel, Waseem} that circulate between classes.

Hints: Lecturer can use a binary semaphore to access classroom so one lecturer in class at any time students and visitors can use counted semaphores to access classroom. You can use locks, barriers, semaphores.

<strong>The running of the program should show something like the table below, that is updating every 2 seconds </strong>

==================================================================================

Classroom           Lecturer               InSession             Students              Visitors

==================================================================================

W201                    Osama                   True                      50                           3

W202                    Alex                      True                        55                          1

JS101                    Faheem                True                        15                          0

W101                     False                    False

W201                    Waseem              True                       54                          5

W202                    Aqeel                    True                       43                          2

W101                     Osama                 True                       18                          1

JS101                    Barry                     True                        25                          2 <strong> </strong>