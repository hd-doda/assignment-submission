Assignment: MERN Stack Application with Firebase 
Authentication and Role-Based Redirect 
Objective: The task is to build a simple MERN stack application that integrates with 
Firebase for user authentication. The application should include role-based access 
(Instructor and Student), where the role is stored both in Firebase and MongoDB. 
Based on the user's role, they should be redirected to different dashboards. 
Requirements: 
1. Firebase Authentication: 
o Implement Firebase Authentication in the application for user login. 
o After login, retrieve the user's role from Firebase, and store it in both 
Firebase and MongoDB. 
2. Role-Based Redirect: 
o Instructor: If the user's role is Instructor, redirect them to the 
Instructor Dashboard. 
o Student: If the user's role is Student, redirect them to the Student 
Dashboard. 
3. Instructor Dashboard: 
o The Instructor Dashboard should include a form where instructors 
can create Multiple Choice Questions (MCQs). 
o The form should include:  
 Question text 
 Multiple options for the question 
 The correct answer 
o When the instructor submits the form, the question should be saved to 
MongoDB. 
4. Student Dashboard: 
o The Student Dashboard should display the MCQs created by the 
instructor. 
o The student should be able to attempt the questions displayed on 
their dashboard. 
5. Frontend (React with Tailwind CSS): 
o Build the frontend using React. 
o Use Tailwind CSS for styling. 
6. Backend (Node.js with Express): 
o Set up a Node.js server using Express. 
o Implement the necessary APIs to handle:  
 Login and Authentication with Firebase. 
 Storing user roles in both Firebase and MongoDB. 
 Fetching and storing MCQs in MongoDB. 
7. Database (MongoDB): 
o Create the following collections:  
 Users: Store user data, including the role (instructor or student). 
 Questions: Store the multiple-choice questions created by the 
instructor. 
Steps to Complete: 
1. Set up Firebase Authentication: 
o Create a Firebase project and enable Email/Password 
authentication. 
o Integrate Firebase Authentication into the frontend to allow users to log 
in. 
2. Implement Role Management: 
o Once the user logs in, determine if the user is an Instructor or 
Student (you can add roles manually in Firebase or create a 
mechanism to assign them). 
o Save the role in both Firebase (Custom Claims) and MongoDB. 
3. Create Role-Based Redirects: 
o After login, check the user's role from Firebase and redirect them to the 
appropriate dashboard.  
 If the role is Instructor, redirect to /instructor-dashboard. 
 If the role is Student, redirect to /student-dashboard. 
4. Instructor Dashboard: 
o Create a form for the instructor to submit multiple-choice questions. 
o Use React Hook Forms or any form handling library for easy form 
management. 
o On form submission, store the question, options, and the correct 
answer in MongoDB. 
5. Student Dashboard: 
o Fetch the MCQs from MongoDB and display them for the student. 
o Allow the student to see the questions and optionally mark answers. 
6. Database Schema: 
o For Users:  
 email (string) 
 role (string: 'instructor' or 'student') 
 firebase_uid (string) 
o For Questions:  
 question_text (string) 
 options (array of strings) 
 correct_answer (string) 
Tech Stack: 
 Frontend: React, Tailwind CSS 
 Backend: Node.js, Express 
 Authentication: Firebase 
 Database: MongoDB
