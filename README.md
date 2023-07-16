# CRAA-HTML-EC2 Repository

This repository contains a Bash script to set up an Apache web server on an EC2 instance running Amazon Linux. The script will update the system, install Apache (httpd), and deploy a web application from a remote ZIP archive.

## Prerequisites

Before running the script, ensure you have the following:

1. An EC2 instance running Amazon Linux.
2. Appropriate permissions to execute the script and install packages (sudo access).

## Usage

Follow these steps to use the script:

1. **Clone the Repository**: Clone this repository to your EC2 instance using the following command:

   ```bash
   git clone https://github.com/ndefrutitus/CRAA-HTML-EC2.git
   ```

2. **Run the Script**: Change directory to the repository and execute the script using the following command:

   ```bash
   cd CRAA-HTML-EC2
   chmod +x setup_apache.sh
   ./setup_apache.sh
   ```

   The script will prompt you for the sudo password as it requires elevated privileges to install Apache and perform other system-related tasks.

3. **Sit Back and Relax**: The script will automatically update the system, install Apache (httpd), download a ZIP archive from a specified URL, extract its contents, and copy the web application files to the appropriate directory.

4. **Verify the Web Application**: Once the script has completed its execution, you should be able to access your web application using the public IP address or DNS name of your EC2 instance in a web browser.

## Important Notes

1. The script uses `sudo su` at the beginning to switch to the root user. This may not be the most secure approach, and it's recommended to use individual `sudo` commands for the required tasks.

2. The script assumes that the ZIP archive (`mole.zip`) containing the web application files is available at the specified URL. Make sure the URL is correct and accessible.

3. This script is specifically designed for Amazon Linux. If you are using a different Linux distribution or operating system, the commands may not work as intended.

4. Make sure to review and understand the script's content before executing it on your production environment, as it involves system-level changes.

