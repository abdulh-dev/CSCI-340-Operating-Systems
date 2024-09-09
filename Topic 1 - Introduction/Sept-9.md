#### Input/Output Problems 
- Computers have a wide variety of peripherals. 
	- Delivering different amounts of data, at different speeds, in different formats. 
- Many are not connected directly to system or expansion bus. 
- Most peripherals are slower than CPU and RAM; a few are faster. 
<mark style="background: #ADCCFFA6;">(a peripheral is any device that isn't internal to the computer)</mark>
- Word length for peripherals may vary from the CPU. 
<mark style="background: #ADCCFFA6;">(Word length is 4bytes in a 32bit system, each word is the unit of memory)</mark>
- Data format may vary (e.g., one word might include parity bits).

<mark style="background: #ADCCFFA6;">CPU needs to fetch and store data, it does this with Memory. The problem here is that its time consumption is very inefficient as the cpu is fast while the memory is slow. (More memory is slower memory). To solve this, we use the cache (an intermediate). The cache can only hold a small amount of relevant data but due to that it can move fast.</mark>


- Peripheral communications are handled with I/O modules. 
- Two major functions: 
	- Interface to processor or memory via bus or central link. 
	- Interface to one or more peripherals via tailored data links.

![[Pasted image 20240909144555.png]]
(I/O module is not an I/O device)
Think of them as middlemen between the system and I/O devices to hold data bdue to their different speeds

#### I/O Module Functions and Structure 
- Major requirements or functions of an I/O module are: 
	- Control & Timing. 
	- CPU Communication. 
	- Device Communication. 
	- Data Buffering. 
	- Error Detection.
![[Pasted image 20240909150635.png]]

#### I/O Operation 
- Three techniques are possible for I/O operations: •
- Programmed I/O • Data are exchanged between the processor and the I/O module • Processor executes a program that gives it direct control of the I/O operation • When the processor issues a command it must wait until the I/O operation is complete • If the processor is faster than the I/O module this is wasteful of processor time 
<mark style="background: #ADCCFFA6;">CPU oversees the entire operation, it does nothing else.

The drawback is that it performs very poorly, in terms of time efficiency</mark>

- Interrupt-driven I/O • Processor issues an I/O command, continues to execute other instructions, and is interrupted by the I/O module when the latter has completed its work 
<mark style="background: #ADCCFFA6;">The CPU will continuosly work and the the other I/O modules will send an interrupt to the cpu telling it is done with the data transfer and can use the data

The drawback that the cpu will still halt at times for each interrupt</mark>

- Direct memory access (DMA) • The I/O module and main memory exchange data directly without processor involvement
The DMA oversees the entire operation in terms of I/O modules 

![[Pasted image 20240909151224.png]]

#### Interrupt Driven I/O 
- Basics 
	- Overcomes CPU waiting and preventing that to happen. 
	- No repeated CPU checking of device. 
	- I/O module interrupts when ready. 

- Operation 
	- CPU issues read command. 
	- I/O module gets data from peripheral while CPU does other work. 
	- I/O module interrupts CPU. 
	- CPU requests data. 
	- I/O module transfers data.

<mark style="background: #ADCCFFA6;">Program counter  is one of the fundamental registers in the cpu, it keeps track of the current and next in line of execution.</mark>

<mark style="background: #ADCCFFA6;">Each interruption has its own sequence of commands (subroutine) based on the type of interruption.
</mark>
![[Pasted image 20240909152516.png]]
![[Pasted image 20240909152540.png]]
Last in first out

#### Design Issues 
- How do you identify the module issuing the interrupt? 
	- Software poll: 
		- CPU asks each module in turn, or checks status register in each module. 
		- Slow. 
	- Daisy Chain or Hardware poll: 
		- Interrupt Acknowledge sent down a chain. 
		- Module responsible places vector on bus. 
		- CPU uses vector to identify handler routine. 
	- Bus arbitration: • Module must claim the bus before it can raise interrupt, e.g. PCI & SCSI. • Processor responds with Interrupt Acknowledge. • Module can then place vector on bus. • How do you deal with multiple interrupts? • Each interrupt line has a priority. • Higher priority lines can interrupt lower priority lines. • If bus mastering only current master can interrupt.


need to do up to slide 43