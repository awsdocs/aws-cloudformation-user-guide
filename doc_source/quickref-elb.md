# Elastic Load Balancing Template Snippets<a name="quickref-elb"></a>

## Elastic Load Balancing Load Balancer Resource<a name="scenario-elb-load-balancer"></a>

This example shows an Elastic Load Balancing load balancer with a single listener, and no instances\.

### JSON<a name="quickref-elb-example-1.json"></a>

```
"MyLoadBalancer" : {
    "Type" : "AWS::ElasticLoadBalancing::LoadBalancer",
    "Properties" : {
        "AvailabilityZones" : [ "us-east-1a" ],
        "Listeners" : [ {
            "LoadBalancerPort" : "80",
            "InstancePort" : "80",
            "Protocol" : "HTTP"
        } ]
    }
}
```

### YAML<a name="quickref-elb-example-1.yaml"></a>

```
MyLoadBalancer:
  Type: AWS::ElasticLoadBalancing::LoadBalancer
  Properties:
    AvailabilityZones:
    - "us-east-1a"
    Listeners:
    - LoadBalancerPort: '80'
      InstancePort: '80'
      Protocol: HTTP
```

## Elastic Load Balancing Load Balancer Resource with Health Check<a name="scenario-elb-load-balancer-with-healthcheck"></a>

This example shows an Elastic Load Balancing load balancer with two Amazon EC2 instances, a single listener and a health check\.

### JSON<a name="quickref-elb-example-2.json"></a>

```
"MyLoadBalancer" : {
    "Type" : "AWS::ElasticLoadBalancing::LoadBalancer",
    "Properties" : {
        "AvailabilityZones" : [ "us-east-1a" ],
        "Instances" : [
            { "Ref" : "logical name of AWS::EC2::Instance resource 1" },
            { "Ref" : "logical name of AWS::EC2::Instance resource 2" }
        ],
        "Listeners" : [ {
            "LoadBalancerPort" : "80",
            "InstancePort" : "80",
            "Protocol" : "HTTP"
        } ],

        "HealthCheck" : {
            "Target" : "HTTP:80/",
            "HealthyThreshold" : "3",
            "UnhealthyThreshold" : "5",
            "Interval" : "30",
            "Timeout" : "5"
        }
    }
}
```

### YAML<a name="quickref-elb-example-2.yaml"></a>

```
MyLoadBalancer:
  Type: AWS::ElasticLoadBalancing::LoadBalancer
  Properties:
    AvailabilityZones:
    - "us-east-1a"
    Instances:
    - Ref: logical name of AWS::EC2::Instance resource 1
    - Ref: logical name of AWS::EC2::Instance resource 2
    Listeners:
    - LoadBalancerPort: '80'
      InstancePort: '80'
      Protocol: HTTP
    HealthCheck:
      Target: HTTP:80/
      HealthyThreshold: '3'
      UnhealthyThreshold: '5'
      Interval: '30'
      Timeout: '5'
```