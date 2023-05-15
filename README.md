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
	- Provides multitasking capabilities to collect and process multiple Thunder instances simultaneously.
	- Installs on any orchestration platform such as public cloud compute instances, private cloud physical or virtual machines, 	hypervisor VMs, and on-premise physical hardware and is self-driven.
	- Supports Linux, CentOS, and Ubuntu platforms as a Python Plugin installation package and Docker containerization.
	- Supports single or multiple Thunder instances.
	- Supports Thunder instances running under AWS autoscale group or Azure Virtual machine scale set (VMSS).
	- Collects data from any type of Thunder device installed on public cloud compute instances, private cloud physical or virtual 	machines, hypervisor VMs and on-premise physical hardware installation.
	- Publishes data to Azure Cloud, AWS Cloud, and VMware ESXi.

### Supported Thunder vADC Performance Metrics
	1.  CPU Usage Percentage (Data).
	2.  Memory Usage Percentage.
	3.  Disk Usage Percentage.
	4.  Throughput Rate (Global/BPS)
	5.  Interface Down Count (Data)
	6.  Total New Connection (Per Sec)
	7.  Transactions Rate (Per Sec)
	8.  Server Down Count
	9.  Server Down Percentage
	10. SSL Errors Count
	11. Server Errors Count
	12. Total Session Count
	13. Packet Rate (per seconds) [Since ACOS 6.0.0]
	14. Packet Drop Rate (per seconds) [Since ACOS 6.0.0]
	    For detailed information, please refer [/TOA_100_USER_GUIDE.pdf] 

### Supported Thunder vADC Performance Logs
	- SysLogs.
	  For detailed information, please refer [/TOA_100_USER_GUIDE.pdf] 
	
### Supported Monitoring Platforms
	1. AWS.
	2. Azure.
	3. VMware.
	
### Supported Use Cases
	1. Monitoring thunder adc metrics or logs or both into AWS Cloudwatch.
	2. Monitoring thunder adc metrics or logs or both into Azure Application Insight and Log Analytics Workspace.
	3. Monitoring thunder adc metrics or logs or both into VMware vRealize Operations and Log Insight.


### Supported A10 Thunder ADC Versions
	64-bit Advanced Core OS (ACOS) version 6.0.0-p2, build 22.
	64-bit Advanced Core OS (ACOS) version 6.0.0-p1, build 47.
	64-bit Advanced Core OS (ACOS) version 5.2.1-P7, build 47.
	64-bit Advanced Core OS (ACOS) version 5.2.1-p6, build 74.
	64-bit Advanced Core OS (ACOS) version 5.2.1-p5, build 114.

### Supported Installation Options
	1. Python Plugin. [Online]
		pip install thunder-observability-agent
		
	2. Python Plugin. [offline].
		pip install thunder_observability_agent-1.0.0-py3-none-any.whl
		Download from [/dist]
		
	3. Docker Container [Kubernetes manifest].
		Download from [/dist/kubernetes]
	
	For detailed installation and configuration steps, please refer [/TOA_100_USER_GUIDE.pdf] 

### License 
	"THUNDER OBSERVABILITY AGENT END USER SOFTWARE LICENSE AGREEMENT"
	For more information please check [/LICENSE.pdf]
	
	All rights reserved @A10Networks Inc.

### Open Source Disclaimer
	For more information, please refer [/OPEN-SOURCE-DISCLAIMER.pdf]

### Examples
	For more information please refer [/examples]
	
### Support Subscription
	Please contact support@a10networks.com
	