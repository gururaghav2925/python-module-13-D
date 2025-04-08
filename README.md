
## Python Program to Evaluate Prefix Expression Using Stack

## Aim:
To write a Python program that takes a prefix expression from the user and evaluates it using a stack.

## Procedure:

1.Get the prefix expression from the user (space-separated).

2.Reverse the expression for left-to-right evaluation.

3.Initialize an empty stack.

4.For each symbol:

  If it’s a number, push it onto the stack.
  
  If it’s an operator, pop two operands from the stack, apply the operator, and push the result back.

5.After evaluation, the stack will contain the final result.

6.Display the result.


## Program:
```python
OPERATORS=set(['*','-','+','%','/','**']) 
def evaluate(expression):
	stack = []
	for c in expression[::-1]:
		if c not in OPERATORS:
			stack.append(int(c))
		else:
			o1 = stack.pop()
			o2 = stack.pop()
			if c == '+':
				stack.append(o1 + o2)
			elif c == '-':
				stack.append(o1 - o2)
			elif c == '*':
				stack.append(o1 * o2)
			elif c == '/':
				stack.append(o1 / o2)
	return stack.pop()
test_expression = input()
print("Prefix Expression :",test_expression)
print("Evaluation result :",evaluate(test_expression))
   ``` 
## Output:
![image](https://github.com/user-attachments/assets/8d76beef-0874-454f-b880-ed4ab0df562b)

## Result:
The program evaluates the given prefix expression using stack operations and displays the final result.
## INSTRUCTOR LED EXAM:
![image](https://github.com/user-attachments/assets/b45ea6ed-91d6-443b-8a59-f2c1ea200fe7)
![image](https://github.com/user-attachments/assets/0c79a2af-42ab-4404-8ec7-8dc87299baef)
![image](https://github.com/user-attachments/assets/9ede8660-5f10-4744-9eaa-efc45245d65f)
![image](https://github.com/user-attachments/assets/a45b389b-a6e5-4af4-b2ea-a55864338084)
![image](https://github.com/user-attachments/assets/8f570420-447e-4c92-88f7-3e672c963a8c)

[python 13.pdf](https://github.com/user-attachments/files/19650058/python.13.pdf)



