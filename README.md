Download Link: https://assignmentchef.com/product/solved-cpt121-assignment-1-part-c-booking-system-for-moolort-heritage-railway
<br>
<strong>This assessment requires you to apply various concepts and techniques covered in weeks 1-4 of the course, in order </strong><strong>to assemble a programmatic solution for a problem based on a simulated real-world scenario.</strong>

<strong>An important part of your development as a programmer is the ability to identify and apply appropriate techniques </strong><strong>or programming structures when implementing the various aspects of a programmatic solution to a given problem, </strong><strong>so in addition to the basic functional requirements of this task, you will also be assessed on your ability to select and utilise appropriate techniques and structures in your solution.</strong>

<strong>This assessment requires you to design and create a Java program to solve analysed stakeholder (user and </strong><strong>supervisor) requirements.</strong>

<strong>Course learning outcomes</strong>

<strong>This assessment is relevant to the following course learning outcomes:</strong>

<ul>

 <li><strong>CLO 1: Solve simple algorithmic computing problems using basic control structures and Object-Oriented </strong><strong>Techniques</strong></li>

 <li><strong>CLO 2: Design and implement computer programs based on analysing and modelling requirements</strong></li>

 <li><strong>CLO 3: Identify and apply basic features of an Object-Oriented programming language through the use of </strong><strong>standard Java (Java SE) language constructs and APIs</strong></li>

 <li><strong>CLO 4: Identify and apply good programming style based on established standards, practices and coding </strong><strong>guidelines</strong></li>

 <li><strong>CLO 5: Devise and apply strategies to test the developed software</strong></li>

</ul>

<strong>Assessment details</strong>

<strong>Your task is to produce, using standard Java (Java SE), a prototype computerised booking system for </strong><strong>‘Moolort Heritage Railway’. This (fictional) volunteer railway runs a monthly tourist steam-train service </strong><strong>between the north-central Victorian stations of Castlemaine and Moolort.</strong>

<strong>Interviews with two Moolort Heritage Railway volunteers are given below: Robert, a Ticket Officer and </strong><strong>Clem, the Railway Manager. You should analyse the interviews to determine the functional requirements for your program. Your supervisor has provided further requirements. These requirements are set out in the three stages </strong><strong><em>(A, B </em></strong><strong>and </strong><strong><em>C) </em></strong><strong>below. Since each stage elaborates on the previous one, you only need to </strong><strong>submit one program — the one implementing the highest stage you were able to complete.</strong>

<strong>The functionality of each stage will be tested on test-case described in </strong><strong><em>TestCases.pdf, </em></strong><strong>which can be found </strong><strong>on the course Canvas under the </strong><strong><em>Assignment 1 </em></strong><strong>link.</strong>

<strong>For each of the stages A, B and C, complete the steps below based on the Double Diamond process: </strong><strong>Discover</strong>

<strong>‘Go wide’ in the form of reading and thinking about the supplied stakeholder requirements. Find out what </strong><strong>the current situation is and understand user behaviours and business drivers.</strong>

<strong>Fill in the supplied ‘Discover and Define’ Word template with a list of different problems that could be </strong><strong>solved.</strong>

<strong>Define</strong>

<strong>From your understanding of the overall issues/requirements, narrow down to a single problem and turn that </strong><strong>into a problem statement. The problem statement defines what you will develop, and you may start some </strong><strong>initial coding to start working out if you can create a solution to the problem you defined.</strong>

<strong>Fill in the supplied ‘Discover and Define’ Word template with a statement of the single problem you will </strong><strong>solve.</strong>

<strong>Develop</strong>

<strong>Start coding to create an initial prototype and program logic to address the problem. You may create a few </strong><strong>different iterations to get to the best prototype. This is a phase for trying ideas out to see if they work.</strong>

<strong>Deliver</strong>

<strong>Pick the best prototype from the ‘Develop’ phase and create the final version of the code, refining and </strong><strong>making it work. The aim is to create a minimum viable product (MVP) to address the problem you have </strong><strong>identified and defined. The final result of this process at stage C will become your final submission for </strong><strong>assessment 1.</strong>

