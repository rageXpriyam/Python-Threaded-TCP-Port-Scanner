Python Threaded TCP Port Scanner

Project Overview

This is a lean, highly efficient command-line utility designed for basic network reconnaissance and security auditing. It performs fast TCP port scans across a specified port range on a target host.

The project is built in Python and is optimized for speed by utilizing multithreading for concurrent connection attempts.

⚡ Key Features

Multithreading: Leverages Python's threading module to execute multiple port checks simultaneously, drastically reducing scan time.

TCP Connect Scan: Performs a full TCP connection attempt (connect_ex) to determine if a port is open.

Clear Output: Provides structured output indicating which ports are found to be OPEN.

Host Resolution: Automatically resolves hostnames to their respective IP addresses.

⚙️ Requirements

This script requires Python 3 and standard Python libraries (socket, sys, time, threading), which are typically included with any Python installation.

🚀 Usage

The script must be executed from the command line and requires three arguments: the target, the starting port, and the ending port.

Syntax

python3 port_scan.py <TARGET> <START_PORT> <END_PORT>


Argument

Description

Example

<TARGET>

The IP address or hostname of the target machine.

192.168.1.1 or scanme.nmap.org

<START_PORT>

The lowest port number to begin the scan at.

1

<END_PORT>

The highest port number to end the scan at.

1000

Example Execution

To scan ports 1 through 1024 on the hostname example.com:

python3 port_scan.py example.com 1 1024


Example Output

----------------------------------------------------------------------
Python Simple Port Scanner
----------------------------------------------------------------------
Scanning target 93.184.216.34
Port 80 is OPEN
Port 443 is OPEN
Time elapsed: 0.154382 seconds
