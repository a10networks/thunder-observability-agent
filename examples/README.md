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
	
	More detailed description and sample configuration file, please check [/AWS, /AZURE, /VMWARE, /ELASTICSEARCH, /PROMETHEUS, /SPLUNK] directory.