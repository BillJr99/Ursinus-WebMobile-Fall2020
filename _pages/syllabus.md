---
layout: syllabus
permalink: /
title: "CS471: Special Topics: Web and Mobile Development"
excerpt: "CS471: Special Topics: Web and Mobile Development"

info:
  course_number: CS471
  course_sections: 
  - section: "A"
  course_title: "Web and Mobile Development"
  course_prerequisites: "CS174 Object Oriented Programming"
  course_start_date: "2020/09/07"
  course_end_date: "2020/12/15"
  course_description: "This course explores web service architectures through the lens of ubiquitous computing sensors and mobile devices.  Authentication models such as SAML and OAUTH will be used to integrate well-known web service interfaces.  Students will be able to expose services as well-defined GraphQL or RESTful service endpoints, and be able to utilize the endpoints of existing services.  Students will collaboratively propose, develop, and present projects with defined broader impacts."
  class_meets_days:
    isM: true
    isT: false
    isW: true
    isR: false
    isF: true 
    isS: false
    isU: false
  class_meets_locations:
  - section:
    - day: "M"
      starttime: "1:30 PM"
      endtime: "2:20 PM"
      place: "Pfahler Hall Room 001"
    - day: "W"
      starttime: "1:30 PM"
      endtime: "2:20 PM"
      place: "Pfahler Hall Room 001"
    - day: "F"
      starttime: "1:30 PM"
      endtime: "2:20 PM"
      place: "Pfahler Hall Room 001"      
  midtermexam: 
    - mdate: "TBD"
      mstarttime: "TBD"
      mendtime: "TBD"
      mroom: "TBD"
    - mdate: "TBD"
      mstarttime: "TBD"
      mendtime: "TBD"
      mroom: "TBD"      
  finalexam: 
    - fdate: "TBD"
      fstarttime: "TBD"
      fendtime: "TBD"
      froom: "TBD"
    - fdate: "TBD"
      fstarttime: "TBD"
      fendtime: "TBD"
      froom: "TBD"
   
instructors:
- name: William Mongan
  title: Professor
  email: billmongan@gmail.com
  phone: "Phone TBD"
  webpage_url: "http://www.billmongan.com"
  picture: /images/profile.png
  officehours:
  - day: "M"
    starttime: "10:00 AM"
    endtime: "10:50 AM"
    location: "TBD"
  - day: "M"
    starttime: "12:30 PM"
    endtime: "1:20 PM"
    location: "TBD"  
  - day: "M"
    starttime: "8:00 PM"
    endtime: "9:00 PM"
    location: "Virtual Office Hours on Microsoft Teams"      
  - day: "T"
    starttime: "10:00 AM"
    endtime: "10:50 AM"
    location: "TBD"
  - day: "T"
    starttime: "8:00 PM"
    endtime: "9:00 PM"
    location: "Virtual Office Hours on Microsoft Teams"     
  - day: "W"
    starttime: "10:00 AM"
    endtime: "10:50 AM"
    location: "TBD"    
  - day: "W"
    starttime: "12:30 PM"
    endtime: "1:20 PM"
    location: "TBD"    
  - day: "F"
    starttime: "10:00 AM"
    endtime: "10:50 AM"
    location: "TBD"     
  - day: "F"
    starttime: "12:30 PM"
    endtime: "1:20 PM"
    location: "Networking Office Hours"    
  
textbooks:
- title: "RESTful Web Services"
  authors: "Leonard Richardson and Sam Ruby"
  edition: "First Edition"
  isbn: "978-0-596-52926-0"
  link: https://www.crummy.com/writing/RESTful-Web-Services/
  image: https://www.crummy.com/writing/RESTful-Web-Services/cover-thumb.png
  isrequired: true  
- title: "RESTful Java with JAX-RS 2.0"
  authors: "Bill Burke"
  edition: "First Edition"
  isbn: "978-1449361341"
  link: https://www.amazon.com/gp/product/144936134X
  image: http://images.amazon.com/images/P/144936134X.01._PI_SCMZZZZZZZ_.jpg
  isrequired: true   

objectives:
- objective: "Design a web-servces architecture that incorporates and generalizes a variety of stakeholder needs, exposed via a well-defined interface of data and functionality."
- objective: "Implement a robust web-service software system server and client that is tolerant of variations in user input and adherent to defined output standards."
- objective: "Implement an appropriate authentication model using standards such as SAML and OAUTH"
- objective: "To design and implement a web-based front-end software system that promotes accessibility and usability by a variety of stakeholders."

goals:
- goal: "Develop web-enabled software that integrates a variety of data sources in a way that enables new functionality greater than the sum of its parts."

grade_breakdown:
- category: "Programming Assignments"
  weight: "50%"
