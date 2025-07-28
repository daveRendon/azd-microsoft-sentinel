[comment]: <> (please keep all comment items at the top of the markdown file)
[comment]: <> (please do not change the ***, as well as <div> placeholders for Note and Tip layout)
[comment]: <> (please keep the ### 1. and 2. titles as is for consistency across all demoguides)
[comment]: <> (section 1 provides a bullet list of resources + clarifying screenshots of the key resources details)
[comment]: <> (section 2 provides summarized step-by-step instructions on what to demo)


[comment]: <> (this is the section for the Note: item; please do not make any changes here)
***
### Microsoft Sentinel-based threat detection and response

<div style="background: lightgreen; 
            font-size: 14px; 
            color: black;
            padding: 5px; 
            border: 1px solid lightgray; 
            margin: 5px;">

**Note:** Below demo steps should be used **as a guideline** for doing your own demos. Please consider contributing to add additional demo steps.
</div>

[comment]: <> (this is the section for the Tip: item; consider adding a Tip, or remove the section between <div> and </div> if there is no tip)

***
### 1. What Resources are getting deployed

This scenario is aligned with the AZ-500 and AZ-104 path and provides a demo solution for creating a proof of concept of Microsoft Sentinel-based threat detection and response.

Specifically, you want to:

    - Start collecting data from Azure Activity and Microsoft Defender for Cloud.
    - Add built in and custom alerts
    - Review how Playbooks can be used to automate a response to an incident.

Resources deployed: 
# Azure Deployment Resources

## Core Resources

- **myVM/Microsoft.Insights.LogAnalyticsAgent** – VM extension  
- **myVM** – Virtual machine  
- **defenderForCloud** – Deployment  
- **myVMNic** – Network interface  
- **Change-Incident-Severity** – Logic app  
- **default** – Onboarding state  
- **myVnet** – Virtual network  
- **myPublicIpAddress** – Public IP address  
- **myNetworkSecurityGroup** – Network security group  
- **bootdiagsh7n2tj4ueici4** – Storage account  
- **la-h7n2tj4ueici4** – Log Analytics workspace  

## Data Connectors & Metadata

- **la-h7n2tj4ueici4/Microsoft.SecurityInsights/DataConnector-AzureActivity** – Data connector  
- **la-h7n2tj4ueici4/Microsoft.SecurityInsights/AzureActivity** – Data connector  
- **la-h7n2tj4ueici4/Microsoft.SecurityInsights/azuresentinel.azure-sentinel-solution-azureactivity** – Metadata  

## Template Specs

- **la-h7n2tj4ueici4-ar-lmwaof3kln4wk/2.0.1** – Template spec version  
- **la-h7n2tj4ueici4-ar-v67aq7vdjtczq/2.0.1** – Template spec version  
- **la-h7n2tj4ueici4-ar-v5rhyk3h6pxwk/2.0.1** – Template spec version  
- **la-h7n2tj4ueici4-hq-fsojx54ezfdwo/2.0.1** – Template spec version  
- **la-h7n2tj4ueici4-ar-bnvb76yc4fdau/2.0.1** – Template spec version  
- **la-h7n2tj4ueici4-ar-ovcreldn7vto2/2.0.1** – Template spec version  
- **la-h7n2tj4ueici4-hq-kdpt4vcacji66/2.0.1** – Template spec version  
- **la-h7n2tj4ueici4-hq-czyhwqivemswq/2.1.1** – Template spec version  
- **la-h7n2tj4ueici4-ar-ey4wtj45eauem/2.0.2** – Template spec version  
- **la-h7n2tj4ueici4-ar-dhepd4eos4ilo/2.0.1** – Template spec version  
- **la-h7n2tj4ueici4-ar-cttbia5pka7b4/2.0.2** – Template spec version  
- **la-h7n2tj4ueici4-hq-6fgmete7aooi2** – Template spec  
- **la-h7n2tj4ueici4-hq-3w37ere3gvu7a** – Template spec  
- **la-h7n2tj4ueici4-wb-s7vgun75224nu** – Template spec  
- **la-h7n2tj4ueici4-hq-z3vpeo7labby4** – Template spec  
- **la-h7n2tj4ueici4-ar-vty5azbprowmm** – Template spec  
- **la-h7n2tj4ueici4-hq-h4qz7a4mb7ljm** – Template spec  
- **la-h7n2tj4ueici4-ar-wcz5esg7vtkty** – Template spec  
- **la-h7n2tj4ueici4-hq-j53s3fu7tmdgu** – Template spec  
- **la-h7n2tj4ueici4-hq-7h4klcenjgjtg** – Template spec  
- **la-h7n2tj4ueici4-hq-4t7ut2nt6k7h4** – Template spec  
- **la-h7n2tj4ueici4-ar-dicyiuovdz66s** – Template spec  
- **la-h7n2tj4ueici4-hq-3etwoyq3c3ucs** – Template spec  
- **la-h7n2tj4ueici4-dc-3ioisqemr5xww** – Template spec  
- **la-h7n2tj4ueici4-ar-p66gqdzh4x3nq** – Template spec  
- **la-h7n2tj4ueici4-hq-lgww4qn2xwlai** – Template spec  
- **la-h7n2tj4ueici4-hq-6ht2oyqbc63pu** – Template spec  
- **la-h7n2tj4ueici4-hq-tvfmu6ffuyuwg** – Template spec  

## Duplicate or Repeated Entries (if applicable)

- **la-h7n2tj4ueici4** – Log Analytics workspace *(duplicate)*  
- **bootdiagsh7n2tj4ueici4** – Storage account *(duplicate)*  
- **la-h7n2tj4ueici4-ar-lmwaof3kln4wk** – Template spec *(duplicate of versioned entry)*  
- **la-h7n2tj4ueici4-ar-v67aq7vdjtczq** – Template spec *(duplicate of versioned entry)*  
- **la-h7n2tj4ueici4-ar-bnvb76yc4fdau** – Template spec *(duplicate of versioned entry)*  
- **la-h7n2tj4ueici4-ar-ovcreldn7vto2** – Template spec *(duplicate of versioned entry)*  
- **la-h7n2tj4ueici4-ar-ey4wtj45eauem** – Template spec *(duplicate of versioned entry)*  
- **la-h7n2tj4ueici4-ar-dhepd4eos4ilo** – Template spec *(duplicate of versioned entry)*  
- **la-h7n2tj4ueici4-ar-cttbia5pka7b4** – Template spec *(duplicate of versioned entry)*  
- **la-h7n2tj4ueici4-hq-kdpt4vcacji66** – Template spec *(duplicate of versioned entry)*  
- **la-h7n2tj4ueici4-hq-fsojx54ezfdwo** – Template spec *(duplicate of versioned entry)*  
- **la-h7n2tj4ueici4-hq-czyhwqivemswq** – Template spec *(duplicate of versioned entry)*  
- **la-h7n2tj4ueici4-ar-v5rhyk3h6pxwk** – Template spec *(duplicate of versioned entry)*  


<img src="https://raw.githubusercontent.com/daverendon/azd-microsoft-sentinel/refs/heads/main/demoguide/rg-microsoft-sentinel.png" alt="Intersite connectivity" style="width:70%;">
<br></br>
<br></br>



### 2. What can I demo from this scenario after deployment

<img src="https://raw.githubusercontent.com/daverendon/azd-microsoft-sentinel/refs/heads/main/demoguide/azd-microsoft-sentinel-diagram.png" alt="Microsoft Sentinel diagram" style="width:70%;">
<br></br>
<br></br>

Once you deploy the environment, you should be able to:

Task 1: Validate the Microsoft Sentinel configuration
Task 2: Validate the connection of Azure Activity to Sentinel
Task 3: Validate the rule that uses the Azure Activity data connector.
Task 4: Review the playbook
Task 5: Manage custom alerts and configure the playbook as an automated response.
Task 6: Invoke an incident and review the associated actions.


[comment]: <> (this is the closing section of the demo steps. Please do not change anything here to keep the layout consistant with the other demoguides.)
<br></br>
***
<div style="background: lightgray; 
            font-size: 14px; 
            color: black;
            padding: 5px; 
            border: 1px solid lightgray; 
            margin: 5px;">

**Note:** This is the end of the current demo guide instructions.
</div>