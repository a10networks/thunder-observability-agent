# A10's Thunder Observability Agent (TOA) - v2.0.0
	The TOA is a lightweight autonomous data processing engine that can be externally installed and configured for any Thunder device.
	TOA offers the following capabilities on Application Delivery Controller (ADC):
	
	- Collects, processes, and publishes 14 Thunder metrics. 
 	  The default data collection frequency is 1 minute. Thunder metrics can be sent to the platform where Thunder is deployed, which includes AWS, Azure, and VMware or can be sent to shared platforms like Elasticsearch (Kibana), Prometheus (Grafana), and Splunk. Metrics can be sent to any one platform at a time. For more information on Thunder metrics, see Supported Thunder Metrics.
	
	- Collects, processes, and publishes Thunder Syslogs.
 	  The default data collection frequency is 1 minute. The logs can be published on various platforms like AWS, Azure, VMware, Kibana (Elasticsearch), Grafana (Prometheus and Pushgateway), or Splunk. 
	  Logs can be sent to any one platform at a time. For more information on Thunder logs, see Supported Thunder Logs.

	- Manages the data collection, processing, aggregation, and publishing internally.
	- Provides multitasking capabilities to collect and process multiple Thunder instances and its partitions simultaneously. Default it collects from shared partition.
	- TOA supports Shared and L3V partitions. The maximum number of partitions supported per Thunder is 20.
	- Installs on any orchestration platform such as public cloud compute instances, private cloud physical or virtual machines, 	hypervisor VMs, and on-premise physical hardware and is self-driven.
	- Installs on Linux, CentOS, and Ubuntu platforms as a Python Plugin installation package and Docker containerization.
	- Supports single or multiple Thunder instances.
	- Supports Thunder instances running under AWS autoscale group or Azure Virtual machine scale set (VMSS).
	- Collects data from any type of Thunder device installed on public cloud compute instances, private cloud physical or virtual 	machines, hypervisor VMs and on-premise physical hardware installation.
	- Publishes data to Azure Cloud, AWS Cloud, and VMware ESXi.

### Supported Use Cases
	1. Monitoring thunder adc metrics or logs or both into AWS Cloudwatch.
	2. Monitoring thunder adc metrics or logs or both into Azure Application Insight and Log Analytics Workspace.
	3. Monitoring thunder adc metrics or logs or both into VMware vRealize Operations and Log Insight.
	4. Monitoring thunder adc metrics or logs or both into Splunk Console.
	5. Monitoring thunder adc metrics or logs or both into ElasticSearch/Kibana Console.
	6. Monitoring thunder adc metrics or logs or both into Prometheus/Grafana Console using PushGateway.

### Supported Installation Options
	1. Python Plugin.
		pip install thunder-observability-agent
		
	2. Docker Container [Kubernetes manifest].
		Download from [/dist/kubernetes]
	
	For detailed installation and configuration please check documentation section.

### Documentation
<a href="https://documentation.a10networks.com/docs/Install/Software/thunder-observability-agent/">A10 TOA Documentation Site</a>.
	

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
	   
### Supported Thunder vADC Performance Logs
	- SysLogs.
	
### Supported Monitoring Platforms
	1. AWS.
	2. Azure.
	3. VMware.
	4. Splunk
	5. ElasticSearch-Kibana
	6. Prometheus-Grafana [PushGateway]

### Supported A10 Thunder ADC Versions
	64-bit Advanced Core OS (ACOS) version 6.0.2.
	64-bit Advanced Core OS (ACOS) version 6.0.1.
	64-bit Advanced Core OS (ACOS) version 6.0.0-P2-SP1.
	64-bit Advanced Core OS (ACOS) version 6.0.0-P1.
	64-bit Advanced Core OS (ACOS) version 5.2.1-P7.
	64-bit Advanced Core OS (ACOS) version 5.2.1-P6.
	64-bit Advanced Core OS (ACOS) version 5.2.1-P5.
	64-bit Advanced Core OS (ACOS) version 4.1.4-GR1.


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
	
	ElasticSearch:
	UC_01	: Collect metrics and logs from thunder/thunders and publish it into elasticsearch/kibana.
	UC_02	: Collect only logs of thunder/thunders and publish it into elasticsearch/kibana.
	UC_03	: Collect only metrics of thunder/thunders and publish it into elasticsearch/kibana.

	Prometheus/Grafana:
	UC_01	: Collect metrics and logs from thunder/thunders and publish it into prometheus/grafana using pushgateway.
	UC_02	: Collect only logs of thunder/thunders and publish it into prometheus/grafana using pushgateway.
	UC_03	: Collect only metrics of thunder/thunders and publish it into prometheus/grafana using pushgateway.

	Splunk:
	UC_01	: Collect metrics and logs from thunder/thunders and publish it into splunk.
	UC_02	: Collect only logs of thunder/thunders and publish it into splunk.
	UC_03	: Collect only metrics of thunder/thunders and publish it into splunk.

	For detail description and sample configuration files, please refer [/examples].
	
### Support Information
	Please contact support@a10networks.com with subject : "TOA Support Request"
