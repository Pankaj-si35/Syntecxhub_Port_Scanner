# Syntecxhub_Port_Scanner
A Python-based TCP Port Scanner with multithreading, timeout handling, exception handling, and result logging.
# Python TCP Port Scanner

A beginner-friendly TCP Port Scanner developed in Python for learning
network security, socket programming, TCP connections, and basic
cybersecurity concepts.

## 📌 Project Overview

This project is a Python-based TCP port scanner that checks whether
specific TCP ports on a target host are open or closed.

The scanner uses Python socket programming to attempt TCP connections
and identify accessible ports.

It also includes:

- Custom target IP/hostname
- Custom port range
- TCP connection testing
- Timeout handling
- Exception handling
- Multithreaded scanning
- Scan result logging

> ⚠️ This tool is intended only for educational purposes and authorized
> security testing. Scan only systems that you own or have explicit
> permission to test.

---

## 🚀 Features

### 1. TCP Port Scanning

The scanner uses Python's `socket` module to establish TCP connections
with the specified ports.

### 2. Custom Target

The user can enter an IP address or hostname.

Example:

```text
127.0.0.1
```

### 3. Custom Port Range

The user can specify the starting and ending port.

Example:

```text
Starting port: 7995
Ending port: 8005
```

### 4. Open/Closed Detection

The scanner identifies ports as:

```text
[+] 8000/tcp OPEN
[-] 8001/tcp CLOSED
```

### 5. Timeout Handling

A socket timeout is configured so that the scanner does not wait
indefinitely for a response.

### 6. Exception Handling

The program handles invalid hostnames/IP addresses and socket errors
without unnecessarily crashing the scanner.

### 7. Multithreading

The project uses Python's `ThreadPoolExecutor` to scan multiple ports
concurrently.

```python
ThreadPoolExecutor(max_workers=20)
```

This makes the scanner faster than checking every port sequentially.

### 8. Result Logging

Scan results are stored in:

```text
scan.log
```

Example:

```text
Port 7995/tcp CLOSED
Port 8000/tcp OPEN
Port 8005/tcp CLOSED
```

---

## 🛠️ Technologies Used

- Python 3
- Socket Programming
- TCP/IP
- ThreadPoolExecutor
- Python Logging
- Kali Linux

---

## 📂 Project Structure

```text
python-tcp-port-scanner/
│
├── scanner.py
├── scan.log
├── README.md
└── screenshots/
    └── scanner-result.png
```

---

## ⚙️ Installation

### Step 1: Clone the repository

```bash
git clone <YOUR-GITHUB-REPOSITORY-URL>
```

### Step 2: Enter the project directory

```bash
cd python-tcp-port-scanner
```

### Step 3: Check Python version

```bash
python3 --version
```

---

## ▶️ How to Use

Run the scanner:

```bash
python3 scanner.py
```

The program will ask for the target:

```text
Enter target IP/hostname:
```

For local testing, use:

```text
127.0.0.1
```

Then enter the port range:

```text
Enter starting port: 7995
Enter ending port: 8005
```

---

## 🧪 Local Testing

For safe local testing, start a temporary HTTP server on port 8000:

```bash
python3 -m http.server 8000
```

Then run the scanner:

```bash
python3 scanner.py
```

Use:

```text
Target: 127.0.0.1
Starting port: 7995
Ending port: 8005
```

The scanner should detect port 8000:

```text
[+] 8000/tcp OPEN
```

Other ports may appear as:

```text
[-] 7999/tcp CLOSED
[-] 8001/tcp CLOSED
```

---

## 📸 Project Screenshots

### TCP Port Scan Result

The scanner successfully identifies port 8000 as open during local
testing.

![TCP Port Scanner Result](screenshots/scanner-result.png)

---

## 📝 Logging

After a scan, the results can be viewed using:

```bash
cat scan.log
```

Example:

```text
Port 7995/tcp CLOSED
Port 7996/tcp CLOSED
Port 8000/tcp OPEN
Port 8001/tcp CLOSED
Port 8005/tcp CLOSED
```

---

## 🎯 Learning Objectives

This project was created to understand:

- TCP/IP networking fundamentals
- TCP port concepts
- Python socket programming
- Client-server communication
- Port scanning methodology
- Socket timeout handling
- Exception handling
- Multithreading
- Security tool development
- Logging and result analysis

---

## 🔐 Security & Ethical Use

This tool should only be used against:

- Your own computer
- Your own virtual machines
- Authorized cybersecurity labs
- Systems for which you have explicit permission to perform testing

Do not scan public systems without authorization.

---

## 🔮 Future Improvements

Possible future improvements include:

- Command-line arguments using `argparse`
- Service/banner detection
- Scan speed configuration
- Better terminal output
- Export results to CSV
- Scan statistics
- Configurable timeout
- Improved error reporting

---

## 👨‍💻 Author

**Pankaj Singh**

Cybersecurity Learner | Python | Network Security | Ethical Hacking

---

## 📄 License

This project is intended for educational and authorized security
testing purposes.