<strong>How to use the Double Diamond will be explained in the course webinar, please ask your instructor if you </strong><strong>have any questions.</strong>







<strong>The assessment is marked out of a total of 10 marks as given in the rubric criteria table at the end of this document.</strong>

<strong>Coding Style/Documentation</strong>

<strong>Your program must follow the coding and documentation style guide given in the file <em>StyleGuide.pdf, </em></strong><strong>available on the course Canvas under the <em>Assignment 1 </em>link.</strong>

<strong>Stage A </strong><strong>– </strong><strong>Basic Journey Booking System for Castlemaine</strong><strong>–</strong><strong>Moolort return trips</strong>

<strong>Your task here is to discover and define the problem and then develop a console-driven Java program which </strong><strong>implements the functional requirements derived from the interviews and instructions given below.</strong>

<strong>Clem — Railway Manager</strong>

<strong><em>“Our volunteers run a once monthly tourist service running from Castlemaine to Moolort which then, </em></strong><strong><em>after a 2-hour stopover, returns to Castlemaine. Our train has three carriages: a ‘First’ class, a second</em></strong>

<strong><em>or ‘Standard’ class, and a third class called ‘Excursion’ class, with seating for 48, 70 and 95 </em></strong><strong><em>passengers, respectively.</em></strong>

<strong><em>Initially we’d like a prototype for producing a Booking Receipt, as this currently has to be filled out by </em></strong><strong><em>hand by our ticketing officers, which is time-consuming and error-prone. We’d also like to be able to track and display the number of seats available as sometimes we accidently over-book.”</em></strong>

<strong>Robert — Ticket Officer</strong>

<strong><em>“We start selling tickets for the next service as soon as the current service has returned to </em></strong><strong><em>Castlemaine. We can have bookings for multiple seats, as long as they are all for the same class. First </em></strong><strong><em>class is adults only, as we have a bar service there, and those passengers also appreciate some quiet. </em></strong><strong><em>Standard and Excursion class, however, can have children too.</em></strong>

<strong><em>So, the ticket prices for First class are $80 per seat. For Standard class, its $55 for an adult and $30 for </em></strong><strong><em>each child and for Excursion class, an adult ticket costs $40 and $20 for each child. Oh, I should </em></strong><strong><em>mention that children under three travel for free. That can cause a problem if we forget to ask the </em></strong><strong><em>customer how old the child is, and issue the wrong ticket. Or even worse, the passenger might not tell us they’ve got a young child, since they travel for free — but we’ve still got to allocate a seat for them!</em></strong>

<strong><em>Sometimes customers ask us how many seats are available for each class before they make a </em></strong><strong><em>booking. Our Promotions Officer, Abe, sometimes wants to know availability information too. We </em></strong><strong><em>have to be careful when accepting any booking to ensure we have enough seats available, so it’d be </em></strong><strong><em>nice if that check could be automated.</em></strong>

<strong><em>Once the booking has been made, we write out a booking receipt listing what class the booking is for, </em></strong><strong><em>the number of each type of seat, the cost of the seat type and the total price for the booked seats of that seat type. Then we include the booking total.</em></strong>

<strong><em>We basically keep repeating some or all of these tasks until it is quitting time!”</em></strong>

<strong>Your supervisor advises that your program should prompt the user to enter the required information in a </strong><strong>user-friendly manner, read those values in from the console and store the corresponding values in variables </strong><strong>of appropriate types. Displayed output should be neatly tabulated. For example, the booking seat quantities, seat-type prices and booked seat-type total prices of a booking should be aligned into respective columns,</strong><strong>with the booking total aligning with the seat-type total </strong><strong>prices.</strong>

<strong>You program for this stage should be implemented as a single class. You will have the opportunity to </strong><strong>implement an Object-Oriented design in stage <em>C.</em></strong>

<strong>Stage B </strong><strong>– </strong><strong>Booking System for a service stopping all stations</strong>

