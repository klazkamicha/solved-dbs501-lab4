Download Link: https://assignmentchef.com/product/solved-dbs501-lab4
<br>
Write a stored Procedure called <strong>mine</strong> that  will accept as Input TWO character parameters: first will be in the Visa Expiry Date format (MM/YY) and second will be either P, F or B (any case). Then it will display what DAY is the Last day of the provided input format and also it will count how many stored Procedures, Functions or Package Bodies you have created in your schema.  You need to take care in your Exception section if the Expiry Date has an Invalid format and  if some other letter was entered.                                           <u>Here are the outputs.</u>

<strong><em>EXECUTE  mine (’11/09′,’P’)</em></strong>

<strong>Last day of the month 11/09 is MondayNumber of stored objects of type P is 7PL/SQL procedure successfully completed.</strong>

<strong><em>EXECUTE  mine (’12/09′,’f’)</em></strong>

<strong>Last day of the month 12/09 is ThursdayNumber of stored objects of type F is 2PL/SQL procedure successfully completed.</strong>

<strong><em>EXECUTE  mine (’01/10′,’T’)</em></strong>

<strong>Last day of the month 01/10 is SundayYou have entered an Invalid letter for the stored object. Try P, F or B.PL/SQL procedure successfully completed.</strong>

<strong><em>EXECUTE  mine (’13/09′,’P’)</em></strong>

<strong>You have entered an Invalid FORMAT for the MONTH and YEAR. Try MM/YY.PL/SQL procedure successfully completed.</strong>

2)         Write a stored Procedure called <strong>add_zip</strong> that  will accept as Input THREE parameters for three columns in the table ZIPCODE (ZIP, CITY and STATE).It will firstly check whether entered ZIP  already exists in the database and if YES – it will stop processing with the message. If NOT —  it will insert new row in the table ZIPCODE where other columns will use USER and SYSDATE pseudo columns. Also it will use TWO Output parameters to display message SUCCESS or FAILURE and current # of rows in the table for the entered STATE.  Then it will display ALL rows from that STATE.  Use BIND variables to display your results.                 Undo your Insert, when Success happened.                                  <u>Here are the outputs:</u>

<u>Case 1:</u>                                                                                                                                              <strong>PL/SQL procedure successfully completed.</strong>

<table width="90%">

 <tbody>

  <tr>

   <td><strong>FLAG </strong></td>

  </tr>

  <tr>

   <td>SUCCESS</td>

  </tr>

 </tbody>

</table>







<table width="90%">

 <tbody>

  <tr>

   <td colspan="3"><strong>ZIPNUM </strong></td>

  </tr>

  <tr>

   <td colspan="3">2</td>

  </tr>

  <tr>

   <td colspan="3"></td>

  </tr>

  <tr>

   <td></td>

  </tr>

  <tr>

   <td width="3"></td>

   <td width="628"></td>

   <td width="2"></td>

   <td width="3"></td>

  </tr>

 </tbody>

</table>

<strong>SELECT  * FROM zipcode</strong>

<strong>WHERE  state = ‘MI’</strong>

<table width="94%">

 <tbody>

  <tr>

   <td colspan="2" width="10%"><strong>ZIP </strong></td>

   <td colspan="2" width="11%"><strong>CITY </strong></td>

   <td width="4%"><strong>STATE </strong></td>

   <td width="21%"><strong>CREATED_BY </strong></td>

   <td width="14%"><strong>CREATED_DATE </strong></td>

   <td width="10%"><strong>MODIFIED_BY </strong></td>

   <td colspan="2" width="23%"><strong>MODIFIED_DATE </strong></td>

  </tr>

  <tr>

   <td colspan="2" width="10%">48104</td>

   <td colspan="2" width="11%">Ann Arbor</td>

   <td width="4%">MI</td>

   <td width="21%">AMORRISO</td>

   <td width="14%">03-AUG-99</td>

   <td width="10%">ARISCHER</td>

   <td colspan="2" width="23%">24-NOV-99</td>

  </tr>

  <tr>

   <td colspan="2" width="10%"><strong>18104 </strong></td>

   <td colspan="2" width="11%"><strong>Chicago </strong></td>

   <td width="4%"><strong>MI </strong></td>

   <td width="21%"><strong>DBS501_093A40 </strong></td>

   <td width="14%"><strong>12-NOV-09 </strong></td>

   <td width="10%"><strong>DBS501_093A40 </strong></td>

   <td colspan="2" width="23%"><strong>12-NOV-09 </strong></td>

  </tr>

  <tr>

   <td width="2%"> </td>

   <td colspan="8" width="92%"></td>

   <td width="3%"> </td>

  </tr>

  <tr>

   <td width="2%"> </td>

   <td colspan="2" width="10%"></td>

   <td colspan="7" width="85%"> </td>

  </tr>

  <tr>

   <td width="13"></td>

   <td width="34"></td>

   <td width="14"></td>

   <td width="48"></td>

   <td width="58"></td>

   <td width="121"></td>

   <td width="137"></td>

   <td width="121"></td>

   <td width="121"></td>

   <td width="21"></td>

  </tr>

 </tbody>

</table>

<strong>Rollback completed</strong>

<u>Case 2:</u>

<strong>This ZIPCODE 48104 is already in the Dataase. Try again.PL/SQL procedure successfully completed.</strong>

