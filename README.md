# CodtechInternshipTask-2
Name:   Deepanshu Thappa
Company: CODTECH IT SOLUTION
ID:     CT08DS5186
Domain: Cyber Security

# Python Port Scanner

This is a simple Python script that scans a range of ports on a specified IP address. It uses multi-threading to speed up the scanning process and identifies open ports.

## Features
- Scans a range of ports on a given IP address.
- Uses multi-threading for faster scanning.
- Simple and easy-to-use interface.

## Usage

### Requirements
- Python 3.x

### Running the Port Scanner

1. Clone the repository or download the script.

    ```bash
    git clone https://github.com/yourusername/port-scanner.git
    cd port-scanner
    ```

2. Run the script.

    ```bash
    python port_scanner.py
    ```

3. Enter the IP address and port range when prompted.

    ```plaintext
    Enter the IP address to scan: 192.168.1.1
    Enter the starting port: 1
    Enter the ending port: 1024
    ```

4. The script will output open ports in the specified range.

    ```plaintext
    Scanning ports 1 to 1024 on 192.168.1.1
    Port 22: Open
    Port 80: Open
    ```

## Code Explanation

The script consists of three main parts:

1. **scan_port(ip, port)**: This function tries to connect to a specified port on the given IP address. If the connection is successful (result == 0), it prints that the port is open.
2. **scan_ports(ip, start_port, end_port)**: This function creates a thread for each port in the specified range and starts the threads. It waits for all threads to finish using `thread.join()`.
3. **Main function**: The script asks the user for the target IP address and the range of ports to scan. It then calls `scan_ports` with the provided inputs.
