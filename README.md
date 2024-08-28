<br>

<h1 align="center">Run Insecure Environment for 24 Hours & Capture Analytics</h1>

<br>

<p align="center">
<img width="900" src="https://github.com/user-attachments/assets/37b10453-47fd-4fda-a40e-7423207e809d" alt="Banner"/>

<br>

<br>

<br>

  <details close> 
  
**<summary> 📝 Context</summary>**

<br>

The next thing we're going to do is just let our Environment sit as it is right now ➜ with everything Running in an Insecure Way.

We're going to let it run like that for 24 hours.

And then we'll come back after a day and **Take a Snapshot of the last 24 hours**.

We're going to record how many of the following Logs we had in the last 24 hours:

- ```SecurityEvent```
- ```Syslog```
- ```SecurityAlert```
- ```SecurityIncident```
- ```AzureNetworkAnalytics_CL```

<br>

After that,we'll start addressing a few of the Incidents and Lockdown our Environment quite a bit.

We'll do this by Practicing Security and **Implementing Security Controls**.

Finally, when our Environment is sufficiently Secured ➜ we're going to wait another 24 Hours and **Take another Snapshot then**.

We'll compare the 2 Environments to show what impact **Implementing Security Control** can had in our Environment.

<br>

<h2></h2>

<br>

  </details>

<br>


The goal now is to **Expose our Environment to Malicious Traffic for 24 hours** in order to **Build 4 Attack Maps for**:

> 🔹 Failed Authentication against **Windows WMs** (RDP / SMB / General Authentication Failures)
> 
> 🔹 Failed Authentication against **Linux VM** (SSH)
> 
> 🔹 Failed Authentication to the **Microsoft SQL Server** (inside our Windows VM)
>
> 🔹 Malicious Inbound Flows for the **Network Security Groups**
> 
> 

<br>

<h2></h2>

<br>

<br>

💡 The Following Table shows the Measurements taken from the Insecure Environment after the Initial 24 Hour' Observation Period:

<br>

### ➡️ Metrics BEFORE Securing our Environment

<br>

| Metric                   | Count
| ------------------------ | -----
| SecurityEvent (Windows VM)            | 19470
| Syslog (Linux VM)                   | 3028
| SecurityAlert (Microsoft Defender for Cloud)            | 10
| SecurityIncident (Sentinel Incidents)        | 348
| NSG Inbound Malicious Flows Allowed | 843

<br>

<h2></h2>

<br>

### ➡️ Attack Maps BEFORE Hardening / Security Controls

<br>

> We're now going to take some **Screenshots of the Attack Maps** we made earlier.
> 
> We'll be able to see what the Maps look like **BEFORE** and **AFTER** we **Implement the Security Controls** and tighten down our Environment.

<br>

Before taking the screenshots ➜ the Workbooks need to be edited to only show the **Last 24 hours**.

💡 The query runs over the last 30 days by default.

<br>

<br>

  <details close> 
  
**<summary> 📋 Steps to Edit the Maps:</summary>**

<br>

From inside the **Workbook** ➜ click on ✏️ **Edit** 

<br>

![azure portal](https://github.com/user-attachments/assets/36767f16-0a49-440e-8066-ea319c615747)

<br>

Then go all the way down and to the right ➜ click the **↑ Edit** button

<br>

![azure portal](https://github.com/user-attachments/assets/443caeaf-db8d-4d16-8358-446bbdf4ae70)

<br>

Change the **Time Range** to ```Last 24 hours```

<br>

![azure portal](https://github.com/user-attachments/assets/94e279f2-ad4d-42bb-ba73-5742b514ed57)

<br>

Finally ➜ click 📒**Done Editing**

<br>

![azure portal](https://github.com/user-attachments/assets/ff74b033-73a4-4548-b537-2853b1b360e9)

<br>

  </details>

<br>

<h2></h2>

<br>

### Windows RDP/SMB Authentication Failures:

<br>

![azure portal](https://github.com/user-attachments/assets/0a35fc4e-2760-4cfa-b34b-bedd77a3cf66)

<br>

### Linux SSH Authentication Failures:

<br>

![azure portal](https://github.com/user-attachments/assets/f2961c42-8b07-40d2-abe3-795dca6fee1e)

<br>

### MS SQL Server Authentication Failures:

<br>

![azure portal](https://github.com/user-attachments/assets/1ab74199-8102-4652-9b00-d8bd7883338e)

<br>

### NSG Allowed Malicious Inbound Flows:

<br>

![azure portal](https://github.com/user-attachments/assets/c3608c90-3819-45b3-815d-b90426343367)

<br>

  </details>

<h2></h2>

<br>

<br>

<br>

<br>

# Summary

<br>

In the next Lab we're going to start **Working the Incidents** and **Securing our Environment**.

We'll go through the **Incident Response Lifecycle** ➜ remediating problems that were found.

After that Incident Response phase ➜ we'll add more **Security Controls** to our Environment and harden it some more.

Finally we'll take another 24 Hour' Snapshot of our Environment's Attack Metrics and make a comparison with the previous results.

<br />

<br />

<br />  

<br /> 

<br />

<br />  

<br /> 

<br />

<br />

 
