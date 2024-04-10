<h1>Building-a-SOC-Honeynet-in-Azure<h1 />


<h2>Description</h2>
In this project, I simulate a small-scale honeynet that attracts real-world traffic from attackers around the world through Microsoft Azure. The goal throughout this project is to demonstrate best security practices, incident response tactics, and the effects of hardening your environment. We'll accomplish this by intentionally deploying virtual machines that have no safeguard from the public internet to attract attackers into our environment. Then after ingesting some log sources into Log Analytics Workspace, Microsoft Sentinel will come in to create attack maps, alerts, and incidents. In order to showcase metrics before and after hardening the environment based off the incidents generated from the 24 hour capture.

<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Diskpart</b>

<h2>Components used in Lab </h2>

- <b>Microsoft Defender for Cloud</b>
- <b>Azure Storage Account</b>
- <b>Microsoft Sentinel</b>
- <b>Azure Virtual Network</b>
- <b>Virtual Machines (2xWindows, 1xLinux)</b>
- <b>Azure Network Security Group</b>
- <b>Azure Storage Account</b>


<h2>Architecture of Lab</h2>

<p align="center">
Launch the utility: <br/>
<img width="842" alt="Screenshot 2024-04-10 at 9 12 24 AM" src="https://github.com/tico15/Building-a-SOC-Honeynet-in-Azure/assets/166507731/8204fff4-47fc-4ad4-87c3-f030a962d36e">

<h2>Run Insecure Environment for 24 Hours and Capture Analytics</h2>
<b>In the "BEFORE" stage of the project, all resources were initially deployed with the hope that attraction would be gained from the public internet. The Virtual Machines had both their Network Security Groups (NSGs) and built-in firewalls wide open, allowing unrestricted access from any source. Additionally, all other resources, such as storage accounts and databases, were deployed with public endpoints visible to the internet, without utilizing any Private Endpoints for added security. These machines were then left to the public for 24 hours to generate the following attack maps mentioned earlier.<br />
<h2>Attack Maps BEFORE HARDENING SECURITY CONTROLS</h2>
<img src="https://github.com/tico15/Building-a-SOC-Honeynet-in-Azure/assets/166507731/5f195f9b-b132-4468-bce4-8a092e0e24ff"
<br />
<img src="https://github.com/tico15/Building-a-SOC-Honeynet-in-Azure/assets/166507731/148e63ff-d7c3-4686-ae44-350eb180d043"
<br />
<img src="https://github.com/tico15/Building-a-SOC-Honeynet-in-Azure/assets/166507731/53b1bbb4-4e47-4bae-b288-d33583612ee0"
<br />
<img src="https://github.com/tico15/Building-a-SOC-Honeynet-in-Azure/assets/166507731/cc7f3adb-6f49-4064-9518-62b7fe7d25ab"
<br/>
<h2>HARDENING STEPS</h2>
<b>The initial 24-hour study revealed that the lab was vulnerable to multiple threats due to its visibility on the public internet. To address these findings, I activated NIST SP 800-53 r4 within the compliance section of Microsoft Defender and focused on fulfilling the compliance standards associated with SC.7.*. Additional assessments for SC-7 - Boundary Protection.<br />
<h2>Attack Maps AFTER Hardening / Security Controls</h2>
<b>There were no results to display for the 24-hour repeat map queries following the hardening of the assets.<br />
<h2>CONCLUSION</h2>
<b>In this project, a mini honeynet was constructed in Microsoft Azure and log sources were integrated into a Log Analytics workspace. Microsoft Sentinel was employed to trigger alerts and create incidents based on the ingested logs. Additionally, metrics were measured in the insecure environment before security controls were applied, and then again after implementing security measures. The significant reduction in security events and incidents following the implementation of security controls highlights their effectiveness in safeguarding the environment.<br />
<h2>DATA OF BEFORE AND AFTER SECURING ENVIROMENT</h2>
<img src="https://github.com/tico15/Building-a-SOC-Honeynet-in-Azure/assets/166507731/a06addb5-382d-4123-9975-7391f9dc3876"
<br />
