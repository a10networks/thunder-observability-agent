# SPLUNK EXAMPLE USE-CASES

## UC_01 - COLLECT_LOG_METRIC_FROM_THUNDER_&_PUBLISH_IN_SPLUNK
    - Use Cases : 01
    - Scenario  : Collect metrics and logs from thunder/thunders and publish it into splunk.
    
    - Description : Borse Inc is regular a10 client. Company purchased an instance of thunder long back and deployed it on some cloud platform,
    
         This instance is configured as ADC server load balancer for there gaming applications named [Pokers and Football]
         and from past few months company is getting timeout/fail-over complain from there online gaming customers. 
         These generally happened on occasions/event/festival/holidays due to high traffic load on thunder.
         Company wants a standard way to monitor all 14 metrics and logs generated by a thunder on Splunk.
         Also want to get email alert notifications when aggregated cpu usage crosses 75% threshold value so that proper 
         action can be taken on time.
      
    - Company has some shared environment with some hardware space leftover with below information:
        - Linux Environment IP : 10.22.32.51
        - Hardware 			: 2GB RAM, 1CPU, 4GB memory.
    
    - Company has below thunder environment details:
        - Thunder IP: 10.22.32.01
        - User Name : Online_Pokers_TH
        - Password : Thunder@Borse@3201
        - Resource_Id : 09611d51-9534-4f78-b3a1-fe7262152e37
        
    - Company has below Splunk monitoring solution details:
        - splunk_host : "10.64.25.143:8088"
    
    - Company has shared Splunk credentials
        - token_log=8d189d83-a370-418d-a201-fb779c7b77ca
        - token_metrics=cee5368e-d53f-4771-84d7-022b3b033f43
    
    - Solution : A10 support team suggested to install 'Thunder Observability Agent[TOA]' within a cloud platform.
        It's pretty straight forward and super easy.
    
    - Configure TOA:
        - /usr/toaenv/thunder-observability-agent/config.json  
    
          {
            "splunk_provider": 1,
            "splunk_metric": 1,
            "splunk_cpu": 1,
            "splunk_memory": 1,
            "splunk_disk": 1,
            "splunk_throughput": 1,
            "splunk_interfaces": 1,
            "splunk_cps": 1,
            "splunk_tps": 1,
            "splunk_server_down_count": 1,
            "splunk_server_down_percentage": 1,
            "splunk_ssl_cert": 1,
            "splunk_server_error": 1,
            "splunk_sessions": 1,
            "splunk_packet_rate": 1,
            "splunk_packet_drop": 1,
            "splunk_log": 1,
            "splunk_host": "10.64.25.143:8088"
          }
    
       - /root/.thunder/credentials  
         
          {
              "autoscale" : 0,
              "provider" : "",
              "thunders": [
                {
                  "ip": "10.22.32.01",
                  "username": "Online_Pokers_TH",
                  "password": "Thunder@Borse@3201",
                  "resource_id": "09611d51-9534-4f78-b3a1-fe7262152e37",
                  "active_partitions": "POKERS,FOOTBALL"
                }
              ]
          }
    
    
     - /root/.splunk/credentials
        
        token_log=8d189d83-a370-418d-a201-fb779c7b77ca
        token_metrics=cee5368e-d53f-4771-84d7-022b3b033f43
    
    -- All Set ---
    
    Check Logs : /var/logs/thunder-observability-agent/agent.log

