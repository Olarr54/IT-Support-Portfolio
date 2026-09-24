# Server Troubleshooting Case Studies

During my university server practicals, I came across several problems while setting up and testing Windows Server and Ubuntu Server.

These were useful because I had to investigate the problem rather than simply follow the setup instructions.

## Case Study 1 – Static IP Configuration

### Problem

My Ubuntu Server initially had a problem after I tried to configure a static IP address.

### What I checked

I used:

```bash
ip a

to check the current network information.

I then checked the Netplan configuration and compared the IP address, subnet and gateway with the VMware NAT network.

What I found

The network configuration did not match the VMware network settings correctly.

Fix

I corrected the network configuration and tested the connection again.

Result

The server was able to communicate correctly using the new configuration.

What I learned

This showed me the importance of checking the actual network configuration before making random changes. IP address, subnet and gateway settings all need to work together.

Case Study 2 – XAMPP Services Not Starting
Problem

While working with a PHP application, the Apache and MySQL services in XAMPP were not starting correctly.

What I checked

I looked at the error messages and considered possible causes such as:

Port conflicts
Permissions
Existing services using the required ports
Incorrect configuration
Investigation

I checked the configuration and logs to understand what was preventing the services from starting.

I then tried different configuration changes and tested the services again.

Result

I was eventually able to get the services running in the lab environment.

What I learned

This taught me not to immediately reinstall software when something goes wrong. Checking error messages and logs can give useful information about what is actually causing the problem.

Case Study 3 – PHP and MySQL Connection
Problem

I had an issue when testing a PHP application that connected to a MySQL database.

What I checked

I reviewed the PHP code and checked the database connection details.

What I found

There were coding errors including incorrect variable names and missing semicolons.

Fix

I corrected the errors and tested the PHP page again.

Result

The PHP application was able to connect to the database successfully.

What I learned

This showed me how small configuration or coding mistakes can cause an application to fail. It also reinforced the importance of checking the error and testing each part of a problem separately.

Case Study 4 – BitLocker in a Virtual Machine
Problem

I had difficulty enabling BitLocker on the Windows Server virtual machine because the VM did not have a compatible TPM available.

What I checked

I investigated the BitLocker requirements and looked at the relevant Windows Group Policy settings.

Fix

I changed the relevant Group Policy setting in the lab environment so that BitLocker could be enabled without a compatible TPM.

Result

I was able to continue testing BitLocker on the virtual machine.

What I learned

This was a good example of troubleshooting an issue caused by the environment rather than the software itself. It also showed me the importance of researching error messages and requirements before changing settings.

My Troubleshooting Approach

Across these problems, I found that a simple process worked well:

Understand what is not working
Check the error message or symptoms
Look at the relevant settings, logs or configuration
Identify the most likely cause
Make a controlled change
Test the result
Record what was changed

This is the approach I would use when investigating an IT support issue before deciding whether it needs to be escalated.