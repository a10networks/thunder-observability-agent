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
	
	More detailed description and sample configuration file, please check [/AWS, /AZURE, /VMWARE] directory.