README - TCP Port Scanner Tool

This is a Python-based TCP port scanning tool that utilizes the `nmap` library to scan a given hostname or IP address for open ports. It provides a command-line interface to accept the target host and a list of ports to scan. The tool attempts to identify the service running on each port and displays the state of the port (open or closed).

## Installation

1. Clone the repository or download the `scanner.py` file to your local machine.
2. Ensure you have Python installed on your system (version 3.6 or higher).
3. Install the required dependencies by running the following command:

```
pip install python-nmap argparse
```

## Usage

To use the TCP port scanner tool, follow these steps:

1. Open a terminal or command prompt.
2. Navigate to the directory where the `scanner.py` file is located.
3. Run the following command:

```
python scanner.py -o <host> -p <port1,port2,port3...>
```

Replace `<host>` with the IP address or hostname you want to scan, and `<port1,port2,port3...>` with a comma-separated list of ports you want to scan.

For example, to scan the host `192.168.1.100` on ports `80`, `443`, and `8080`, you would run:

```
python scanner.py -o 192.168.1.100 -p 80,443,8080
```

The tool will then initiate the port scanning process and display the results for each port, indicating whether it is open or closed.

Note: Make sure you have the necessary permissions to perform network scanning on the target host.

## Example Output

```
[&] 192.168.1.100 tcp/port 80 open
[&] 192.168.1.100 tcp/port 443 closed
[&] 192.168.1.100 tcp/port 8080 open
```

## Troubleshooting

If you encounter any issues or errors while running the tool, ensure that you have provided the correct command-line arguments in the correct format. The tool expects the `-o` or `--host` argument for the target host and the `-p` or `--port` argument for the list of ports to scan.

If you forgot to provide the command-line arguments, you will receive an error message prompting you to provide the necessary arguments.

If you still encounter any difficulties, please feel free to open an issue on the project's repository for further assistance.

## Disclaimer

This tool is provided for educational and ethical purposes only. You should only use it with the appropriate permissions on systems you own or have authorization to test. The authors are not responsible for any misuse or damage caused by this tool.
