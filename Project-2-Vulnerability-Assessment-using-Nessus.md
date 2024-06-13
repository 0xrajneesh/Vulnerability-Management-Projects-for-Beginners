# Project 2: Basic Vulnerability Assessment using Nessus

## Introduction
In this project, students will learn the fundamentals of vulnerability assessment using Nessus, a widely-used vulnerability scanner. Nessus helps in identifying vulnerabilities, misconfigurations, and compliance issues in various systems and applications. By the end of this project, students will be able to install Nessus, perform vulnerability scans, and analyze scan results.

## Pre-requisites
- Basic understanding of network and system administration
- Familiarity with Linux command line
- A computer with a Linux-based operating system (preferably Ubuntu)
- Nessus Home or Professional license (Nessus Home is free for personal use)

## Lab Set-up and Tools
- Ubuntu 20.04 or later
- Nessus installed (instructions provided in the first task)
- A target machine for scanning (can be a local VM or a networked device)

## Exercises

### Exercise 1: Installing Nessus

**Steps:**

1. Download the Nessus installation package from the Tenable website:
    ```bash
    wget https://www.tenable.com/downloads/api/v1/public/pages/nessus/downloads/XXXX/download?i_agree_to_tenable_license_agreement=true
    ```
2. Install Nessus:
    ```bash
    sudo dpkg -i <name-of-downloaded-file>.deb
    ```
3. Start the Nessus service:
    ```bash
    sudo systemctl start nessusd
    ```
4. Enable Nessus to start on boot:
    ```bash
    sudo systemctl enable nessusd
    ```
5. Access the Nessus web interface by navigating to `https://<your-ip>:8834` in a web browser.

**Expected Output:**
- Nessus should be installed and running. You should be able to access the Nessus web interface and proceed with the initial setup.

### Exercise 2: Configuring Nessus for Scanning

**Steps:**

1. Log in to the Nessus web interface.
2. Complete the initial setup by creating an admin account and activating Nessus with the provided activation code.
3. Navigate to the "Settings" section to configure any necessary proxy settings or updates.

**Expected Output:**
- Nessus is configured and ready to create new scan policies and tasks.

### Exercise 3: Creating a Scan Policy

**Steps:**

1. In the Nessus web interface, navigate to the "Policies" section.
2. Click "New Policy" to create a new scan policy.
3. Choose a policy template that suits your needs (e.g., Basic Network Scan).
4. Configure the scan settings, such as scan name, description, and target preferences.
5. Save the policy.

**Expected Output:**
- A new scan policy is created and saved, ready to be used for scanning tasks.

### Exercise 4: Running a Vulnerability Scan

**Steps:**

1. In the Nessus web interface, navigate to the "Scans" section.
2. Click "New Scan" and select the previously created policy.
3. Enter the scan details, such as scan name and target IP address.
4. Save the scan and click "Launch" to start the scan.

**Expected Output:**
- Nessus starts scanning the configured target. You can monitor the scan progress and view preliminary results.

### Exercise 5: Analyzing Scan Results

**Steps:**

1. Once the scan is complete, navigate to the "Scans" section and click on the completed scan.
2. Review the scan results, paying attention to identified vulnerabilities, their severity, and suggested remediation steps.
3. Export the scan report in your preferred format (e.g., PDF, HTML).

**Expected Output:**
- A detailed report of the scan results, highlighting vulnerabilities, their severity, and suggested remediation actions.

By completing these exercises, students will gain hands-on experience in setting up and using Nessus for vulnerability assessment, creating scan policies, running scans, and interpreting scan results.
