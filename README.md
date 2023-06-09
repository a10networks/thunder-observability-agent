# A10's Thunder Observability Agent (TOA) - v1.0.0
	The TOA is a lightweight autonomous data processing engine that can be externally installed and configured for any Thunder device.
	TOA offers the following capabilities on Application Delivery Controller (ADC):
	
	- Collects, processes and publishes fourteen Thunder metrics. 
	  The default data collection frequency is 1 minute. 
	  The metrics can be published on the same platform where the Thunder instance is deployed.
	  For more information on Thunder metrics, see Thunder Metric Support.
	
	- Collects, processes, and publishes Thunder Syslogs. 
	  The default data collection frequency is 1 minute. 
	  The logs can be published on the same platform where the Thunder instance is deployed. 
	  Additionally, logs can also be sent to any AWS, Azure, or VMware platforms.
	  
	- Manages the data collection, processing, aggregation, and publishing internally.
	- Provides multitasking capabilities to collect and process multiple Thunder instances and its partitions simultaneously. Default it collects from shared partition.
	- Installs on any orchestration platform such as public cloud compute instances, private cloud physical or virtual machines, 	hypervisor VMs, and on-premise physical hardware and is self-driven.
	- Supports Linux, CentOS, and Ubuntu platforms as a Python Plugin installation package and Docker containerization.
	- Supports single or multiple Thunder instances.
	- Supports Thunder instances running under AWS autoscale group or Azure Virtual machine scale set (VMSS).
	- Collects data from any type of Thunder device installed on public cloud compute instances, private cloud physical or virtual 	machines, hypervisor VMs and on-premise physical hardware installation.
	- Publishes data to Azure Cloud, AWS Cloud, and VMware ESXi.

### Supported Use Cases
	1. Monitoring thunder adc metrics or logs or both into AWS Cloudwatch.
	2. Monitoring thunder adc metrics or logs or both into Azure Application Insight and Log Analytics Workspace.
	3. Monitoring thunder adc metrics or logs or both into VMware vRealize Operations and Log Insight.

### Supported Installation Options
	1. Python Plugin.
		pip install thunder-observability-agent
		
	2. Docker Container [Kubernetes manifest].
		Download from [/dist/kubernetes]
	
	For detailed installation and configuration steps, please refer [/TOA_100_USER_GUIDE.pdf] 
	
### Supported Thunder vADC Performance Metrics
	1.  CPU Usage Percentage (Data).
	2.  Memory Usage Percentage.
	3.  Disk Usage Percentage.
	4.  Throughput Rate (Global/BPS)
	5.  Interface Down Count (Data)
	6.  Total New Connection (Sec)
	7.  Transactions Rate (Sec)
	8.  Server Down Count
	9.  Server Down Percentage
	10. SSL Errors Count
	11. Server Errors Count
	12. Total Session Count
	13. Packet Rate (Sec) [Since ACOS 5.2.1-P7+]
	14. Packet Drop Rate (Sec) [Since ACOS 5.2.1-P7+]
	    For detailed information, please refer [/TOA_100_USER_GUIDE.pdf] 

### Supported Thunder vADC Performance Logs
	- SysLogs.
	  For detailed information, please refer [/TOA_100_USER_GUIDE.pdf] 
	
### Supported Monitoring Platforms
	1. AWS.
	2. Azure.
	3. VMware.

### Supported A10 Thunder ADC Versions
	64-bit Advanced Core OS (ACOS) version 6.0.0-P2-SP1, build 6.
	64-bit Advanced Core OS (ACOS) version 6.0.0-P1,     build 47.
	64-bit Advanced Core OS (ACOS) version 5.2.1-P7,     build 160.
	64-bit Advanced Core OS (ACOS) version 5.2.1-P6,     build 74.
	64-bit Advanced Core OS (ACOS) version 5.2.1-P5,     build 114.
	64-bit Advanced Core OS (ACOS) version 4.1.4-GR1,    build 34

### Documentation
	A10 Documentation Site: https://documentation.a10networks.com

### License 
<a href="https://www.a10networks.com/wp-content/uploads/EULA_Thunder_Observability_Agent.pdf">THUNDER OBSERVABILITY AGENT END USER SOFTWARE LICENSE AGREEMENT</a>.

All rights reserved @A10 Networks Inc.

### Open Source Disclaimer
	For more information, please refer [/OPEN-SOURCE-DISCLAIMER.pdf]

### Examples
	
	VMware	Platform: 
	UC_01	  Collect metrics and logs from thunder/thunders running in vmware environment and publish it into vmware-vrops and vmware-vrli.
	UC_02	: Collect logs from thunder/thunders running in vmware environment and publish it into vmware-vrli.
	UC_03	: Collect metrics from thunder/thunders running in vmware environment and publish it into vmware-vrops.
	UC_04	: Collect logs from thunder/thunders running in vmware environment and publish it into aws-cloudwatch.
	UC_05	: Collect logs from thunder/thunders running in vmware environment and publish it into azure-log-workspace.
	
	Azure Cloud:
	UC_01	: Collect metrics and logs from thunder/thunders running in azure environment and publish it into azure-application-insights and azure-log-analytics-workspace.
	UC_02	: Collect logs from thunder/thunders running in azure environment and publish it into azure-log-analytics-workspace.
	UC_03	: Collect metrics from thunder/thunders running in azure environment and publish it into azure-application-insights.
	UC_04	: Collect logs from thunder/thunders running in azure environment and publish it into vmware-vrli.
	UC_05	: Collect logs from thunder/thunders running in azure environment and publish it into aws-cloudwatch.
	  
	AWS Cloud:	 
	UC_01	: Collect metrics and logs from thunder/thunders running in aws environment and publish it into aws-cloudwatch.
	UC_02	: Collect only logs of thunder/thunders running in aws environment and publish it into aws-cloudwatch.
	UC_03	: Collect only metrics of thunder/thunders running in aws environment and publish it into aws-cloudwatch.
	UC_04	: Collect only logs of thunder/thunders running in aws environment and publish it into vmware-vrli.
	UC_05	: Collect only logs of thunder/thunders running in aws environment and publish it into azure-log-analytics-workspace.
	
	For detail description and sample configuration files, please refer [/examples].
	
### Support Subscription
	Please contact support@a10networks.com