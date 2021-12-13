Using MATLAB, a code to emulate the USB and UART protocols in the transmitting state. 

The code reads a file based on the user request:
• A Configuration File: which is a JSON file that contains the protocol name and parameters
(like bit rate, number of stop bits, … etc.). 
containing an array of 2 objects: one for UART and the other for USB. Please, refer to the
provided configuration file to determine the protocol names as either “USB” or “UART”. Any
other protocol name should result in an error message to the user. For each case, your code should
decode the following information from the provided configuration file:

◦ For the case of UART:
▪ The number of data bits per packet (either 7 or 8 bits).
▪ The number of stop bits (1 or 2 bits).
▪ The parity used (even, odd, or none).
▪ The bit duration.
◦ For the case of USB:
▪ The synchronization pattern (8 bits: 7 zeros followed by a one).
▪ The length of the packet identifier (8 bits for PID).
(Note that PID of the first packet is 1 and is incremented by 1 for every new packet).
▪ The destination address (11 bits) (assume any 11 bit address).
▪ The size of the payload (assume it 128 bytes).
▪ The bit duration.
• An Input Data File: which is an ASCII text file that contains the data to be transmitted by
the protocol specified by the user. Please use the attached file (inputdata.txt)
 
