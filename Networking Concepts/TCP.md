- Ensures reliable data transfer
- Since it is mostly used with ip, it is sometimes called TCP/IP stack

# Packet Format
![Pasted image 20230113110732](Pasted%20image%2020230113110732.png)

- TCP header contains more fields than UDP and can range from 20 to 60 bytes
- They share some info with [UDP](UDP.md), like source port number, destination port number and checksum


# Start to finish
- Lets follow along in how connection is established

## Step 1: Establish connection
- Two computers need to establish connection via **three way 
![Pasted image 20230113111554](Pasted%20image%2020230113111554.png)

- Each packet will look something like this
![Pasted image 20230113111452](Pasted%20image%2020230113111452.png)

- SYN = Synchronize?
- ACK=Acknowledge!

- Three way handshake:
	1. The first computer sends a packet with **SYN** bit set to 1 
	2. The second computer sends back a packet with ACK bit set to 1 and SYN bit set to 1
	3. The first computer sends reply back with an ACK

- No data is utilised for the handshake, once connection is established they are ready to send and recieve packets

## Step 2: Send packets of data
![Pasted image 20230113114853](Pasted%20image%2020230113114853.png)

- Packet must always be acknowledged after they are recieved
- Steps involved:
	1. The first computer send data with and a sequence number
	2. The second computer acknowledges it by setting ACK bit and increasing the ack number by length of recieved data
![Pasted image 20230113122356](Pasted%20image%2020230113122356.png)

This helps in understanding which data was succefully recieved, lost  and which data was accidentally send twice

## Step 3: Close the connection
Either computers can close the connection when they no longer want to send or recieve data
![Pasted image 20230113122624](Pasted%20image%2020230113122624.png)

# Detecting lost packet
- TCP connection uses timeout to detect lost packets

![Pasted image 20230113123247](Pasted%20image%2020230113123247.png)

- Steps:
	1. After sending data, sender starts the time and puts packet in a retransmission queue
	2. If timer runs out and sender hasn't recieved ack from reciever, packet will be resend
	3. Retransmission may lead to the receipient recieving duplicate packets
- If a packet was not actually lost but just very slow, will have recieve duplicate packets

# Handling out of order packets
![Pasted image 20230113124139](Pasted%20image%2020230113124139.png)

If a seq no from sender doesn't match the one reciepent acknowledged, recipient send an ack with last ack no

Sometimes its due to slower route
![Pasted image 20230113125104](Pasted%20image%2020230113125104.png)

Sometimes the packet may be lost
![Pasted image 20230113125137](Pasted%20image%2020230113125137.png)


in anycase,  the sender must retransmit the packet