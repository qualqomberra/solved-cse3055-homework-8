Download Link: https://assignmentchef.com/product/solved-cse3055-homework-8
<br>



<ul>

 <li>Consider the unnormalized relation R with six attributes ABCDEF and the following functional dependencies:</li>

</ul>

AB  à  CDE

<ul>

 <li>à F</li>

 <li>à D</li>

</ul>

<ol>

 <li> What is the key(s) for the relation?</li>

 <li> What is the normal form of this relation? Explain it.</li>

 <li> Decompose R into 3NF relations step by step if it is not in 3NF.</li>

</ol>

<ul>

 <li>Consider the following normalized relations from a database in a large retail chain:</li>

</ul>




<strong>STORE</strong> (StoreID, Region, ManagerID, SquareFeet)

<strong>EMPLOYEE</strong> (EmployeeID, WhereWork, EmployeeName, EmployeeAddress)

<strong>DEPARTMENT</strong> (DepartmentID, ManagerID, SalesGoal)

<strong>SCHEDULE</strong> (DepartmentID, EmployeeID, Date)




What opportunities might exist for denormalizing these relations when defining the physical records for this database? Under what circumstances would you consider creating such denormalized records?







<ul>

 <li>[14 pts] Consider the following two relations for Millennium College:</li>

</ul>




<strong>STUDENT</strong> (StudentID,  StudentName,  CampusAddress,  GPA)

<strong>REGISTRATION</strong> (StudentID,  CourseID,  Grade)




Following is a typical query against these relations:

SELECT  Student.StudentID,  StudentName,  CourseID,  Grade

FROM  Student,  Registration

WHERE  Student.StudentID = Registration.StudentID   AND   GPA &gt; 3.0 ORDER BY  StudentName;




<ol>

 <li> On what attributes should indexes be defined to speed up this query? Give the reasons for each attribute selected.</li>

 <li> Write SQL commands to create indexes for each attribute you identified in part a.</li>

</ol>

<ul>

 <li>You have a STUDENT table that has SID, Name, and Age columns. Which data pages are accessed to execute the queries below, under situations given at (a) and (b)? (Assume that index seek is used whenever possible)</li>

</ul>

<table width="221">

 <tbody>

  <tr>

   <td width="85"> </td>

   <td width="74"><strong>STUDENT </strong></td>

   <td width="62"> </td>

  </tr>

  <tr>

   <td width="85"><strong>SID </strong></td>

   <td width="74"><strong>Name </strong></td>

   <td width="62"><strong>Age </strong></td>

  </tr>

  <tr>

   <td width="85"> </td>

   <td width="74"> </td>

   <td width="62"> </td>

  </tr>

  <tr>

   <td width="85"> </td>

   <td width="74"> </td>

   <td width="62"> </td>

  </tr>

 </tbody>

</table>




<ol>

 <li>[18 pts] The table has a <em>clustered index</em> on <strong>SID</strong> column, and no other indexes. The index structure and data is stored on data pages as the following:</li>

</ol>

<table width="593">

 <tbody>

  <tr>

   <td width="29"> </td>

   <td width="108"><strong>Page 110 </strong></td>

   <td width="26"> </td>

   <td width="118"><strong>Page 120 </strong></td>

   <td width="26"> </td>

   <td width="126"><strong>Page 130 </strong></td>

   <td width="26"> </td>

   <td width="134"><strong>Page 140 </strong></td>

  </tr>

  <tr>

   <td width="29"><strong>01 </strong></td>

   <td width="108">1      Ayşe      2</td>

   <td width="26"><strong>01 </strong></td>

   <td width="118">4    Adem        4</td>

   <td width="26"><strong>01 </strong></td>

   <td width="126">7     Mert        8</td>

   <td width="26"><strong>01 </strong></td>

   <td width="134">10    Ceren     13</td>

  </tr>

  <tr>

   <td width="29"><strong>02 </strong></td>

   <td width="108">2     Fatma    7</td>

   <td width="26"><strong>02 </strong></td>

   <td width="118">5    Mehtap    4</td>

   <td width="26"><strong>02 </strong></td>

   <td width="126">8   Mehmet  10</td>

   <td width="26"><strong>02 </strong></td>

   <td width="134">11    Ali          16</td>

  </tr>

  <tr>

   <td width="29"><strong>03 </strong></td>

   <td width="108">3      Can      11</td>

   <td width="26"><strong>03 </strong></td>

   <td width="118">6    Ahmet      6</td>

   <td width="26"><strong>03 </strong></td>

   <td width="126">9    Zeynep    17</td>

   <td width="26"><strong>03 </strong></td>

   <td width="134">12    Yavuz     16</td>

  </tr>

 </tbody>

