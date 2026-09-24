## Quiz One

### 1.3

- Packet: portion of data
- Packet switches: routers + link-layer switches
- Store and forward transmission: must have recieved all of a packet before 
  it can be sent
- Forwarding tables: Switches have these tables which convert destination IPs
  to intermidary router IPs
- Routing Protocols: How do I decide the mapping in myforwarding table? EX: 
  shortest path!  
- Circuit Switching: reserve links for data transfer (analogy: a restaraunt 
  that takes reservations)
    - Gives guarantee throuput rates
    - Does not guarantee lack of congestion
    - Requires setup overhead
    - Multiplexing:
        - Frequency-Division Multiplexing: 'each circuit continuously gets a 
          fraction of bandwidth'
        - Time Division Multiplexing: 'each circuit gets all of the bandwidth 
          periodically'
 - Packet Switching vs. Circuit Switching:
     - Packet switching (more popular):
         - Pros:
             - Simpler to implement
             - Better use of resources
         - Cons:
             - Variable end-to-end delays => bad for realtime services 
               like telephony
    - Circuit Switching:
        - Pros:
            - Guaranteed end-to-end delays => better for real-time services
        - Cons: 
            - Wasteful of resources
- Network of Networks (structure 5)
    - ISP hierarchy: Access ISP -> Regional ISP -> Tier-1 ISP
    - Point of Presence (PoP): Group of routers in a location that can be paid 
      to connected to
    - Multi-home: ISP connecting to two or more ISPs above it
    - Peer: Neery ISPs can connect with oneanother
    - IXP: somewhere where multiple ISPs can peer together
    - Content-Provider Network (EX: Google)

### 1.4

- Delay in Packet-Switched Networks:
    - Total nodal delay = processing + queueing + transmission
        - Notice no propagation
    - Processing delay: process headers, read forward table, error checking
    - Note that these types of problems can be thought of as simple unit 
      conversion math
- Queueing Delay + Packet Loss
    - Traffic Intesity = # of bits $\cdot$ average rate at which packets arrive
      at the queue / transmission rate
    - Intensity > 1 => infinite average delay
    - Intensity $\le$ 1 => average queuing delay of 0 under uniform traffic, 
      bursty traffic => $\frac{N - 1) L}{2R}$
   - Packet loss: queue's full => packet loss
- End-to-end Delay: how long it takes a packet to get from A to B (does not 
  take into account queuing delay)
- Traceroute: a program for tracking the path of data
- Throughput in Computer Networks:
    - Instantaneous throughput: rate at which reciever is recieving a file
    - Average throughput: rate over some period of time
    - Bottleneck link: has lower transmission rate than its throughput -> 
      slowing down the message transfer

### 2.2 The WEb and HTTP

- 

### 2.4
