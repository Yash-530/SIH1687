# Web Application Fuzzer

## Overview
Web applications are essential for online services but are prone to cyber-attacks. This fuzzer automates the discovery and security testing of directories, virtual hosts, API endpoints, URL parameters, custom test cases, and subdomains, ensuring robust security measures.

## Features
- **Directory and File Enumeration**: Identifies hidden directories and files.
- **Virtual Host Discovery**: Detects misconfigured virtual hosts.
- **API Endpoint Testing**: Evaluates API security vulnerabilities.
- **Parameter Fuzzing**: Identifies SQLi, XSS, and other injection flaws.
- **Custom Test Cases**: Supports user-defined security tests.
- **Subdomain Enumeration**: Maps additional attack surfaces.
- **Comprehensive Reporting**: Provides structured reports on vulnerabilities.

## Project Structure
```
web-fuzzer/
├── data/                 # Storage for wordlists and payloads
│   ├── wordlists/        # Common directories, parameters, subdomains
│   ├── payloads/         # Predefined attack payloads
├── src/                  # Source code
│   ├── fuzzer.py         # Main fuzzing engine
│   ├── directory_fuzz.py # Directory and file enumeration
│   ├── vhost_fuzz.py     # Virtual host detection
│   ├── api_fuzz.py       # API endpoint security analysis
│   ├── parameter_fuzz.py # URL parameter fuzzing
│   ├── subdomain_fuzz.py # Subdomain discovery
│   ├── custom_tests.py   # User-defined test cases
│   ├── report_generator.py # Automated reporting tool
│   ├── utils.py          # Utility functions and helpers
├── reports/              # Stores generated vulnerability reports
├── config/               # Configuration files
├── logs/                 # Logs for debugging and tracking
├── requirements.txt      # Python dependencies
├── README.md             # Project documentation
├── LICENSE               # License information
```

## Installation
```bash
git clone https://github.com/YOUR_GITHUB_USERNAME/web-fuzzer.git
cd web-fuzzer
pip install -r requirements.txt
```

## Usage
### Running the Fuzzer
```bash
python src/fuzzer.py --target https://example.com --mode all
```
**Modes:**
- `directories`: Enumerates directories and files.
- `vhosts`: Identifies virtual hosts.
- `api`: Tests API endpoints.
- `parameters`: Fuzzes URL parameters.
- `subdomains`: Discovers subdomains.
- `custom`: Executes user-defined test cases.
- `all`: Runs all available tests.

### Sample Output
```
[+] Found hidden directory: /admin/
[+] Potential SQL injection detected in parameter: id
[+] Subdomain discovered: dev.example.com
```

## Configuration
Modify `config/settings.json` to customize scanning parameters, request headers, and concurrency settings.

## Reporting
Reports are saved in `reports/` in JSON and HTML formats, detailing findings and remediation suggestions.

## Future Enhancements
- **Machine Learning Integration**: AI-driven vulnerability classification.
- **Multi-threaded Execution**: Faster and more efficient fuzzing.
- **GUI Interface**: User-friendly visual interface for configuring scans.
- **Real-time Notifications**: Alerts on detected vulnerabilities.

## Contribution
Pull requests are welcome. For major changes, open an issue first to discuss the proposed modifications.

## License
Distributed under the MIT License. See `LICENSE` for details.