## UC_02 - COLLECT_ONLY_LOG_FROM_THUNDER_&_PUBLISH_IN_SPLUNK
    - Use Cases : 02
    - Scenario  : Collect logs from thunder/thunders and publish it into splunk.
    
    - Description : Borse Inc is regular a10 client. Company purchased an instance of thunder long back and deployed it on some cloud platform,
         This instance is configured as ADC server load balancer for there gaming applications named [Pokers and Football]
         and from past few months company is getting timeout/fail-over complain from there online gaming customers. 
         These generally happened on occasions/event/festival/holidays due to high traffic load on thunder.
         Company wants a standard way to monitor logs generated by a thunder on Splunk.
                 
    - Company has some shared environment with some hardware space leftover with below information:
        - Linux Environment IP : 10.22.32.51
        - Hardware 			: 2GB RAM, 1CPU, 4GB memory.
    
    - Company has below thunder environment details:
        - Thunder IP: 10.22.32.01
        - User Name : Online_Pokers_TH
        - Password : Thunder@Borse@3201
        - Resource_Id : 09611d51-9534-4f78-b3a1-fe7262152e37
        
    - Company has below Splunk monitoring solution details:
        - splunk_host : "10.64.25.143:8088"
    
    - Company has shared Splunk credentials
        - token_log=8d189d83-a370-418d-a201-fb779c7b77ca
        - token_metrics=cee5368e-d53f-4771-84d7-022b3b033f43
    
    - Solution : A10 support team suggested to install 'Thunder Observability Agent[TOA]' within a cloud platform.
        It's pretty straight forward and super easy.
    
    - Configure TOA:
        - /usr/toaenv/thunder-observability-agent/config.json  
    
          {
            "splunk_provider": 1,
            "splunk_log": 1,
            "splunk_host": "10.64.25.143:8088"
          }
    
       - /root/.thunder/credentials  
         
          {
              "autoscale" : 0,
              "provider" : "",
              "thunders": [
                {
                  "ip": "10.22.32.01",
                  "username": "Online_Pokers_TH",
                  "password": "Thunder@Borse@3201",
                  "resource_id": "09611d51-9534-4f78-b3a1-fe7262152e37",
                  "active_partitions": "POKERS,FOOTBALL"
                }
              ]
          }
    
    
     - /root/.splunk/credentials
        
        token_log=8d189d83-a370-418d-a201-fb779c7b77ca
        token_metrics=cee5368e-d53f-4771-84d7-022b3b033f43
    
    -- All Set ---
    
    Check Logs : /var/logs/thunder-observability-agent/agent.log
## UC_03 - COLLECT_ONLY_METRIC_FROM_THUNDER_&_PUBLISH_IN_SPLUNK
    - Use Cases : 03
    - Scenario  : Collect metrics from thunder/thunders and publish it into splunk.
    
    - Description : Borse Inc is regular a10 client. Company purchased an instance of thunder long back and deployed it on some cloud platform,
    
         This instance is configured as ADC server load balancer for there gaming applications named [Pokers and Football]
         and from past few months company is getting timeout/fail-over complain from there online gaming customers. 
         These generally happened on occasions/event/festival/holidays due to high traffic load on thunder.
         Company wants a standard way to monitor all 14 metrics and logs generated by a thunder on Splunk.
         Also want to get email alert notifications when aggregated cpu usage crosses 75% threshold value so that proper 
         action can be taken on time.
      
    - Company has some shared environment with some hardware space leftover with below information:
        - Linux Environment IP : 10.22.32.51
        - Hardware 			: 2GB RAM, 1CPU, 4GB memory.
    
    - Company has below thunder environment details:
        - Thunder IP: 10.22.32.01
        - User Name : Online_Pokers_TH
        - Password : Thunder@Borse@3201
        - Resource_Id : 09611d51-9534-4f78-b3a1-fe7262152e37
        
    - Company has below Splunk monitoring solution details:
        - splunk_host : "10.64.25.143:8088"
    
    - Company has shared Splunk credentials
        - token_log=8d189d83-a370-418d-a201-fb779c7b77ca
        - token_metrics=cee5368e-d53f-4771-84d7-022b3b033f43
    
    - Solution : A10 support team suggested to install 'Thunder Observability Agent[TOA]' within a cloud platform.
        It's pretty straight forward and super easy.
    
    - Configure TOA:
        - /usr/toaenv/thunder-observability-agent/config.json  
    
          {
            "splunk_provider": 1,
            "splunk_metric": 1,
            "splunk_cpu": 1,
            "splunk_memory": 1,
            "splunk_disk": 1,
            "splunk_throughput": 1,
            "splunk_interfaces": 1,
            "splunk_cps": 1,
            "splunk_tps": 1,
            "splunk_server_down_count": 1,
            "splunk_server_down_percentage": 1,
            "splunk_ssl_cert": 1,
            "splunk_server_error": 1,
            "splunk_sessions": 1,
            "splunk_packet_rate": 1,
            "splunk_packet_drop": 1,
            "splunk_host": "10.64.25.143:8088"
          }
    
       - /root/.thunder/credentials  
         
          {
              "autoscale" : 0,
              "provider" : "",
              "thunders": [
                {
                  "ip": "10.22.32.01",
                  "username": "Online_Pokers_TH",
                  "password": "Thunder@Borse@3201",
                  "resource_id": "09611d51-9534-4f78-b3a1-fe7262152e37",
                  "active_partitions": "POKERS,FOOTBALL"
                }
              ]
          }
    
    
     - /root/.splunk/credentials
        
        token_log=8d189d83-a370-418d-a201-fb779c7b77ca
        token_metric=cee5368e-d53f-4771-84d7-022b3b033f43
    
    -- All Set ---
    
    Check Logs : /var/logs/thunder-observability-agent/agent.log