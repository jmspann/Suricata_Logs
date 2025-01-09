<h1>Examine Alerts, Logs, & Rules with Suricata</h1>

<h2>Description</h2>
This lab will show how to examine alerts, logs, and rules using Suricata within a Linux command-line.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Linux Command-Line</b>

<h2>Environments Used </h2>

- <b>KALI LINUX</b>
- <b>Linux Bash Shell</b>
- <b>Suricata</b>

<h2>Program Walk-Through:</h2>

<p align="center">
First, we begin by examining the Suricata rule defined in the "custom.rules" file using the <em><strong>cat</strong></em> command: <br/>
<img src="https://i.imgur.com/dASuIDH.png" height="100%" width="100%" alt="Suricata Logs"/>
<br />
<br />
Next, we trigger the rule so we can examine the alert logs that Suricata generates. We can verify it ran successfully by comparing the number of files from before and after in the "suricata" subdirectory using <em><strong>ls</strong></em>:  <br/>
<img src="https://i.imgur.com/D6enynr.png" height="100%" width="100%" alt="Suricata Logs"/>
<br />
<br />
Now we examine the logs the Suricata rule generated, starting with the "fast.log": <br/>
<img src="https://i.imgur.com/x5S3jxI.png" height="100%" width="100%" alt="Suricata Logs"/>
<br />
<br />
For a more in-depth analysis of the data, open the "eve.json" file. Since this log file contains more information, we will use the <em><strong>jq</strong></em> command to display the entries in an improved format:  <br/>
<img src="https://i.imgur.com/d2WHcAW.png" height="100%" width="100%" alt="Suricata Logs"/>
<br />
<br />
Now we will use the <em><strong>jq</strong></em> command to extract specific event data: <br/>
<img src="https://i.imgur.com/EURgKuH.png" height="100%" width="100%" alt="Suricata Logs"/>
<br />
<br />
Finally, we will use the <em><strong>jq</strong></em> command to display all event logs related to a specific "flow_id" from the "eve.json" file: <br/>
<img src="https://i.imgur.com/y2lxvBv.png" height="100%" width="100%" alt="Suricata Logs"/>
</p>
<br />
<br />



