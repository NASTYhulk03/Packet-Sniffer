# Packet Sniffer

## Description
Packet Sniffer is a network traffic analyzer that captures and analyzes network packets in real-time. This tool is designed to help network administrators and security professionals monitor and diagnose network issues, as well as detect potential security threats. The sniffer supports capturing packets from multiple network interfaces and can output detailed packet data for further analysis.

## Running the Application

### Development Mode
To run the Packet Sniffer in development mode, follow these steps:

1. Clone the repository:
    ```sh
    git clone https://github.com/EONRaider/Packet-Sniffer.git
    cd Packet-Sniffer
    ```

2. Install the dependencies:
    ```sh
    pip install -r requirements.txt
    # or
    poetry install
    ```

3. Execute the `sniffer.py` file with administrative privileges:
    ```sh
    sudo python3 packet_sniffer/sniffer.py
    ```

> **Note:** The `sudo` command is required due to the use of `socket.SOCK_RAW`, which needs administrative privileges to run on GNU/Linux. Ensure you are using the interpreter from your virtual environment (if applicable) rather than the system interpreter.

### Optional: Build the Binary
You can compile your own binary using the `build.py` file with the PyInstaller package. Dependency management works with both Poetry (recommended) and Virtualenv.

1. Install dependencies (as shown in Development Mode, Step 2).

2. Build the binary:
    ```sh
    python3 build.py
    ```

## Usage
To use the Packet Sniffer, run the `sniffer.py` script with the following options:

```sh
sniffer.py [-h] [-i INTERFACE] [-d]
