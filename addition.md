# Addition

Scenario: Add two numbers
  
  Given I have a calculator that's turned on.

  When I enter "number1"
  And I press "+" button
  And I enter "number2"
  And I press "=" button
  
  Then I see the "added sum" as the result

Scenario: Add more numbers

   Given I have a Calculator that's on a ON  

   When I enter first number and
   I press "+" button
   And enter next number 
   And press "+" button 
   And enter next number
   And press "+" button
   repeat this till last but one number  
   And enter the last number 
   And I press "=" button
   
   Then I see the "summation" of all the entered numbers

Scenario: Result is too large to display (or overrunning the limits)

  Given: I have a number to display as the result of the sum on the calculator's screen.

  When: I check it's length is not under limit of the calculator.

  Then: I display the rounded off value on the calculator's screen.

Scenario: Numbers can be negative

  Given I have a Calculator that's on a ON  

  When I enter "-ve number1"
  And I press "+" button
  And I enter " -ve number2"
  And I press "=" button
  
  Then I see the "added sum" as the result as a -ve no

Scenario: Numbers can be fraction

Scenario: Number can be irrational

Scenario: Length of each number

Scenario: If number1 or number2 is not entered

  Given I have a calculator that's turned on.

  When I do not enter "number1"
  And I press "+" button
  And I do not enter "number2"
  And I press "=" button

  Then I will see an error

Scenario: If the number is real/complex

  Given I have a calculator that's turned on.
  
  When I enter a real number, "number1"
  And I press "+" button
  And I enter a complex number,
  real part of "number2"
  And I press '+' button
  complex part of "number2"
  And I press "=" button

  Then I see the "error" or garbage value as the result

Scenario: If we are inbetween some operation

  Given I have a calculator that's turned on.

  When I enter "number1"
  And I press "+" button
  And I press some other arithmetic operation
  And I enter "number2"
  And I press "=" button

  Then I will see an error