</table>










<ol>

 <li><strong>Query 1: </strong>select Name from STUDENT where SID &lt; 11</li>

</ol>




<ol>

 <li><strong>Query 2: </strong>select * from STUDENT where Age = 16</li>

</ol>




<ul>

 <li><strong>Query 3: </strong>select * from STUDENT where SID = 7</li>

</ul>

<ol>

 <li>The table has a <em>non-clustered index</em> on <strong>Age</strong> column, and no other indexes. The index structure and data is stored on data pages as the following:</li>

</ol>

<table width="593">

 <tbody>

  <tr>

   <td width="29"> </td>

   <td width="108"><strong>Page 220 </strong></td>

   <td width="26"> </td>

   <td width="132"><strong>Page 230 </strong></td>

   <td width="26"> </td>

   <td width="113"><strong>Page 240 </strong></td>

   <td width="26"> </td>

   <td width="134"><strong>Page 250 </strong></td>

  </tr>

  <tr>

   <td width="29"><strong>2 </strong></td>

   <td width="108">100:01</td>

   <td width="26"><strong>6 </strong></td>

   <td width="132">110:03</td>

   <td width="26"><strong>10 </strong></td>

   <td width="113">120:02</td>

   <td width="26"><strong>16 </strong></td>

   <td width="134">130:02</td>

  </tr>

  <tr>

   <td width="29"><strong>4 </strong></td>

   <td width="108">110:01</td>

   <td width="26"><strong>7 </strong></td>

   <td width="132">100:02</td>

   <td width="26"><strong>11 </strong></td>

   <td width="113">100:03</td>

   <td width="26"><strong>16 </strong></td>

   <td width="134">130:03</td>

  </tr>

  <tr>

   <td width="29"><strong>4 </strong></td>

   <td width="108">110:02</td>

   <td width="26"><strong>8 </strong></td>

   <td width="132">120:01</td>

   <td width="26"><strong>13 </strong></td>

   <td width="113">130:01</td>

   <td width="26"><strong>17 </strong></td>

   <td width="134">120:03</td>

  </tr>

 </tbody>

</table>










<table width="593">

 <tbody>

  <tr>

   <td width="29"> </td>

   <td width="108"><strong>Page 100 </strong></td>

   <td width="26"> </td>

   <td width="118"><strong>Page 110 </strong></td>

   <td width="26"> </td>

   <td width="126"><strong>Page 120 </strong></td>

   <td width="26"> </td>

   <td width="134"><strong>Page 130 </strong></td>

  </tr>

  <tr>

   <td width="29"><strong>01 </strong></td>

   <td width="108">1      Ayşe      2</td>

   <td width="26"><strong>01 </strong></td>

   <td width="118">4    Adem        4</td>

   <td width="26"><strong>01 </strong></td>

   <td width="126">7     Mert        8</td>

   <td width="26"><strong>01 </strong></td>

   <td width="134">10    Ceren     13</td>

  </tr>

  <tr>

   <td width="29"><strong>02 </strong></td>

   <td width="108">2     Fatma    7</td>

   <td width="26"><strong>02 </strong></td>

   <td width="118">5    Mehtap    4</td>

   <td width="26"><strong>02 </strong></td>

   <td width="126">8   Mehmet  10</td>

   <td width="26"><strong>02 </strong></td>

   <td width="134">11    Ali          16</td>

  </tr>

  <tr>

   <td width="29"><strong>03 </strong></td>

   <td width="108">3      Can      11</td>

   <td width="26"><strong>03 </strong></td>

   <td width="118">6    Ahmet      6</td>

   <td width="26"><strong>03 </strong></td>

   <td width="126">9    Zeynep    17</td>

   <td width="26"><strong>03 </strong></td>

   <td width="134">12    Yavuz     16</td>

  </tr>

 </tbody>

</table>










<ol>

 <li><strong>Query 1: </strong>select Age, Name from STUDENT where SID &lt; 9</li>

</ol>




<ol>

 <li><strong>Query 2: </strong>select Age from STUDENT where Age &lt; 8</li>

</ol>




<ul>

 <li><strong>Query 3: </strong>select * from STUDENT where Age = 8</li>

</ul>








