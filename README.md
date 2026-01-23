# SQLMap Automation Script (sqlm)

[![zread](https://img.shields.io/badge/Ask_Zread-_.svg?style=flat&color=00b0aa&labelColor=000000&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB3aWR0aD0iMTYiIGhlaWdodD0iMTYiIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTQuOTYxNTYgMS42MDAxSDIuMjQxNTZDMS44ODgxIDEuNjAwMSAxLjYwMTU2IDEuODg2NjQgMS42MDE1NiAyLjI0MDFWNC45NjAxQzEuNjAxNTYgNS4zMTM1NiAxLjg4ODEgNS42MDAxIDIuMjQxNTYgNS42MDAxSDQuOTYxNTZDNS4zMTUwMiA1LjYwMDEgNS42MDE1NiA1LjMxMzU2IDUuNjAxNTYgNC45NjAxVjIuMjQwMUM1LjYwMTU2IDEuODg2NjQgNS4zMTUwMiAxLjYwMDEgNC45NjE1NiAxLjYwMDFaIiBmaWxsPSIjZmZmIi8%2BCjxwYXRoIGQ9Ik00Ljk2MTU2IDEwLjM5OTlIMi4yNDE1NkMxLjg4ODEgMTAuMzk5OSAxLjYwMTU2IDEwLjY4NjQgMS42MDE1NiAxMS4wMzk5VjEzLjc1OTlDMS42MDE1NiAxNC4xMTM0IDEuODg4MSAxNC4zOTk5IDIuMjQxNTYgMTQuMzk5OUg0Ljk2MTU2QzUuMzE1MDIgMTQuMzk5OSA1LjYwMTU2IDE0LjExMzQgNS42MDE1NiAxMy43NTk5VjExLjAzOTlDNS42MDE1NiAxMC42ODY0IDUuMzE1MDIgMTAuMzk5OSA0Ljk2MTU2IDEwLjM5OTlaIiBmaWxsPSIjZmZmIi8%2BCjxwYXRoIGQ9Ik0xMy43NTg0IDEuNjAwMUgxMS4wMzg0QzEwLjY4NSAxLjYwMDEgMTAuMzk4NCAxLjg4NjY0IDEwLjM5ODQgMi4yNDAxVjQuOTYwMUMxMC4zOTg0IDUuMzEzNTYgMTAuNjg1IDUuNjAwMSAxMS4wMzg0IDUuNjAwMUgxMy43NTg0QzE0LjExMTkgNS42MDAxIDE0LjM5ODQgNS4zMTM1NiAxNC4zOTg0IDQuOTYwMVYyLjI0MDFDMTQuMzk4NCAxLjg4NjY0IDE0LjExMTkgMS42MDAxIDEzLjc1ODQgMS42MDAxWiIgZmlsbD0iI2ZmZiIvPgo8cGF0aCBkPSJNNCAxMkwxMiA0TDQgMTJaIiBmaWxsPSIjZmZmIi8%2BCjxwYXRoIGQ9Ik00IDEyTDEyIDQiIHN0cm9rZT0iI2ZmZiIgc3Ryb2tlLXdpZHRoPSIxLjUiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIvPgo8L3N2Zz4K&logoColor=ffffff)](https://zread.ai/YanivHaliwa/sqlmap_enhance)

A powerful bash script that enhances and automates SQLMap operations for SQL injection testing with advanced output processing and data organization.

## Disclaimer

This tool is intended for legal security testing purposes only. Using this tool against any website or application without explicit permission is illegal. Always ensure you have proper authorization before conducting security tests.

## Description

This script streamlines SQLMap usage for security professionals by:

- Automating common SQLMap commands with an easy-to-use interface
- Organizing extracted data in a structured, readable format
- Providing an interactive menu for various SQL injection testing options
- Extracting and organizing database schemas and content systematically
- Capturing and securely storing password hashes and credentials
- Generating comprehensive reports of discovered vulnerabilities

## Features

### Core Functionality
- Interactive testing menu with guided options
- Support for both URL targets and request file inputs
- DBMS type specification for targeted testing
- Structured output organization in user-defined directories

### Automated Detection & Extraction
- Complete database enumeration and discovery
- Table schema automatic extraction and organization
- Intelligent data extraction from vulnerable tables
- Password hash capture and secure storage
- System information gathering (OS, hostname, web server details)
- Privilege escalation opportunity detection

### Data Management
- Rebuilds structure logs with consistent formatting
- Deduplicates extracted data for clean results
- Creates separate files for each database and table
- Merges cached results to prevent data loss
- Maintains session context across multiple runs

## Installation

1. Clone the repository using the following command:

```bash
git clone https://github.com/YanivHaliwa/sqlmap_enhance.git
cd sqlmap_enhance
```

2. Navigate to the SQLMap enhance directory:
   ```bash
   cd Cyber-Stuff/sqlmap_enhance
   ```

3. Make the script executable:
   ```bash
   chmod +x sqlmLite sqlmPro sqlway
   ```
 

4. Ensure you have SQLMap installed:
   ```bash
   # Install sqlmap if not already installed
   sudo apt-get install sqlmap
   ```

## Usage

```bash
./sqlm -r <request-file> | -u <url-or-ip> [-d <dbms>]
```

### Options:
- `-r` - Specify a request file (captured HTTP request)
- `-u` - Specify a target URL or IP address
- `-d` - Specify the DBMS type (optional)

## Example Workflows

### Testing a vulnerable web form:
```bash
./sqlm -u "http://vulnerable-site.com/page.php?id=1"
```

### Using a captured request with Burp Suite:
```bash
./sqlm -r request.txt
```

### Targeting a specific database type:
```bash
./sqlm -u "http://vulnerable-site.com/page.php?id=1" -d mysql
```

## Requirements

- SQLMap installed and available in PATH
- Bash shell environment
- Standard Unix utilities

## Security Considerations

- Only use on systems you have explicit permission to test
- Handle extracted data securely and confidentially
- Follow responsible disclosure practices
- Delete sensitive extracted data when testing is complete

## License

This script is provided for educational and professional security testing purposes only.

## Author

Created by [Yaniv Haliwa](https://github.com/YanivHaliwa) for security testing and educational purposes.
