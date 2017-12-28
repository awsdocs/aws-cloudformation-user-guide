# AWS::ElasticLoadBalancingV2::TargetGroup<a name="aws-resource-elasticloadbalancingv2-targetgroup"></a>

The `AWS::ElasticLoadBalancingV2::TargetGroup` resource creates an Elastic Load Balancing target group that routes requests to one or more registered targets, such as EC2 instances\. For more information, see [Getting Started](http://docs.aws.amazon.com/elasticloadbalancing/latest/userguide/load-balancer-getting-started.html) in the *Elastic Load Balancing User Guide*\.


+ [Syntax](#aws-resource-elasticloadbalancingv2-targetgroup-syntax)
+ [Properties](#w3ab2c21c10d607b9)
+ [Return Values](#w3ab2c21c10d607c11)
+ [Examples](#w3ab2c21c10d607c13)

## Syntax<a name="aws-resource-elasticloadbalancingv2-targetgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticloadbalancingv2-targetgroup-syntax.json"></a>

```
{
  "Type" : "AWS::ElasticLoadBalancingV2::TargetGroup",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-healthcheckintervalseconds)" : Integer,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-healthcheckpath)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-healthcheckport)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-healthcheckprotocol)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-healthchecktimeoutseconds)" : Integer,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-healthythresholdcount)" : Integer,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-matcher)" : Matcher,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-name)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-port)" : Integer,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-protocol)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-tags)" : [ Resource Tag, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-targetattributes)" : [ TargetGroupAttributes, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-targets)" : [ TargetDescription, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-targettype)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-unhealthythresholdcount)" : Integer,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-vpcid)" : String
  }
}
```

### YAML<a name="aws-resource-elasticloadbalancingv2-targetgroup-syntax.yaml"></a>

```
Type: "AWS::ElasticLoadBalancingV2::TargetGroup"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-healthcheckintervalseconds): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-healthcheckpath): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-healthcheckport): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-healthcheckprotocol): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-healthchecktimeoutseconds): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-healthythresholdcount): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-matcher): Matcher
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-name): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-port): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-protocol): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-tags):
    - Resource Tag
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-targetattributes):
    - TargetGroupAttributes
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-targets):
    - TargetDescription
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-targettype): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-unhealthythresholdcount): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticloadbalancingv2-targetgroup-vpcid): String
```

## Properties<a name="w3ab2c21c10d607b9"></a>

`HealthCheckIntervalSeconds`  
The approximate number of seconds between health checks for an individual target\.  
*Required: *No  
*Type*: Integer  
*Update requires*: No interruption

`HealthCheckPath`  
The ping path destination where Elastic Load Balancing sends health check requests\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`HealthCheckPort`  
The port that the load balancer uses when performing health checks on the targets\.  
For valid and default values, see the `HealthCheckPort` parameter for the [CreateTargetGroup](http://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_CreateTargetGroup.html) action in the *Elastic Load Balancing API Reference version 2015\-12\-01*\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`HealthCheckProtocol`  
The protocol that the load balancer uses when performing health checks on the targets, such as `HTTP` or `HTTPS`\.  
For valid and default values, see the `HealthCheckProtocol` parameter for the [CreateTargetGroup](http://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_CreateTargetGroup.html) action in the *Elastic Load Balancing API Reference version 2015\-12\-01*\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`HealthCheckTimeoutSeconds`  
The number of seconds to wait for a response before considering that a health check has failed\.  
*Required: *No  
*Type*: Integer  
*Update requires*: No interruption

`HealthyThresholdCount`  
The number of consecutive successful health checks that are required before an unhealthy target is considered healthy\.  
*Required: *No  
*Type*: Integer  
*Update requires*: No interruption

`Matcher`  
The HTTP codes that a healthy target uses when responding to a health check\.  
*Required: *No  
*Type*: [Elastic Load Balancing TargetGroup Matcher](aws-properties-elasticloadbalancingv2-targetgroup-matcher.md)  
*Update requires*: No interruption

`Name`  
A name for the target group\.  
This name must be unique per account, per region\.  
The target group name should be shorter than 22 characters because AWS CloudFormation uses the target group name to create the name of the load balancer\.
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`Port`  
The port on which the targets receive traffic\.  
*Required: *Yes  
*Type*: Integer  
*Update requires*: Replacement

`Protocol`  
The protocol to use for routing traffic to the targets\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`Tags`  
An arbitrary set of tags \(key–value pairs\) for the target group\. Use tags to help manage resources\.  
*Required: *No  
*Type*:   
*Update requires*: No interruption\.

`TargetGroupAttributes`  
Target group configurations\.  
*Required: *No  
*Type*: List of [Elastic Load Balancing TargetGroup TargetGroupAttributes](aws-properties-elasticloadbalancingv2-targetgroup-targetgroupattributes.md)  
*Update requires*: No interruption

`Targets`  
The targets to add to this target group\.  
*Required: *No  
*Type*: List of [Elastic Load Balancing TargetGroup TargetDescription](aws-properties-elasticloadbalancingv2-targetgroup-targetdescription.md)  
*Update requires*: No interruption

`TargetType`  
The registration type of the targets in this target group\. Valid values are `instance` and `ip`\. The default is `instance`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: Replacement 

`UnhealthyThresholdCount`  
The number of consecutive failed health checks that are required before a target is considered unhealthy\.  
*Required: *No  
*Type*: Integer  
*Update requires*: No interruption

`VpcId`  
The ID of the VPC in which your targets are located\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

## Return Values<a name="w3ab2c21c10d607c11"></a>

### Ref<a name="w3ab2c21c10d607c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the target group's Amazon Resource Name \(ARN\), such as `arn:aws:elasticloadbalancing:us-west-2:123456789012:targetgroup/my-targets/73e2d6bc24d8a067`\.

For more information about using the `Ref` function, see Ref\.

### Fn::GetAtt<a name="w3ab2c21c10d607c11b4"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`LoadBalancerArns`  
A list of Amazon Resource Names \(ARNs\) of the load balancers that route traffic to this target group, such as `[ "arn:aws:elasticloadbalancing:us-west-2:123456789012:loadbalancer/app/my-load-balancer/50dc6c495c0c9188" ]`\.

`TargetGroupFullName`  
The full name of the target group, such as `targetgroup/my-target-group/cbf133c568e0d028`\.

`TargetGroupName`  
The name of the target group, such as `my-target-group`\. This is the value of the target group's `Name` property\.

For more information about using `Fn::GetAtt`, see Fn::GetAtt\.

## Examples<a name="w3ab2c21c10d607c13"></a>

### Create a Target Group with EC2 Instances as Targets<a name="w3ab2c21c10d607c13b2"></a>

The following examples creates a target group that includes the `Instance1` and `Instance2` EC2 instances as targets\. The instances must respond with a `200` status code to pass health check requests\.

#### JSON<a name="aws-resource-elasticloadbalancingv2-targetgroup-example.json"></a>

```
"TargetGroup" : {
  "Type" : "AWS::ElasticLoadBalancingV2::TargetGroup",
  "Properties" : {
    "HealthCheckIntervalSeconds": 30,
    "HealthCheckProtocol": "HTTPS",
    "HealthCheckTimeoutSeconds": 10,
    "HealthyThresholdCount": 4,
    "Matcher" : {
      "HttpCode" : "200"
    },
    "Name": "MyTargets",
    "Port": 10,
    "Protocol": "HTTPS",
    "TargetGroupAttributes": [{
      "Key": "deregistration_delay.timeout_seconds",
      "Value": "20"
    }],
    "Targets": [
      { "Id": {"Ref" : "Instance1"}, "Port": 80 },
      { "Id": {"Ref" : "Instance2"}, "Port": 80 }
    ],
    "UnhealthyThresholdCount": 3,
    "VpcId": {"Ref" : "VPC"},
    "Tags" : [
      { "Key" : "key", "Value" : "value" },
      { "Key" : "key2", "Value" : "value2" }
    ]
  }
}
```

#### YAML<a name="aws-resource-elasticloadbalancingv2-targetgroup-example.yaml"></a>

```
TargetGroup:
  Type: AWS::ElasticLoadBalancingV2::TargetGroup
  Properties:
    HealthCheckIntervalSeconds: 30
    HealthCheckProtocol: HTTPS
    HealthCheckTimeoutSeconds: 10
    HealthyThresholdCount: 4
    Matcher:
      HttpCode: '200'
    Name: MyTargets
    Port: 10
    Protocol: HTTPS
    TargetGroupAttributes:
    - Key: deregistration_delay.timeout_seconds
      Value: '20'
    Targets:
    - Id:
        Ref: Instance1
      Port: 80
    - Id:
        Ref: Instance2
      Port: 80
    UnhealthyThresholdCount: 3
    VpcId:
      Ref: VPC
    Tags:
    - Key: key
      Value: value
    - Key: key2
      Value: value2
```

### Relate an Elastic Load Balancing Load Balancer to an Elastic Load Balancing Target Group<a name="w3ab2c21c10d607c13b4"></a>

The following example creates an Elastic Load Balancing listener and associates it with a target group and a load balancer\.

#### JSON<a name="aws-resource-elasticloadbalancingv2-load-balancer-target-group-example.json"></a>

```
"ALBListener" : {
  "Type" : "AWS::ElasticLoadBalancingV2::Listener",
  "Properties" : {
    "DefaultActions" : [{
      "Type" : "forward",
      "TargetGroupArn" : { "Ref" : "ALBTargetGroup" }
    }],
    "LoadBalancerArn" : { "Ref" : "ApplicationLoadBalancer" },
    "Port" : "80",
    "Protocol" : "HTTP"
  }
},
"ApplicationLoadBalancer" : {
  "Type" : "AWS::ElasticLoadBalancingV2::LoadBalancer",
  "Properties" : {
    "Scheme" : "internet-facing",
    "Subnets" : [ {"Ref" : "PublicSubnetAz1"}, {"Ref" : "PublicSubnetAz2"}],
    "SecurityGroups" : [{"Ref": "ALBSecurityGroup"}]
  }
},
"ALBTargetGroup" : {
  "Type" : "AWS::ElasticLoadBalancingV2::TargetGroup",
  "Properties" : {
    "HealthCheckIntervalSeconds" : 60,
    "UnhealthyThresholdCount" : 10,
    "HealthCheckPath" : "/",
    "Name" : "MyTargetGroup",
    "Port" : 80,
    "Protocol" : "HTTP",
    "VpcId" : { "Ref": "MyVpc" }
  }
}
```

#### YAML<a name="aws-resource-elasticloadbalancingv2-load-balancer-target-group-example.yaml"></a>

```
ALBListener:
  Type: AWS::ElasticLoadBalancingV2::Listener
  Properties:
    DefaultActions:
      Type: forward
      TargetGroupArn:
        Ref: ALBTargetGroup
      LoadBalancerArn:
        Ref: ApplicationLoadBalancer
      Port: 80
      Protocol: HTTP
ApplicationLoadBalancer:
  Type: AWS::ElasticLoadBalancingV2::LoadBalancer
  Properties:
    Scheme: internet-facing
    Subnets:
      Ref: PublicSubnetAz1
      Ref: PublicSubnetAz2
    SecurityGroups:
      Ref: ALBSecurityGroup
ALBTargetGroup:
  Type: AWS::ElasticLoadBalancingV2::TargetGroup
  Properties:
    HealthCheckIntervalSeconds: 60
    UnhealthyThresholdCount: 10
    HealthCheckPath: /
    Name: MyTargetGroup
    Port: 80
    Protocol: HTTP
    VpcId:
      Ref: MyVpc
```

### Specify the Elastic Load Balancing Target Group type<a name="aws-resource-elasticloadbalancingv2-targetgroup-example3"></a>

The following example specifies the target group type as `instance`\.

#### JSON<a name="aws-resource-elasticloadbalancingv2-targetgroup-example3.json"></a>

```
{
    "Parameters": {
        "CidrBlockForVPC": {
            "Type": "String"
        }
    },
    "Resources": {
        "VPC": {
            "Type": "AWS::EC2::VPC",
            "Properties": {
                "CidrBlock": {
                    "Ref": "CidrBlockForVPC"
                }
            }
        },
        "TargetGroup": {
            "Type": "AWS::ElasticLoadBalancingV2::TargetGroup",
            "Properties": {
                "Port": 1000,
                "Protocol": "HTTPS",
                "TargetType": "instance",
                "VpcId": {
                    "Ref": "VPC"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-elasticloadbalancingv2-targetgroup-example3.yaml"></a>

```
Parameters:
  CidrBlockForVPC:
    Type: String
Resources:
  VPC:
    Type: 'AWS::EC2::VPC'
    Properties:
      CidrBlock: !Ref CidrBlockForVPC
  TargetGroup:
    Type: 'AWS::ElasticLoadBalancingV2::TargetGroup'
    Properties:
      Port: 1000
      Protocol: HTTPS
      TargetType: instance
      VpcId: !Ref VPC
```