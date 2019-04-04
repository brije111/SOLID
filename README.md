# SOLID


SOLID is one of the most important acronyms in the world of Object Oriented Programming.

The importance of SOLID comes from the fact that it is practically impossible to write a &quot;clean&quot; code if you don&#39;t know what distinguishes a &quot;clean&quot; code from a &quot;dirty&quot; one.

SOLID principle are not rules or laws or perfect truth. It is a good principle or advice in order to write &quot;clean&quot; code.

Developed by American software engineer &amp; instructor Robert C Martin (also known as Uncle Bob) in his tech paper &quot;Design principles &amp; design patterns&quot;

It was Michael Feathers (the author of &quot;Working Effectively with Legacy Code&quot;) who &quot;acronymized&quot; these principles to SOLID.

#

**1.Single Responsibility Principle (SRP)**


- A class should have one and only one reason to change
- In SRP responsibility is &quot;reason to change&quot;.
- SRP looks simple on the first glance, but it is, probably, the most difficult SOLID principle to follow in practice.
- Following SRP is difficult because &quot;reasons to change&quot; become certain only in the future, when requirements actually change. At design time, all we can do is estimate which requirements are likely to change and which are stable. In other words, following SRP inevitably involves some amount of prophetic work.
- In addition to being the most difficult to implement, SRP is also the most fundamental SOLID principle. The more the design violates SRP, the less the gain from application of other SOLID principles will be.
- To know whether a class follow SRP ask &quot;What that class does?&quot; If you have to use the conjunction &quot;and&quot; or &quot;or&quot; the it is likely that class don&#39;t follow SRP



**Benefits**

- Easier to change
- Easier to understand
- More reusable
- Easier to test



**Example 1**
```
package srp;

public class Employee {
	double calculatePay() {
		//business logic for calculating payment
		return 0;
	}
	
	Employee save(Employee emp) {
		//business logic for storing employee information
		return emp;
	}
}
/*
 * So this call has 2 responsibility, So this doesn't follow the SRP
 * The solution is there should be two classes one for each responsibility
 */
class EmployeePay{
	double calculatePay() {
		//business logic for calculating payment
		return 0;
	}
}
class EmployeeRepo{
	Employee save(Employee emp) {
		//business logic for storing employee information
		return emp;
	}
}
```



**Example 2**

 

**Example 3**

 