- category: "Labs"
  weight: "25%"
- category: "Final Project"
  weight: "20%"
- category: "Class Participation"
  weight: "5%"

letter_grades:
- letter: "A+"
  range: "96.9-100"
- letter: "A"
  range: "93-96.89"
- letter: "A-"
  range: "89.5-92.99"
- letter: "B+"
  range: "87-89.49"
- letter: "B"
  range: "83-86.99"
- letter: "B-"
  range: "79.5-82.99"
- letter: "C+"
  range: "77-79.49"
- letter: "C"
  range: "73-76.99"
- letter: "C-"
  range: "69.5-72.99"
- letter: "D+"
  range: "69-69.49"
- letter: "D"
  range: "63-66.99"
- letter: "D-"
  range: "59.5-62.99"
- letter: "F"
  range: "59.49 and below" 

schedule:
- week: "0"
  date: "0"
  title: "Course Sneak Preview"
  link: "http://www.billmongan.com"
  deliverables:
  - dtitle: "Lab 0: Warmup Handed Out"
    dlink: "http://www.billmongan.com"
- week: "0"
  date: "1"
  title: "Web Services"
- week: "1"
  date: "0"
  title: "Web Service Design"
- week: "2"
  date: "0"
  title: "GraphQL"
- week: "3"
  date: "0"
  title: "RESTful Web Services"
- week: "4"
  date: "0"
  title: "Interacting with Existing Services through Web Service Clients"
- week: "5"
  date: "0"
  title: "Authentication Models"
- week: "5"
  date: "1"
  title: "Digital Certificates through Public Key Cryptosystems"  
- week: "5"
  date: "2"
  title: "The Peruvian Coin Flip"    
- week: "6"
  date: "0"
  title: "SAML"
- week: "6"
  date: "1"
  title: "OAuth"
  readings:
  - rtitle: "OAuth 2.0 Simplified"
    rlink: "https://aaronparecki.com/oauth-2-simplified/#roles"   
- week: "7"
  date: "0"
  title: "Creating Your Own Web Services"
- week: "8"
  date: "0"
  title: "Databases"
- week: "8"
  date: "2"
  title: "NoSQL"  
- week: "9"
  date: "0"
  title: "Server-Side Authenticaiton Models"  
- week: "10"
  date: "0"
  title: "Mobile Application Development"    
- week: "10"
  date: "1"
  title: "HTML5 and Front End and Mobile Development"  
- week: "10"
  date: "2"
  title: "CSS"  
- week: "11"
  date: "0"
  title: "jQuery"  
- week: "12"
  date: "0"
  title: "Angular Framework for Cross Platform Development"  
- week: "13"
  date: "0"
  title: "Open-Source Software Development"  
- week: "14"
  date: "0"
  title: "Workshopping"
  
university:
  semester: "Fall"
  academicyear: "2020-21"
  fall:
  - kname: "Convocation"
    kdate: "2020/08/28"
    kdisplay: true
  - kname: "Add Deadline"
    kdate: "2020/09/11"
    kdisplay: true
  - kname: "Drop with a W Deadline"
    kdate: "2020/10/28"
    kdisplay: true  
  - kname: "Mid Semester Grades Posted"
    kdate: "2020/10/16"
    kdisplay: false
  - kname: "2020 Transition to Remote Learning after Thanksgiving Break"
    kdate: "2020/11/30"
    kdisplay: true
  - kname: "Finals Week Begins"
    kdate: "2020/12/16"
    kdisplay: false
  - kname: "Finals Week Ends"
    kdate: "2020/12/22"
    kdisplay: false
  spring:
  - kname: "Reading Day"
    kdate: "2021/05/6"
    kdisplay: true
  - kname: "Add Deadline"
    kdate: "2021/02/2"
    kdisplay: true
  - kname: "Drop with a W Deadline"
    kdate: "2021/03/24"
    kdisplay: true
  - kname: "Mid Semester Grades Posted"
    kdate: "2021/03/5"
    kdisplay: false
  - kname: "Baccalaureate"
    kdate: "2021/05/14"
    kdisplay: false
  - kname: "Commencement"
    kdate: "2021/05/15"
    kdisplay: false
  - kname: "Finals Week Begins"
    kdate: "2021/05/07"
    kdisplay: false
  - kname: "Finals Week Ends"
    kdate: "2021/05/13"
    kdisplay: false    
  fallholidays:
  - date: "2020/10/19"
  - date: "2020/10/20"
  - date: "2020/11/25"
  - date: "2020/11/26"
  - date: "2020/11/27" 
  springholidays:
  - date: "2021/03/08"  
  - date: "2021/03/09"
  - date: "2021/03/10"
  - date: "2021/03/11"
  - date: "2021/03/12"
    
---
Welcome!