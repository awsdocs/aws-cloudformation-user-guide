# Elastic Load Balancing template snippets<a name="quickref-elb"></a>

## Elastic Load Balancing load balancer resource<a name="scenario-elb-load-balancer"></a>

This example shows an Elastic Load Balancing load balancer with a single listener, and no instances\.

### JSON<a name="quickref-elb-example-1.json"></a>

```
 1. "MyLoadBalancer" : {
 2.     "Type" : "AWS::ElasticLoadBalancing::LoadBalancer",
 3.     "Properties" : {
 4.         "AvailabilityZones" : [ "us-east-1a" ],
 5.         "Listeners" : [ {
 6.             "LoadBalancerPort" : "80",
 7.             "InstancePort" : "80",
 8.             "Protocol" : "HTTP"
 9.         } ]
10.     }
11. }
```

### YAML<a name="quickref-elb-example-1.yaml"></a>

```
1. MyLoadBalancer:
2.   Type: AWS::ElasticLoadBalancing::LoadBalancer
3.   Properties:
4.     AvailabilityZones:
5.     - "us-east-1a"
6.     Listeners:
7.     - LoadBalancerPort: '80'
8.       InstancePort: '80'
9.       Protocol: HTTP
```

## Elastic Load Balancing load balancer resource with health check<a name="scenario-elb-load-balancer-with-healthcheck"></a>

This example shows an Elastic Load Balancing load balancer with two Amazon EC2 instances, a single listener and a health check\.

### JSON<a name="quickref-elb-example-2.json"></a>

```
 1. "MyLoadBalancer" : {
 2.     "Type" : "AWS::ElasticLoadBalancing::LoadBalancer",
 3.     "Properties" : {
 4.         "AvailabilityZones" : [ "us-east-1a" ],
 5.         "Instances" : [
 6.             { "Ref" : "logical name of AWS::EC2::Instance resource 1" },
 7.             { "Ref" : "logical name of AWS::EC2::Instance resource 2" }
 8.         ],
 9.         "Listeners" : [ {
10.             "LoadBalancerPort" : "80",
11.             "InstancePort" : "80",
12.             "Protocol" : "HTTP"
13.         } ],
14. 
15.         "HealthCheck" : {
16.             "Target" : "HTTP:80/",
17.             "HealthyThreshold" : "3",
18.             "UnhealthyThreshold" : "5",
19.             "Interval" : "30",
20.             "Timeout" : "5"
21.         }
22.     }
23. }
```

### YAML<a name="quickref-elb-example-2.yaml"></a>

```
 1. MyLoadBalancer:
 2.   Type: AWS::ElasticLoadBalancing::LoadBalancer
 3.   Properties:
 4.     AvailabilityZones:
 5.     - "us-east-1a"
 6.     Instances:
 7.     - Ref: logical name of AWS::EC2::Instance resource 1
 8.     - Ref: logical name of AWS::EC2::Instance resource 2
 9.     Listeners:
10.     - LoadBalancerPort: '80'
11.       InstancePort: '80'
12.       Protocol: HTTP
13.     HealthCheck:
14.       Target: HTTP:80/
15.       HealthyThreshold: '3'
16.       UnhealthyThreshold: '5'
17.       Interval: '30'
18.       Timeout: '5'
```