<strong>Your task here is to extend your console-driven Java program to implement the functional requirements </strong><strong>derived from the interviews and instructions given below.</strong>

<strong>Clem — Railway Manager</strong>

<strong><em>“Our service has been generally under-utilised and so we’ve decided to change it from one that was </em></strong><strong><em>express between Castlemaine and Moolort to one that stops all stations. Our stations are, in order: </em></strong><strong><em>Castlemaine, Campbell, Guildford, Strangway, Newstead and Moolort. We’d like your booking </em></strong><strong><em>system to be able to handle passengers boarding/alighting at any station. The service will still be a </em></strong><strong><em>return one, and on the return trip, we would only pick passengers up from the station they alighted</em></strong>

<strong><em>at earlier and return them to their initial starting point, so the receipt should indicate the </em></strong><strong><em>passenger’s initial boarding point, and their outward bound destination point. Our pricing structure </em></strong><strong><em>has changed to reflect that passenger journeys can be shorter under this new system and we hope </em></strong><strong><em>this will attract new patronage to offset the possible reduced revenue of shorter trips.</em></strong>

<strong><em>We’ve also decided to implement a group discount of ten percent off bookings with ten or more paying passengers and would like your system to automatically handle that and report the cost </em></strong><strong><em>saving on the booking receipt.”</em></strong>

<strong>Robert — Ticket Officer</strong>

<strong><em>“There’s now a booking fee of $5 per paying passenger. But as there are five stops on our line, management decided the cost per station would be of the previous seat cost. So, for example, a </em></strong><strong><em>single return First class adult seat from Guildford to Strangway is now $16 plus a $5 booking fee. If </em></strong><strong><em>they went from Guildford to Newstead return, that would be a total of $37. Quite a bargain, if you ask me. We don’t want to have to type out the relevant station names each time we sell a ticket. </em></strong><strong><em>Just entering a numeric code, such as 0 for Castlemaine and 5 for Moolort would be good enough, </em></strong><strong><em>as long as we were given the numbers in the prompt.”</em></strong>

<strong>Your supervisor advises that your program must utilise arrays of primitive data type for storing how many </strong><strong>seats are available for travelling to each stop. An array of String should also be used for storing railway </strong><strong>station names.</strong>

<strong>You program for this stage should be implemented as a single class. You will have the opportunity to </strong><strong>implement an Object-Oriented design in stage <em>C.</em></strong>




<strong><em>0</em></strong><strong> RMIT</strong>

<strong>UNIVERSITY</strong>

<strong>Stage C — Object-Oriented implementation of the Booking System for a service stopping all </strong><strong>stations</strong>

<strong>Your supervisor advises that you should remodel your stage B Java program to use three classes in order to </strong><strong>provide the functionality specified in stage B.</strong>

<ul>

 <li><strong>Class <em>TrainService </em>stores and manipulates information relevant to the train journey such as what </strong><strong>stations comprise the journey and how many of each seat type are available throughout the journey. </strong><strong>Arrays should still be used by the class to store this information.</strong></li>

 <li><strong>Class <em>BookingReceipt </em>implements methods relevant to calculating and printing out a booking </strong><strong>receipt, formatted as specified in stages A &amp; B.</strong></li>

 <li><strong>Class <em>BookingSystem </em>implements the <em>main </em> It collects user information and uses the </strong><strong><em>TrainService </em></strong><strong>and <em>BookingReceipt </em>classes to implement the functionality of stage B.</strong></li>

</ul>

<strong>For the purposes of this stage, <em>Object-Oriented technique </em>involves satisfying all the following criteria:</strong>

<ul>

 <li><strong>Appropriate choice of classes and methods as per good Object-Oriented programming practice</strong></li>

 <li><strong>Appropriate private instance variables and/or constants defined for all required values</strong></li>

 <li><strong>Variables required only within a method are defined locally</strong></li>

 <li><strong>Visibility of instance variables set to private as per good Object-Oriented programming practice</strong></li>

</ul>