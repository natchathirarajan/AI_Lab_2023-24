# Ex.No: 10  Logic Programming –  Simple queries from facts and rules
### DATE: 09/03/2024                                                                           
### REGISTER NUMBER : 212221040112
### AIM: 
To write a prolog program to find the answer of query. 
###  Algorithm:
	@@ -21,9 +21,21 @@ Construct the FOL representation for the following sentences <br>
5.	 Bill eats peanuts  <br> 
   Convert into clause form and Prove that John like Apple by using Prolog. <br> 
### Program:
```prolog
likes(john,X):- 
 food(X). 
eats(bill,X):- 
 eats(sue,X). 
eats(Y,X):- 
 food(X). 
eats(bill,peanuts). 
food(apple). 
food(chicken). 
food(peanuts).
```

### Output:
![image](https://github.com/Anbuselvan04/AI_Lab_2023-24/assets/119410896/a6f76a92-72cf-4c8b-817b-32db45ec46de)

### Task 2:
Consider the following facts and represent them in predicate form: <br>              
	@@ -34,18 +46,46 @@ Consider the following facts and represent them in predicate form: <br>
Convert the facts in predicate form to clauses and then prove by resolution: “Steve likes BK301 course”<br> 

### Program:
```prolog
likes(steve,X):-
     easycourse(X).
hard(sciencecourse).
easycourse(X):-
          course(X,dept(havefun)).
course(bk301,dept(havefun)).
```

### Output:
![image](https://github.com/Anbuselvan04/AI_Lab_2023-24/assets/119410896/0b52fb45-fb4b-443a-acd2-69b96e86113a)

### Task 3:
Consider the statement <br> 
“This is a crime for an American to sell weapons to hostile nations. The Nano , enemy of America has some missiles and its missiles were sold it by Colonal West who is an American” <br> 
Convert to Clause form and prove west is criminal by using Prolog.<br> 
### Program:
```prolog
criminal(X):-
	american(X),
	weapon(Y),
	hostile(Z),
	sells(X,Y,Z).
weapon(Y):-
                 missile(Y).
hostile(Z):-
                 enemy(Z,X).
sells(west,Y,nano):-
	missile(Y),
	owns(nano,Y).
missile(m).
owns(nano,m).
enemy(nano,america).
american(west).
```

### Output:
![image](https://github.com/Anbuselvan04/AI_Lab_2023-24/assets/119410896/47d234a8-6f84-43f9-88dc-67abcd56e301)

### Result:
Thus the prolog programs were executed successfully and the answer of query was found.
