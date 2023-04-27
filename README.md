# Router_1x3
Routing is the process of moving a packet of data from source to destination and enables messages to pass from one computer to another and eventually reach the target machine.
A router is a networking device that forwards data packets between computer networks.

There are various sub-modules of router i.e. Register, FIFO, FSM and Synchronizer which are synthesized and simulated and finally connected to its top module. 
Router- Top Level module consists of FSM, REGISTER,SYNCHRONIZER, FIFO_0, FIFO_1, FIFO_2.

PACKET FORMAT: The packet consists of 3 parts: Header, payload and parity each of 8 bit width and the length of the payload can be extended between 3 between 1 byte to 63 byte.

Router : FIFO

There are 3 FIFOs used in the router design. Each FIFO is of 9 bits wide and 16 bit bytes depth. 
The 9th bit is 1 for header byte and 0 for the remaining bytes.

Router : SYNCHRONIZER

This module provides synchronization between router FSM and router FIFO modules.
It provides faithful communication between the single input port and three output ports.

Router : FSM

there are 8 states in the fsm which generates the control signals for other blocks in the router

DECODE_ADDRESS,LOAD_FIRST_DATA,LOAD_DATA,LOAD_PARITY,FIFO_FULL_STATE,LOAD_AFTER_FULL,WAIT_TILL_EMPTY,CHECK_PARITY_ERROR

ROUTER: REGISTER

This module implements 4 internal registers in order to hold a header byte, FIFO full state byte, internal parity and
packet parity byte.