<table width="90%">

 <tbody>

  <tr>

   <td colspan="3"><strong>FLAG </strong></td>

  </tr>

  <tr>

   <td colspan="3">FAILURE</td>

  </tr>

  <tr>

   <td colspan="2"><strong>ZIPNUM </strong></td>

  </tr>

  <tr>

   <td colspan="2">1</td>

  </tr>

  <tr>

   <td colspan="2"></td>

  </tr>

  <tr>

   <td width="239"></td>

   <td width="236"></td>

   <td width="161"></td>

  </tr>

 </tbody>

</table>

<strong>SELECT  * FROM zipcode</strong>

<strong>WHERE  state = ‘MI’</strong>

<table width="94%">

 <tbody>

  <tr>

   <td width="10%"><strong>ZIP </strong></td>

   <td width="11%"><strong>CITY </strong></td>

   <td width="4%"><strong>STATE </strong></td>

   <td width="21%"><strong>CREATED_BY </strong></td>

   <td width="14%"><strong>CREATED_DATE </strong></td>

   <td width="10%"><strong>MODIFIED_BY </strong></td>

   <td width="23%"><strong>MODIFIED_DATE </strong></td>

  </tr>

  <tr>

   <td width="10%">48104</td>

   <td width="11%">Ann Arbor</td>

   <td width="4%">MI</td>

   <td width="21%">AMORRISO</td>

   <td width="14%">03-AUG-99</td>

   <td width="10%">ARISCHER</td>

   <td width="23%">24-NOV-99</td>

  </tr>

 </tbody>

</table>

<strong> </strong>

3)         Re-write the previous question so that you use a stored BOOLEAN FUNCTION called <strong>exist_zip</strong> that will check if the provided zip code already exists in the database or not. Then incorporate your function into the new  procedure called <strong>add_zip2.</strong>    <u>Outputs remain the same.</u>

4)         Write a stored CHARACTER FUNCTION called <strong>instruct_status</strong> that  will accept as Input TWO parameters – instructor’s First and Last name entered in the Upper case. It will firstly check whether the entered name combination exists,  and if NOT  – it will stop processing with the message. If YES —  it will then count how many sections is this person scheduled to teach and then display the appropriate message (the basic criteria is more than 9 courses or NO courses or  between those two numbers).                                                                                                   You will test your function firstly with the plain SELECT statement (A) and then with the BIND variables (B and C)                                                                         <u>Here are the outputs:</u>

<ol>

 <li>A) After SELECT statement has been issued</li>

</ol>

<table width="90%">

 <tbody>

  <tr>

   <td><strong>LAST_NAME </strong></td>

   <td><strong>Instructor Status </strong></td>

  </tr>

  <tr>

   <td><strong>Chow </strong></td>

   <td><strong>This Instructor is NOT scheduled to teach </strong></td>

  </tr>

  <tr>

   <td><strong>Frantzen </strong></td>

   <td><strong>This Instructor will teach 10 course and needs a vacation </strong></td>

  </tr>

  <tr>

   <td><strong>Hanks </strong></td>

   <td><strong>This Instructor will teach 9 courses. </strong></td>

  </tr>

  <tr>

   <td><strong>Lowry </strong></td>

   <td><strong>This Instructor will teach 9 courses. </strong></td>

  </tr>

  <tr>

   <td><strong>Morris </strong></td>

   <td><strong>This Instructor will teach 10 course and needs a vacation </strong></td>

  </tr>

  <tr>

   <td><strong>Pertez </strong></td>

   <td><strong>This Instructor will teach 10 course and needs a vacation </strong></td>

  </tr>

  <tr>

   <td><strong>Schorin </strong></td>

   <td><strong>This Instructor will teach 10 course and needs a vacation </strong></td>

  </tr>

  <tr>

   <td><strong>Smythe </strong></td>

   <td><strong>This Instructor will teach 10 course and needs a vacation </strong></td>

  </tr>

  <tr>

   <td><strong>Willig </strong></td>

   <td><strong>This Instructor is NOT scheduled to teach </strong></td>

  </tr>

  <tr>

   <td><strong>Wojick </strong></td>

   <td><strong>This Instructor will teach 10 course and needs a vacation </strong></td>

  </tr>

 </tbody>

</table>

<strong>10 rows selected.</strong>

<ol>

 <li>B) After INPUT parameters ‘PETER’ and ‘PAN’ were provided <strong>PL/SQL procedure successfully completed.</strong></li>

</ol>




<table width="90%">

 <tbody>

  <tr>

   <td colspan="3"><strong>MESSAGE </strong></td>

  </tr>

  <tr>

   <td colspan="3"><strong>There is NO such instructor</strong>.</td>

  </tr>

  <tr>

   <td colspan="3"></td>

  </tr>

  <tr>

   <td></td>

  </tr>

  <tr>

   <td width="3"></td>

   <td width="628"></td>

   <td width="2"></td>

   <td width="3"></td>

  </tr>

 </tbody>

</table>

<ol>

 <li>C) After INPUT parameters ‘IRENE’ and ‘WILLIG’ were provided <strong>PL/SQL procedure successfully completed.</strong></li>

</ol>

<table width="90%">

 <tbody>

  <tr>

   <td colspan="4"><strong>MESSAGE </strong></td>

  </tr>

  <tr>

   <td colspan="4"><strong>This Instructor is NOT scheduled to teach </strong></td>

  </tr>

  <tr>

   <td colspan="4"></td>

  </tr>

  <tr>

   <td colspan="2"> </td>

  </tr>

  <tr>

   <td></td>

   <td> </td>

  </tr>

 </tbody>

</table>