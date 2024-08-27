<br>

<h1 align="center">Run Insecure Environment for 24 Hours & Capture Analytics</h1>

<br>

<p align="center">
<img width="900" src="https://github.com/user-attachments/assets/e874e594-c69f-439f-90e7-d588ba7841c8" alt="Banner"/>

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

>   <details close> 
>   
> **<summary> 📋 Steps to Edit the Maps:</summary>**
> 
> <br>
> 
> From inside the **Workbook** ➜ click on ✏️ **Edit** 
> 
> <br>
> 
> ![azure portal](https://github.com/user-attachments/assets/d42567b3-d717-466b-a98e-a7c98062dfa3)
> 
> <br>
> 
> Then go all the way down and to the right ➜ click the **↑ Edit** button
> 
> <br>
> 
> ![azure portal](https://github.com/user-attachments/assets/44ef059e-e7a7-48f4-b6de-1a6f63bb87ab)
> 
> <br>
> 
> Change the **Time Range** to ```Last 24 hours```
> 
> <br>
> 
> ![azure portal](https://github.com/user-attachments/assets/44ef059e-e7a7-48f4-b6de-1a6f63bb87ab)
> 
> <br>
> 
> Finally ➜ click 📒**Done Editing**
> 
> <br>
> 
> ![azure portal](https://github.com/user-attachments/assets/d70ed30f-7bde-4e90-8e45-c4e5ea86a2d0)
> 
> <br>
> 
>   </details>

<br>

<h2></h2>

<br>

### Windows RDP/SMB Authentication Failures:

<br>

![azure portal](https://github.com/user-attachments/assets/e892d644-b7ba-4f0a-b5b4-869a195a725c)

<br>

### Linux SSH Authentication Failures:

<br>

![azure portal](https://github.com/user-attachments/assets/04c1e583-c9b4-45d8-9ef1-cc91baf91b7f)

<br>

### MS SQL Server Authentication Failures:

<br>

![azure portal](https://github.com/user-attachments/assets/10d0922f-149a-4280-b0e8-7c1d4c0be0fc)

<br>

### NSG Allowed Malicious Inbound Flows:

<br>

![azure portal](https://github.com/user-attachments/assets/10d0922f-149a-4280-b0e8-7c1d4c0be0fc)

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

We'll go through the **Incident Response Lifecycle** ➜ remidiating problems that were found.

Then after that Incident Response stage ➜ we're going to further add more **Security Controls** to our Environment and harden it some more.

Then finally we'll take another 24 Hour' Snapshot of our Environment's Attack Metrics and make a comparison with the previous results.

<br />

<br />

<br />  

<br /> 

<br />

<br />  

<br /> 

<br />

<br />

 
