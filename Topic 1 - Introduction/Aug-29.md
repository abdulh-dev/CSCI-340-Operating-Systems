This is the first class, Lecture 1 slides
<mark style="background: #ADCCFFA6;">Text like this is my own notes seperate from the slides, CMD + H is the hotkey</mark>
<mark style="background: #FFF3A3A6;">Text like this is important and from the slides, CMD + J is the hotkey</mark>
#### Section goals 
- To describe the basic organization of computer systems 
- To provide a grand tour of the major components of operating systems 
- To give an overview of the many types of computing environments

#### Section Topics
- What is an Operating System? 
- Computer architecture and organization 
	- Memory 
	- I/O, interrupts, and buses 
	- Networks 
- Computing environments 
	- Distributed computing and virtualization 
	- Parallel computing
	- <mark style="background: #ADCCFFA6;">Cloud computing (similar to the other two but entirely different)</mark>
	


#### What is an Operating System?

<mark style="background: #ADCCFFA6;">The operating system is the middleman between the Applications and the Hardware. To manipulate the hardware for complex instructions and computations. Manipulating the hardware is any action taken by the computer. </mark>

<mark style="background: #ADCCFFA6;">The terminal is not an operating system.</mark>

<mark style="background: #ADCCFFA6;">The operating systems are needed for any type of computation </mark>

<mark style="background: #ADCCFFA6;">OSS - Operating System Services</mark> 

Parallel - multiple computers on 1 set of data

Distributed - multiple differnt streams of data on different computers


#### Computer system components 
- In general, a system is a cohesive collection of interrelated and interdependent parts. 
- A computer system includes the hardware and the software that together make the aggregate usable by users, which include not just people, but machines or other “things”. 
	- Hardware includes processors, I/O devices, all types of memory and secondary storage. 
	- Software includes the operating system and the software that uses it, which is called the application layer. 
		- <mark style="background: #FFF3A3A6;">The operating system is the software that interacts directly with the hardware; applications do not. </mark>
		- <mark style="background: #FFF3A3A6;">The application layer includes software development tools, web browsers, all types of media editors and viewers, shells, commands, etc. (User data is part of the application layer)</mark>


<mark style="background: #FFF3A3A6;">OS is essentially a program that acts as an intermediary between a user of a computer and the computer hardware</mark>
![[OS-in-system-image.png]]

OS requirements 
- The layered structure of a computer system implies that an operating system has three important responsibilities: 
	- The operating system alone must control the hardware resources. 
	- The operating system alone must enable and control the execution of all other software on the computer. 
	- The operating system must give users the ability to develop, run, and manage applications and their data. 
	- But these are not the only things for which operating systems are responsible

<mark style="background: #ADCCFFA6;">The OS conveys the needs of the application to the hardware and then convey the output back to the application.</mark>

<mark style="background: #ADCCFFA6;">If there are multiple commands, the operating system must organize and manage every command from the application.</mark>

<mark style="background: #ADCCFFA6;">This leads to different applications have different levels of privledge, based on the functionality of the machine</mark> 

