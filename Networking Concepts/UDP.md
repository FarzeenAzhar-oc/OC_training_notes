**User Datagram Protocol**
- Lightweight
- Works on top of IP
- Provides mechanism to detect corrupt data in packet, but doesn't solve  other problems
- SImple but fast

## Packet format
- Sending packets using UDP over IP , the data porion of each IP packet is formatted as a **UDP segment**
![Pasted image 20230111161509](Pasted%20image%2020230111161509.png)

Each UDP segment contains an **8 byte header and a variable length data**
Each byte represents the following
## Port number
- The first 4 bytes of UDP header stores the port number
	- i.e. $2^{16}$ [ports](ports.md)
- Go to [ports](ports.md) for a more general overview of [ports](ports.md)

## Segment length
- 2 bytes store length
- i.e. Max length = $2^{16} - 1 =65535$ bytes

## Checksum
- Final 2 bytes is checksum
- Field used by sender and reciever to check corruption in data segments

Before sending data sender will calculate checksum based on the data and add it in checksum
The reciever will calculate the same and compare


