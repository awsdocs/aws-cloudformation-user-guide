# AWS::ElasticLoadBalancing::LoadBalancer<a name="aws-properties-ec2-elb"></a>

The AWS::ElasticLoadBalancing::LoadBalancer type creates a LoadBalancer\.

**Note**  
If this resource has a public IP address and is also in a VPC that is defined in the same template, you must use the `DependsOn` attribute to declare a dependency on the VPC\-gateway attachment\. For more information, see [DependsOn Attribute](aws-attribute-dependson.md)\.

**Topics**
+ [Syntax](#aws-resource-elasticloadbalancing-loadbalancer-syntax)
+ [Properties](#aws-properties-ec2-elb-prop)
+ [Return Values](#aws-properties-ec2-elb-ref)
+ [Examples](#w3ab2c21c10d632c15)

## Syntax<a name="aws-resource-elasticloadbalancing-loadbalancer-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticloadbalancing-loadbalancer-syntax.json"></a>

```
{
   "Type": "AWS::ElasticLoadBalancing::LoadBalancer",
   "Properties": {
      "[AccessLoggingPolicy](#cfn-ec2-elb-accessloggingpolicy)" : AccessLoggingPolicy,
      "[AppCookieStickinessPolicy](#cfn-ec2-elb-appcookiestickinesspolicy)" : [ AppCookieStickinessPolicy, ... ],
      "[AvailabilityZones](#cfn-ec2-elb-availabilityzones)" : [ String, ... ],
      "[ConnectionDrainingPolicy](#cfn-ec2-elb-connectiondrainingpolicy)" : ConnectionDrainingPolicy,
      "[ConnectionSettings](#cfn-ec2-elb-connectionsettings)" : ConnectionSettings,
      "[CrossZone](#cfn-ec2-elb-crosszone)" : Boolean,
      "[HealthCheck](#cfn-ec2-elb-healthcheck)" : HealthCheck,
      "[Instances](#cfn-ec2-elb-instances)" : [ String, ... ],
      "[LBCookieStickinessPolicy](#cfn-ec2-elb-lbcookiestickinesspolicy)" : [ LBCookieStickinessPolicy, ... ],
      "[LoadBalancerName](#cfn-ec2-elb-elbname)" : String,
      "[Listeners](#cfn-ec2-elb-listeners)" : [ Listener, ... ],
      "[Policies](#cfn-ec2-elb-policies)" : [ ElasticLoadBalancing Policy, ... ],
      "[Scheme](#cfn-ec2-elb-scheme)" : String,
      "[SecurityGroups](#cfn-ec2-elb-securitygroups)" : [ Security Group, ... ],
      "[Subnets](#cfn-ec2-elb-subnets)" : [ String, ... ],
      "[Tags](#cfn-ec2-elb-tags)" : [ Resource Tag, ... ]
   }
}
```

### YAML<a name="aws-resource-elasticloadbalancing-loadbalancer-syntax.yaml"></a>

```
Type: "AWS::ElasticLoadBalancing::LoadBalancer"
Properties:
  [AccessLoggingPolicy](#cfn-ec2-elb-accessloggingpolicy):
    AccessLoggingPolicy
  [AppCookieStickinessPolicy](#cfn-ec2-elb-appcookiestickinesspolicy):
    - AppCookieStickinessPolicy
  [AvailabilityZones](#cfn-ec2-elb-availabilityzones):
    - String
  [ConnectionDrainingPolicy](#cfn-ec2-elb-connectiondrainingpolicy):
    ConnectionDrainingPolicy
  [ConnectionSettings](#cfn-ec2-elb-connectionsettings):
    ConnectionSettings
  [CrossZone](#cfn-ec2-elb-crosszone): Boolean
  [HealthCheck](#cfn-ec2-elb-healthcheck):
    HealthCheck
  [Instances](#cfn-ec2-elb-instances):
    - String
  [LBCookieStickinessPolicy](#cfn-ec2-elb-lbcookiestickinesspolicy):
    - LBCookieStickinessPolicy
  [LoadBalancerName](#cfn-ec2-elb-elbname): String
  [Listeners](#cfn-ec2-elb-listeners):
    - Listener
  [Policies](#cfn-ec2-elb-policies):
    - ElasticLoadBalancing Policy
  [Scheme](#cfn-ec2-elb-scheme): String,
  [SecurityGroups](#cfn-ec2-elb-securitygroups):
    - Security Group
  [Subnets](#cfn-ec2-elb-subnets):
    - String
  [Tags](#cfn-ec2-elb-tags):
    - Resource Tag
```

## Properties<a name="aws-properties-ec2-elb-prop"></a>

`AccessLoggingPolicy`  <a name="cfn-ec2-elb-accessloggingpolicy"></a>
Captures detailed information for all requests made to your load balancer, such as the time a request was received, client’s IP address, latencies, request path, and server responses\.  
*Required*: No  
*Type*: [Elastic Load Balancing AccessLoggingPolicy](aws-properties-ec2-elb-accessloggingpolicy.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AppCookieStickinessPolicy`  <a name="cfn-ec2-elb-appcookiestickinesspolicy"></a>
Generates one or more stickiness policies with sticky session lifetimes that follow that of an application\-generated cookie\. These policies can be associated only with HTTP/HTTPS listeners\.  
*Required*: No  
*Type*: A list of [AppCookieStickinessPolicy](aws-properties-ec2-elb-AppCookieStickinessPolicy.md) objects\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AvailabilityZones`  <a name="cfn-ec2-elb-availabilityzones"></a>
The Availability Zones in which to create the load balancer\. You can specify the `AvailabilityZones` or `Subnets` property, but not both\.  
For load balancers that are in a VPC, specify the `Subnets` property\.
*Required*: No  
*Type*: List of String values  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) if you did not have an Availability Zone specified and you are adding one or if you are removing all Availability Zones\. Otherwise, update requires [no interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\.

`ConnectionDrainingPolicy`  <a name="cfn-ec2-elb-connectiondrainingpolicy"></a>
Whether deregistered or unhealthy instances can complete all in\-flight requests\.  
*Required*: No  
*Type*: [Elastic Load Balancing ConnectionDrainingPolicy](aws-properties-ec2-elb-connectiondrainingpolicy.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ConnectionSettings`  <a name="cfn-ec2-elb-connectionsettings"></a>
Specifies how long front\-end and back\-end connections of your load balancer can remain idle\.  
*Required*: No  
*Type*: [Elastic Load Balancing ConnectionSettings](aws-properties-ec2-elb-connectionsettings.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`CrossZone`  <a name="cfn-ec2-elb-crosszone"></a>
Whether cross\-zone load balancing is enabled for the load balancer\. With cross\-zone load balancing, your load balancer nodes route traffic to the back\-end instances across all Availability Zones\. By default the `CrossZone` property is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`HealthCheck`  <a name="cfn-ec2-elb-healthcheck"></a>
Application health check for the instances\.  
*Required*: No  
*Type*: [ElasticLoadBalancing LoadBalancer HealthCheck](aws-properties-ec2-elb-health-check.md)\.  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) if you did not have a health check specified and you are adding one or if you are removing a health check\. Otherwise, update requires [no interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\.

`Instances`  <a name="cfn-ec2-elb-instances"></a>
A list of EC2 instance IDs for the load balancer\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`LBCookieStickinessPolicy`  <a name="cfn-ec2-elb-lbcookiestickinesspolicy"></a>
Generates a stickiness policy with sticky session lifetimes controlled by the lifetime of the browser \(user\-agent\), or by a specified expiration period\. This policy can be associated only with HTTP/HTTPS listeners\.  
*Required*: No  
*Type*: A list of [LBCookieStickinessPolicy](aws-properties-ec2-elb-LBCookieStickinessPolicy.md) objects\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`LoadBalancerName`  <a name="cfn-ec2-elb-elbname"></a>
A name for the load balancer\. For valid values, see the `LoadBalancerName` parameter for the [http://docs.aws.amazon.com/elasticloadbalancing/2012-06-01/APIReference/API_CreateLoadBalancer.html](http://docs.aws.amazon.com/elasticloadbalancing/2012-06-01/APIReference/API_CreateLoadBalancer.html) action in the *Elastic Load Balancing API Reference version 2012\-06\-01*\.  
If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the load balancer\. The name must be unique within your set of load balancers\. For more information, see [Name Type](aws-properties-name.md)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Listeners`  <a name="cfn-ec2-elb-listeners"></a>
One or more listeners for this load balancer\. Each listener must be registered for a specific port, and you cannot have more than one listener for a given port\.  
If you update the property values for a listener specified by the `Listeners` property, AWS CloudFormation will delete the existing listener and create a new one with the updated properties\. During the time that AWS CloudFormation is performing this action, clients will not be able to connect to the load balancer\.
*Required*: Yes  
*Type*: A list of [ElasticLoadBalancing Listener Property Type](aws-properties-ec2-elb-listener.md) objects\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Policies`  <a name="cfn-ec2-elb-policies"></a>
A list of elastic load balancing policies to apply to this elastic load balancer\. Specify only back\-end server policies\. For more information, see [DescribeLoadBalancerPolicyTypes](http://docs.aws.amazon.com/elasticloadbalancing/2012-06-01/APIReference/API_DescribeLoadBalancerPolicyTypes.html) in the *Elastic Load Balancing API Reference version 2012\-06\-01*\.  
*Required*: No  
*Type*: A list of [ElasticLoadBalancing policy](aws-properties-ec2-elb-policy.md) objects\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Scheme`  <a name="cfn-ec2-elb-scheme"></a>
For load balancers attached to an Amazon VPC, this parameter can be used to specify the type of load balancer to use\. Specify `internal` to create an internal load balancer with a DNS name that resolves to private IP addresses or `internet-facing` to create a load balancer with a publicly resolvable DNS name, which resolves to public IP addresses\.  
If you specify `internal`, you must specify subnets to associate with the load balancer, not Availability Zones\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SecurityGroups`  <a name="cfn-ec2-elb-securitygroups"></a>
*Required*: No  
*Type*: A list of security groups assigned to your load balancer within your virtual private cloud \(VPC\)\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Subnets`  <a name="cfn-ec2-elb-subnets"></a>
A list of subnet IDs in your virtual private cloud \(VPC\) to attach to your load balancer\. Do not specify multiple subnets that are in the same Availability Zone\. You can specify the `AvailabilityZones` or `Subnets` property, but not both\.  
For more information about using Elastic Load Balancing in a VPC, see [How Do I Use Elastic Load Balancing in Amazon VPC](http://docs.aws.amazon.com/ElasticLoadBalancing/latest/DeveloperGuide/UserScenariosForVPC.html) in the *Elastic Load Balancing Developer Guide*\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) if you did not have an subnet specified and you are adding one or if you are removing all subnets\. Otherwise, update requires [no interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\. To update the load balancer to another subnet that is in the same Availability Zone, you must do two updates\. You must first update the load balancer to use a subnet in different Availability Zone\. After the update is complete, update the load balancer to use the new subnet that is in the original Availability Zone\.

`Tags`  <a name="cfn-ec2-elb-tags"></a>
An arbitrary set of tags \(key\-value pairs\) for this load balancer\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="aws-properties-ec2-elb-ref"></a>

### Ref<a name="w3ab2c21c10d632c13b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example, `mystack-myelb-1WQN7BJGDB5YQ`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d632c13b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`CanonicalHostedZoneName`  
The name of the Route 53 hosted zone that is associated with the load balancer\.  
If you specify `internal` for the Elastic Load Balancing scheme, use `DNSName` instead\. For an `internal` scheme, the load balancer doesn't have a `CanonicalHostedZoneName` value\.
Example: `mystack-myelb-15HMABG9ZCN57-1013119603.``us-east-2``.elb.amazonaws.com`

`CanonicalHostedZoneNameID`  
The ID of the Route 53 hosted zone name that is associated with the load balancer\.  
Example: `Z3DZXE0Q79N41H`

`DNSName`  
The DNS name for the load balancer\.  
Example: `mystack-myelb-15HMABG9ZCN57-1013119603.``us-east-2``.elb.amazonaws.com`

`SourceSecurityGroup.GroupName`  
The security group that you can use as part of your inbound rules for your load balancer's back\-end Amazon EC2 application instances\.  
Example: `amazon-elb`

`SourceSecurityGroup.OwnerAlias`  
The owner of the source security group\.  
Example: `amazon-elb-sg`

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Examples<a name="w3ab2c21c10d632c15"></a>

### A load balancer with a health check and access logs<a name="w3ab2c21c10d632c15b2"></a>

#### JSON<a name="aws-resource-elasticloadbalancing-loadbalancer-example1.json"></a>

```
"ElasticLoadBalancer" : {
  "Type" : "AWS::ElasticLoadBalancing::LoadBalancer",
  "Properties" : {
    "AvailabilityZones" : { "Fn::GetAZs" : "" },
    "Instances" : [ { "Ref" : "Ec2Instance1" },{ "Ref" : "Ec2Instance2" } ],
    "Listeners" : [ {
      "LoadBalancerPort" : "80",
      "InstancePort" : { "Ref" : "WebServerPort" },
      "Protocol" : "HTTP"
    } ],
    "HealthCheck" : {
      "Target" : {
        "Fn::Join" : [ "", [ "HTTP:", { "Ref" : "WebServerPort" }, "/" ] ]
      },
      "HealthyThreshold" : "3",
      "UnhealthyThreshold" : "5",
      "Interval" : "30",
      "Timeout" : "5"
    },
    "AccessLoggingPolicy": {
      "S3BucketName": {
        "Ref": "S3LoggingBucket"
      },
      "S3BucketPrefix": "MyELBLogs",
      "Enabled": "true",
      "EmitInterval" : "60"
    },
  "DependsOn": "S3LoggingBucketPolicy"
  }
}
```

#### YAML<a name="aws-resource-elasticloadbalancing-loadbalancer-example1.yaml"></a>

```
ElasticLoadBalancer:
  Type: AWS::ElasticLoadBalancing::LoadBalancer
  Properties:
    AvailabilityZones:
      Fn::GetAZs: ''
    Instances:
    - Ref: Ec2Instance1
    - Ref: Ec2Instance2
    Listeners:
    - LoadBalancerPort: '80'
      InstancePort:
        Ref: WebServerPort
      Protocol: HTTP
    HealthCheck:
      Target:
        Fn::Join:
        - ''
        - - 'HTTP:'
          - Ref: WebServerPort
          - "/"
      HealthyThreshold: '3'
      UnhealthyThreshold: '5'
      Interval: '30'
      Timeout: '5'
    AccessLoggingPolicy:
      S3BucketName:
        Ref: S3LoggingBucket
      S3BucketPrefix: MyELBLogs
      Enabled: 'true'
      EmitInterval: '60'
    DependsOn: S3LoggingBucketPolicy
```

### A load balancer with access logging enabled<a name="w3ab2c21c10d632c15b4"></a>

The following sample snippet creates an Amazon S3 bucket with a bucket policy that allows the load balancer to store information in the `Logs/AWSLogs/AWS account number/` folder\. The load balancer also includes an explicit dependency on the bucket policy, which is required before the load balancer can write to the bucket\.

#### JSON<a name="aws-resource-elasticloadbalancing-loadbalancer-example2.json"></a>

```
"S3LoggingBucket": {
  "Type": "AWS::S3::Bucket"
},
"S3LoggingBucketPolicy": {
  "Type": "AWS::S3::BucketPolicy",
  "Properties": {
    "Bucket": {
      "Ref": "S3LoggingBucket"
    },
    "PolicyDocument": {
      "Version": "2012-10-17",
      "Statement": [ {
        "Sid": "ELBAccessLogs20130930",
        "Effect": "Allow",
        "Resource": {
          "Fn::Join": [
            "",
            [
              "arn:aws:s3:::",
              { "Ref": "S3LoggingBucket" },
              "/",
              "Logs",
              "/AWSLogs/",
              { "Ref": "AWS::AccountId" },
              "/*"
            ]
          ]
        },
        "Principal": { "Ref": "ElasticLoadBalancingAccountID" },
        "Action": [
          "s3:PutObject"
        ]
      } ]
    }
  }
},
"ElasticLoadBalancer": {
  "Type": "AWS::ElasticLoadBalancing::LoadBalancer",
  "Properties": {
    "AvailabilityZones": { "Fn::GetAZs": "" },
    "Listeners": [{
      "LoadBalancerPort": "80",
      "InstancePort": "80",
      "Protocol": "HTTP"
    }],
    "HealthCheck": {
      "Target": "HTTP:80/",
      "HealthyThreshold": "3",
      "UnhealthyThreshold": "5",
      "Interval": "30",
      "Timeout": "5"
    },
    "AccessLoggingPolicy": {
      "S3BucketName": {
        "Ref": "S3LoggingBucket"
      },
      "S3BucketPrefix": "Logs",
      "Enabled": "true",
      "EmitInterval" : "60"
    }
  },
  "DependsOn": "S3LoggingBucketPolicy"
}
```

#### YAML<a name="aws-resource-elasticloadbalancing-loadbalancer-example2.yaml"></a>

```
S3LoggingBucket:
  Type: AWS::S3::Bucket
S3LoggingBucketPolicy:
  Type: AWS::S3::BucketPolicy
  Properties:
    Bucket:
      Ref: S3LoggingBucket
    PolicyDocument:
      Version: '2012-10-17'
      Statement:
      - Sid: ELBAccessLogs20130930
        Effect: Allow
        Resource:
          Fn::Join:
          - ''
          - - 'arn:aws:s3:::'
            - Ref: S3LoggingBucket
            - "/"
            - Logs
            - "/AWSLogs/"
            - Ref: AWS::AccountId
            - "/*"
        Principal:
          Ref: ElasticLoadBalancingAccountID
        Action:
        - s3:PutObject
ElasticLoadBalancer:
  Type: AWS::ElasticLoadBalancing::LoadBalancer
  Properties:
    AvailabilityZones:
      Fn::GetAZs: ''
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
    AccessLoggingPolicy:
      S3BucketName:
        Ref: S3LoggingBucket
      S3BucketPrefix: Logs
      Enabled: 'true'
      EmitInterval: '60'
  DependsOn: S3LoggingBucketPolicy
```

### A load balancer with a connection draining policy<a name="w3ab2c21c10d632c15b6"></a>

The following snippet enables a connection draining policy that ends connections to a deregistered or unhealthy instance after 60 seconds\.

#### JSON<a name="aws-resource-elasticloadbalancing-loadbalancer-example3.json"></a>

```
"ElasticLoadBalancer" : {
  "Type" : "AWS::ElasticLoadBalancing::LoadBalancer",
  "Properties" : {
    "AvailabilityZones" : { "Fn::GetAZs" : "" },
    "Instances" : [ { "Ref" : "Ec2Instance1" },{ "Ref" : "Ec2Instance2" } ],
    "Listeners": [{
      "LoadBalancerPort": "80",
      "InstancePort": "80",
      "Protocol": "HTTP"
    }],
    "HealthCheck": {
      "Target": "HTTP:80/",
      "HealthyThreshold": "3",
      "UnhealthyThreshold": "5",
      "Interval": "30",
      "Timeout": "5"
    },
    "ConnectionDrainingPolicy": {
      "Enabled" : "true",
      "Timeout" : "60"
    }
  }
}
```

#### YAML<a name="aws-resource-elasticloadbalancing-loadbalancer-example3.yaml"></a>

```
ElasticLoadBalancer:
  Type: AWS::ElasticLoadBalancing::LoadBalancer
  Properties:
    AvailabilityZones:
      Fn::GetAZs: ''
    Instances:
    - Ref: Ec2Instance1
    - Ref: Ec2Instance2
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
    ConnectionDrainingPolicy:
      Enabled: 'true'
      Timeout: '60'
```

### A load balancer with multiple policies<a name="w3ab2c21c10d632c15b8"></a>

The following snippet creates a load balancer with listeners on port 80 and 443\. The snippet applies a proxy on port 80 and a back\-end server authentication policy on port 443\.

#### JSON<a name="aws-resource-elasticloadbalancing-loadbalancer-example4.json"></a>

```
"ElasticLoadBalancer": {
  "Type": "AWS::ElasticLoadBalancing::LoadBalancer",
  "Properties": {
    "SecurityGroups" : { "Ref" : "SecurityGroups" },
    "Scheme" : "internet-facing",
    "AvailabilityZones": { "Fn::GetAZs": "" },
    "Listeners": [
      {
        "LoadBalancerPort": "80",
        "InstancePort": "80",
        "Protocol": "TCP",
        "InstanceProtocol" : "TCP"
      },
      {
        "LoadBalancerPort": "443",
        "InstancePort": "443",
        "Protocol": "HTTPS",
        "SSLCertificateId" : { "Ref" : "CertARN" },
        "PolicyNames" : ["MySSLNegotiationPolicy", "MyAppCookieStickinessPolicy"]
      }
    ],
    "Policies" : [
      {
        "PolicyName" : "MySSLNegotiationPolicy",
        "PolicyType" : "SSLNegotiationPolicyType",
        "Attributes" : [
            { "Name" : "Protocol-TLSv1", "Value" : "true" },
            { "Name" : "Protocol-SSLv2", "Value" : "true" },
            { "Name" : "Protocol-SSLv3", "Value" : "false" },
            { "Name" : "DHE-RSA-AES256-SHA", "Value" : "true" }
        ]
      },
      {
        "PolicyName" : "MyAppCookieStickinessPolicy",
        "PolicyType" : "AppCookieStickinessPolicyType",
        "Attributes" : [
          { "Name" : "CookieName", "Value" : "MyCookie" }
        ]
      },
      {
        "PolicyName" : "MyPublicKeyPolicy",
        "PolicyType" : "PublicKeyPolicyType",
        "Attributes" : [
          { "Name" : "PublicKey", "Value" : { "Fn::Join" : [ "\n", [
            "MIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQDh/51Aohx5VrpmlfGHZCzciMBa",
            "fkHve+MQYYJcxmNUKMdsWnz9WtVfKxxWUU7Cfor4lorYmENGCG8FWqCoLDMFs7pN",
            "yGEtpsrlKhzZWtgY1d7eGrUrBil03bI90E2KW0j4qAwGYAC8xixOkNClicojeEz4",
            "f4rr3sUf+ZBSsuMEuwIDAQAB" ] ] }
          }
        ]
      },
      {
        "PolicyName" : "MyBackendServerAuthenticationPolicy",
        "PolicyType" : "BackendServerAuthenticationPolicyType",
        "Attributes" : [
          { "Name" : "PublicKeyPolicyName", "Value" : "MyPublicKeyPolicy" }
        ],
        "InstancePorts" : [ "443" ]
      },
      {
        "PolicyName" : "EnableProxyProtocol",
        "PolicyType" : "ProxyProtocolPolicyType",
        "Attributes" : [
          { "Name"  : "ProxyProtocol", "Value" : "true" }
        ],
        "InstancePorts" : ["80"]
      }
    ]
  }
}
```

#### YAML<a name="aws-resource-elasticloadbalancing-loadbalancer-example4.yaml"></a>

```
ElasticLoadBalancer:
  Type: AWS::ElasticLoadBalancing::LoadBalancer
  Properties:
    SecurityGroups:
      Ref: SecurityGroups
    Scheme: internet-facing
    AvailabilityZones:
      Fn::GetAZs: ''
    Listeners:
    - LoadBalancerPort: '80'
      InstancePort: '80'
      Protocol: TCP
      InstanceProtocol: TCP
    - LoadBalancerPort: '443'
      InstancePort: '443'
      Protocol: HTTPS
      SSLCertificateId:
        Ref: CertARN
      PolicyNames:
      - MySSLNegotiationPolicy
      - MyAppCookieStickinessPolicy
    Policies:
    - PolicyName: MySSLNegotiationPolicy
      PolicyType: SSLNegotiationPolicyType
      Attributes:
      - Name: Protocol-TLSv1
        Value: 'true'
      - Name: Protocol-SSLv2
        Value: 'true'
      - Name: Protocol-SSLv3
        Value: 'false'
      - Name: DHE-RSA-AES256-SHA
        Value: 'true'
    - PolicyName: MyAppCookieStickinessPolicy
      PolicyType: AppCookieStickinessPolicyType
      Attributes:
      - Name: CookieName
        Value: MyCookie
    - PolicyName: MyPublicKeyPolicy
      PolicyType: PublicKeyPolicyType
      Attributes:
      - Name: PublicKey
        Value:
          Fn::Join:
          - "\n"
          - - MIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQDh/51Aohx5VrpmlfGHZCzciMBa
            - fkHve+MQYYJcxmNUKMdsWnz9WtVfKxxWUU7Cfor4lorYmENGCG8FWqCoLDMFs7pN
            - yGEtpsrlKhzZWtgY1d7eGrUrBil03bI90E2KW0j4qAwGYAC8xixOkNClicojeEz4
            - f4rr3sUf+ZBSsuMEuwIDAQAB
    - PolicyName: MyBackendServerAuthenticationPolicy
      PolicyType: BackendServerAuthenticationPolicyType
      Attributes:
      - Name: PublicKeyPolicyName
        Value: MyPublicKeyPolicy
      InstancePorts:
      - '443'
    - PolicyName: EnableProxyProtocol
      PolicyType: ProxyProtocolPolicyType
      Attributes:
      - Name: ProxyProtocol
        Value: 'true'
      InstancePorts:
      - '80'
```

### Additional Examples<a name="w3ab2c21c10d632c15c10"></a>

You can view additional examples from the AWS CloudFormation sample template collection: [Sample Templates](cfn-sample-templates.md)\.