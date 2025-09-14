# Capture Network Traffic with Wireshark

## Objective
Capture and analyze network traffic using **Wireshark**, based on the provided screen recording.  
The focus is on **HTTP traffic** (requests and responses) and understanding client-server communication.

## Method
Representative frames were extracted from the recording at regular intervals and reviewed to compile findings.  
The analysis focused on observed Wireshark actions such as starting a capture, applying filters, and inspecting packets.

## Findings
- Wireshark was launched and an active network interface selected.  
- The capture was started, generating live traffic.  
- A filter was applied: `http`.  
- HTTP **GET** and **POST** requests were observed, including host headers and user-agent strings.  
- Server responses such as **HTTP/1.1 200 OK** and **404 Not Found** were visible.  
- Packet details expanded to show TCP/IP layers and HTTP headers.  

## Detailed Analysis
1. **HTTP Request/Response Flow**: The recording demonstrates how browsers send GET requests and receive server responses.  
   Host headers and user-agent strings confirm details of the client.  

2. **Protocol Layers**: The packet details pane shows Ethernet, IP, TCP, and HTTP layers, illustrating encapsulation.  

3. **Filters**: Applying the `http` filter effectively isolates web traffic from other noise.  

4. **Troubleshooting Potential**: Capturing HTTP reveals errors (404 responses) and validates server availability.  

## Recommendations
- Use HTTPS for sensitive data instead of HTTP to avoid clear-text transmissions.  
- Apply filters (e.g., `ip.addr == x.x.x.x`) to narrow analysis to specific hosts.  
- Regularly capture and analyze traffic for troubleshooting and security auditing.  
- Save captures in `.pcap` format for future offline analysis.  
- Consider exporting packet details to CSV/JSON for automated log analysis.  

## Deliverables
- `wireshark_capture.pcap` → Saved capture file  
- `README.md` → Explanation of captured packets  

## Demo Video Idea
1. Launch Wireshark and select a network interface.  
2. Start capturing live traffic.  
3. Browse a website to generate HTTP packets.  
4. Stop capture and save results as `wireshark_capture.pcap`.  
5. Apply the `http` filter to display only HTTP traffic.  
6. Walk through HTTP requests and responses (GET/POST and 200 OK).  
