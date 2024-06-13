# Project 1: Introduction to Network Vulnerability Scanning with OpenVAS

## Introduction
In this project, students will learn the basics of network vulnerability scanning using OpenVAS (Open Vulnerability Assessment System). OpenVAS is a comprehensive open-source framework that helps identify security vulnerabilities in networked systems. By the end of this project, students will be able to set up OpenVAS, perform basic scans, and interpret scan results.

## Pre-requisites
- Basic knowledge of networking concepts
- Familiarity with Linux command line
- A computer with a Linux-based operating system (preferably Ubuntu)

## Lab Set-up and Tools
- Ubuntu 20.04 or later
- OpenVAS installed (instructions provided in the first task)
- A target machine for scanning (can be a local VM or a networked device)

## Exercises

### Exercise 1: Installing OpenVAS

**Steps:**

1. Update the system packages:
    ```bash
    sudo apt update
    sudo apt upgrade -y
    ```
2. Add the OpenVAS repository:
    ```bash
    sudo add-apt-repository ppa:mrazavi/openvas
    ```
3. Install OpenVAS:
    ```bash
    sudo apt update
    sudo apt install openvas -y
    ```
4. Initialize OpenVAS setup:
    ```bash
    sudo gvm-setup
    ```
5. Start the OpenVAS services:
    ```bash
    sudo gvm-start
    ```

**Expected Output:**
- OpenVAS should be installed and running. Access the OpenVAS web interface at `https://<your-ip>:9392` with the default admin credentials provided during setup.

### Exercise 2: Configuring OpenVAS for Scanning

**Steps:**

1. Log in to the OpenVAS web interface.
2. Navigate to the "Configuration" section and select "Targets".
3. Click "New Target" to create a new scan target.
4. Enter the target details (e.g., target name and IP address).
5. Save the new target configuration.

**Expected Output:**
- A new scan target is configured and ready for scanning.

### Exercise 3: Performing a Basic Network Scan

**Steps:**

1. In the OpenVAS web interface, go to the "Scans" section and select "Tasks".
2. Click "New Task" to create a new scan task.
3. Fill in the task details, selecting the previously created target.
4. Save the task and start the scan.

**Expected Output:**
- OpenVAS starts scanning the configured target. You can monitor the scan progress in the "Tasks" section.

### Exercise 4: Reviewing Scan Results

**Steps:**

1. Once the scan is complete, navigate to the "Scans" section and select "Reports".
2. Click on the report corresponding to the completed scan task.
3. Review the scan results, focusing on identified vulnerabilities and their severity.

**Expected Output:**
- A detailed report of the scan results, highlighting vulnerabilities, their severity, and possible remediation steps.

### Exercise 5: Remediating Identified Vulnerabilities

**Steps:**

1. Based on the scan report, identify high-severity vulnerabilities.
2. Research and implement remediation steps for the identified vulnerabilities (e.g., applying patches, configuring firewalls).
3. Re-scan the target to verify that vulnerabilities have been mitigated.

**Expected Output:**
- The target system shows reduced or no high-severity vulnerabilities upon re-scanning, indicating successful remediation.

By completing these exercises, students will gain hands-on experience in setting up and using OpenVAS for network vulnerability scanning, understanding scan results, and taking steps to remediate identified vulnerabilities.
