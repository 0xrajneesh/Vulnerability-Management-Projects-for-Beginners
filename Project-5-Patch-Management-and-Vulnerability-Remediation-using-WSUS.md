# Project 5: Introduction to Patch Management and Vulnerability Remediation using WSUS

## Introduction
In this project, students will learn the basics of patch management and vulnerability remediation using WSUS (Windows Server Update Services). WSUS allows administrators to manage the distribution of updates released through Microsoft Update to computers in a corporate environment. By the end of this project, students will be able to set up WSUS, configure client machines, approve and deploy updates, and verify the update status.

## Pre-requisites
- Basic understanding of Windows Server and client management
- A Windows Server 2016 or later machine
- Windows client machines (e.g., Windows 10) for testing

## Lab Set-up and Tools
- Windows Server 2016 or later with WSUS role installed
- Windows client machines
- Active Directory for domain-joined machines (optional but recommended)

## Exercises

### Exercise 1: Installing and Configuring WSUS

**Steps:**

1. Open Server Manager on your Windows Server machine.
2. Click on "Manage" > "Add Roles and Features".
3. Follow the wizard to add the WSUS role:
    - Select "Windows Server Update Services".
    - Choose the required services and proceed with the installation.
4. After installation, launch the WSUS Configuration Wizard:
    - Configure the update source.
    - Choose the classifications and products you want to update.
    - Set up synchronization schedule.
    - Complete the wizard to finish configuration.

**Expected Output:**
- WSUS is installed and configured with the initial setup complete.

### Exercise 2: Configuring Group Policies for WSUS

**Steps:**

1. Open the Group Policy Management Console (GPMC) on your Windows Server.
2. Create a new Group Policy Object (GPO) or edit an existing one.
3. Navigate to "Computer Configuration" > "Policies" > "Administrative Templates" > "Windows Components" > "Windows Update".
4. Configure the following policies:
    - "Specify Intranet Microsoft update service location": Set it to the WSUS server URL (e.g., `http://wsusserver`).
    - "Configure Automatic Updates": Set it to auto-download and schedule the install.
5. Link the GPO to the desired organizational unit (OU) containing the client machines.

**Expected Output:**
- Group Policies are configured to direct client machines to use the WSUS server for updates.

### Exercise 3: Approving and Deploying Updates

**Steps:**

1. Open the WSUS console on your Windows Server.
2. Navigate to "Updates" > "All Updates".
3. Select the updates you want to approve for installation.
4. Right-click on the selected updates and choose "Approve".
5. Select the target computer groups and approve the updates for them.

**Expected Output:**
- Selected updates are approved for deployment to the specified computer groups.

### Exercise 4: Verifying Update Status on Client Machines

**Steps:**

1. On a client machine, open Command Prompt as an administrator.
2. Run the following command to force the client to check for updates:
    ```bash
    wuauclt /detectnow
    ```
3. Open Windows Update from the Control Panel or Settings and check for updates.
4. Verify that the updates approved in WSUS are listed and begin installing.

**Expected Output:**
- The client machine detects and installs updates as configured by the WSUS server.

### Exercise 5: Generating and Analyzing WSUS Reports

**Steps:**

1. Open the WSUS console on your Windows Server.
2. Navigate to "Reports" and select the desired report type (e.g., Update Status Summary).
3. Configure the report parameters and generate the report.
4. Analyze the report to review update compliance and identify any issues.

**Expected Output:**
- A detailed report showing the update status and compliance of client machines, helping to identify any pending or failed updates.

By completing these exercises, students will gain hands-on experience with WSUS for patch management and vulnerability remediation, including setting up the server, configuring clients, deploying updates, and analyzing update compliance.
