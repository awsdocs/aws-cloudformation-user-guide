# AWS::ElasticLoadBalancingV2::LoadBalancer<a name="aws-resource-elasticloadbalancingv2-loadbalancer"></a>

The `AWS::ElasticLoadBalancingV2::LoadBalancer` resource creates an Elastic Load Balancing Application or Network Load Balancer\. For more information, see [Getting Started](http://docs.aws.amazon.com/elasticloadbalancing/latest/userguide/load-balancer-getting-started.html) in the *Elastic Load Balancing User Guide*\.

**Note**  
AWS CloudFormation does not automatically create tags \(key–value pairs\) for an Elastic Load Balancing load balancer\. You must use the [Tags](#cfn-elasticloadbalancingv2-loadbalancer-tags) property to create tags to associate with the load balancer\.

**Topics**
+ [Syntax](#aws-resource-elasticloadbalancingv2-loadbalancer-syntax)
+ [Properties](#w3ab2c21c10d648c10)
+ [Return Values](#w3ab2c21c10d648c12)
+ [Examples](#w3ab2c21c10d648c14)

## Syntax<a name="aws-resource-elasticloadbalancingv2-loadbalancer-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticloadbalancingv2-loadbalancer-syntax.json"></a>

```
{
  "Type" : "AWS::ElasticLoadBalancingV2::LoadBalancer",
  "Properties" : {    
    "[LoadBalancerAttributes](#cfn-elasticloadbalancingv2-loadbalancer-loadbalancerattributes)" : [ [*LoadBalancerAttributes*](aws-properties-elasticloadbalancingv2-loadbalancer-loadbalancerattributes.md), ... ],
    "[Name](#cfn-elasticloadbalancingv2-loadbalancer-name)" : String,
    "[Scheme](#cfn-elasticloadbalancingv2-loadbalancer-scheme)" : String,
    "[SecurityGroups](#cfn-elasticloadbalancingv2-loadbalancer-securitygroups)" : [ String, ... ],
    "[SubnetMappings](#cfn-elasticloadbalancingv2-loadbalancer-subnetmappings)" : [ [*SubnetMapping*](aws-properties-elasticloadbalancingv2-loadbalancer-subnetmapping.md), ... ],
    "[Subnets](#cfn-elasticloadbalancingv2-loadbalancer-subnets)" : [ String, ... ],
    "[Tags](#cfn-elasticloadbalancingv2-loadbalancer-tags)" : [ Resource Tag, ... ],
    "[Type](#cfn-elasticloadbalancingv2-loadbalancer-type)" : String,
    "[IpAddressType](#cfn-elasticloadbalancingv2-loadbalancer-ipaddresstype)" : String
  }
}
```

### YAML<a name="aws-resource-elasticloadbalancingv2-loadbalancer-syntax.yaml"></a>

```
Type: "AWS::ElasticLoadBalancingV2::LoadBalancer"
Properties:
  [LoadBalancerAttributes](#cfn-elasticloadbalancingv2-loadbalancer-loadbalancerattributes):
    - [LoadBalancerAttributes](aws-properties-elasticloadbalancingv2-loadbalancer-loadbalancerattributes.md)
  [Name](#cfn-elasticloadbalancingv2-loadbalancer-name): String
  [Scheme](#cfn-elasticloadbalancingv2-loadbalancer-scheme): String
  [SecurityGroups](#cfn-elasticloadbalancingv2-loadbalancer-securitygroups):
    - String
  [SubnetMappings](#cfn-elasticloadbalancingv2-loadbalancer-subnetmappings):
    - [*SubnetMapping*](aws-properties-elasticloadbalancingv2-loadbalancer-subnetmapping.md)
  [Subnets](#cfn-elasticloadbalancingv2-loadbalancer-subnets):
    - String
  [Tags](#cfn-elasticloadbalancingv2-loadbalancer-tags):
    - Resource Tag
  [Type](#cfn-elasticloadbalancingv2-loadbalancer-type): String
  [IpAddressType](#cfn-elasticloadbalancingv2-loadbalancer-ipaddresstype): String
```

## Properties<a name="w3ab2c21c10d648c10"></a>

For more information and valid parameter values, see the see the `[CreateLoadBalancer](http://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_CreateLoadBalancer.html)` action in the [Elastic Load Balancing API Reference version 2015\-12\-01](http://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/)\.

`LoadBalancerAttributes`  <a name="cfn-elasticloadbalancingv2-loadbalancer-loadbalancerattributes"></a>
Specifies the load balancer configuration\.  
*Required*: No  
*Type*: A list of [Elastic Load Balancing LoadBalancer LoadBalancerAttributes](aws-properties-elasticloadbalancingv2-loadbalancer-loadbalancerattributes.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Name`  <a name="cfn-elasticloadbalancingv2-loadbalancer-name"></a>
Specifies a name for the load balancer\. This name must be unique within your AWS account and can have a maximum of 32 alphanumeric characters and hyphens\. A name can't begin or end with a hyphen\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Scheme`  <a name="cfn-elasticloadbalancingv2-loadbalancer-scheme"></a>
Specifies whether the load balancer is internal or Internet\-facing\. Valid values are `internet-facing` and `internal`\. The default is `internet-facing`\.  
The nodes of an Internet\-facing load balancer have public IP addresses\. The DNS name of an Internet\-facing load balancer is publicly resolvable to the public IP addresses of the nodes\. Therefore, Internet\-facing load balancers can route requests from clients over the Internet\.  
The nodes of an internal load balancer have only private IP addresses\. The DNS name of an internal load balancer is publicly resolvable to the private IP addresses of the nodes\. Therefore, internal load balancers can only route requests from clients with access to the VPC for the load balancer\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SecurityGroups`  <a name="cfn-elasticloadbalancingv2-loadbalancer-securitygroups"></a>
\[Application Load Balancers\] Specifies a list of the IDs of the security groups to assign to the load balancer\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SubnetMappings`  <a name="cfn-elasticloadbalancingv2-loadbalancer-subnetmappings"></a>
The subnets to attach to the load balancer, specified as a list of `SubnetMapping` property types\. You can specify only one subnet per Availability Zone\. You must specify either subnets or subnet mappings\.  
\[Application Load Balancers\] The load balancer is allocated one static IP address per subnet\. You cannot specify your own Elastic IP addresses\.  
\[Network Load Balancers\] You can specify one Elastic IP address per subnet\.  
*Required*: No  
*Type*: List of [Elastic Load Balancing LoadBalancer SubnetMapping](aws-properties-elasticloadbalancingv2-loadbalancer-subnetmapping.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Subnets`  <a name="cfn-elasticloadbalancingv2-loadbalancer-subnets"></a>
The subnets to attach to the load balancer, specified as a list of subnet IDs\. You can specify only one subnet per Availability Zone\. You must specify either subnets or subnet mappings\.  
\[Application Load Balancers\] You must specify subnets from at least two Availability Zones\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Tags`  <a name="cfn-elasticloadbalancingv2-loadbalancer-tags"></a>
Specifies an arbitrary set of tags \(key–value pairs\) to associate with this load balancer\. Use tags to manage your resources\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Type`  <a name="cfn-elasticloadbalancingv2-loadbalancer-type"></a>
Specifies the type of load balancer to create\. Valid values are `application` and `network`\.The default is `application`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`IpAddressType`  <a name="cfn-elasticloadbalancingv2-loadbalancer-ipaddresstype"></a>
\[Application Load Balancers\] The type of IP addresses that are used by the load balancer's subnets, such as `ipv4` \(for IPv4 addresses\) or `dualstack` \(for IPv4 and IPv6 addresses\)\. For valid values, see the `IpAddressType` parameter for the `[CreateLoadBalancer](http://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_CreateLoadBalancer.html)` action in the *Elastic Load Balancing API Reference version 2015\-12\-01*\. The default value is `ipv4`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)  
If `Scheme` is `internal`, then `IpAddressType` must be `ipv4`\.

## Return Values<a name="w3ab2c21c10d648c12"></a>

### Ref<a name="w3ab2c21c10d648c12b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the ARN of the load balancer, for example:

```
arn:aws:elasticloadbalancing:us-west-2:123456789012:loadbalancer/app/my-internal-load-balancer/50dc6c495c0c9188
```

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d648c12b4"></a>

`Fn::GetAtt` returns a value for the following attributes\.

`DNSName`  
The DNS name for the load balancer, for example `my-load-balancer-424835706.us-west-2.elb.amazonaws.com`\.

`CanonicalHostedZoneID`  
The ID of the Amazon Route 53 hosted zone associated with the load balancer, for example `Z2P70J7EXAMPLE`\.

`LoadBalancerFullName`  
The full name of the load balancer, for example `app/my-load-balancer/50dc6c495c0c9188`\.

`LoadBalancerName`  
The name of the load balancer, for example `my-load-balancer`\.

`SecurityGroups`  
The IDs of the security groups for the load balancer, for example `sg-123456a`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Examples<a name="w3ab2c21c10d648c14"></a>

### Load balancer with idle timeout period specified<a name="aws-resource-elasticloadbalancingv2-loadbalancer-example1"></a>

The following example creates an internal load balancer with an idle timeout period of `50` seconds\.

#### JSON<a name="aws-resource-elasticloadbalancingv2-loadbalancer-example.json"></a>

```
"loadBalancer" : {
  "Type": "AWS::ElasticLoadBalancingV2::LoadBalancer",
  "Properties": {
    "Scheme" : "internal",
    "Subnets" : [ {"Ref": "SubnetAZ1"}, {"Ref" : "SubnetAZ2"}],
    "LoadBalancerAttributes" : [
      { "Key" : "idle_timeout.timeout_seconds", "Value" : "50" }
    ],
    "SecurityGroups": [{"Ref": "SecurityGroup1"}, {"Ref" : "SecurityGroup2"}],
    "Tags" : [
      { "Key" : "key", "Value" : "value" },
      { "Key" : "key2", "Value" : "value2" }
    ]
  }
}
```

#### YAML<a name="aws-resource-elasticloadbalancingv2-loadbalancer-example.yaml"></a>

```
loadBalancer:
  Type: AWS::ElasticLoadBalancingV2::LoadBalancer
  Properties:
    Scheme: internal
    Subnets:
    - Ref: SubnetAZ1
    - Ref: SubnetAZ2
    LoadBalancerAttributes:
    - Key: idle_timeout.timeout_seconds
      Value: '50'
    SecurityGroups:
    - Ref: SecurityGroup1
    - Ref: SecurityGroup2
    Tags:
    - Key: key
      Value: value
    - Key: key2
      Value: value2
```

### Load balancer with subnets<a name="aws-resource-elasticloadbalancingv2-listenercertificate-example2"></a>

The following example creates a load balancer with two mapped subnets\.

#### JSON<a name="aws-resource-elasticloadbalancingv2-loadbalancer-example2.json"></a>

```
{
    "Parameters": {
        "FirstSubnet": {
            "Type": "String"
        },
        "SecondSubnet": {
            "Type": "String"
        },
        "ELBType": {
            "Type": "String"
        },
        "ELBIpAddressType": {
            "Type": "String"
        }
    },
    "Resources": {
        "loadBalancer": {
            "Type": "AWS::ElasticLoadBalancingV2::LoadBalancer",
            "Properties": {
                "SubnetMappings": [
                    {
                        "AllocationId": {
                            "Fn::GetAtt": [
                                "FirstEIP",
                                "AllocationId"
                            ]
                        },
                        "SubnetId": {
                            "Ref": "FirstSubnet"
                        }
                    },
                    {
                        "AllocationId": {
                            "Fn::GetAtt": [
                                "SecondEIP",
                                "AllocationId"
                            ]
                        },
                        "SubnetId": {
                            "Ref": "SecondSubnet"
                        }
                    }
                ],
                "Type": {
                    "Ref": "ELBType"
                },
                "IpAddressType": {
                    "Ref": "ELBIpAddressType"
                }
            }
        },
        "FirstEIP": {
            "Type": "AWS::EC2::EIP",
            "Properties": {
                "Domain": "vpc"
            }
        },
        "SecondEIP": {
            "Type": "AWS::EC2::EIP",
            "Properties": {
                "Domain": "vpc"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-elasticloadbalancingv2-loadbalancer-example2.yaml"></a>

```
Parameters:
  FirstSubnet:
    Type: String
  SecondSubnet:
    Type: String
  ELBType:
    Type: String
  ELBIpAddressType:
    Type: String
Resources:
  loadBalancer:
    Type: 'AWS::ElasticLoadBalancingV2::LoadBalancer'
    Properties:
      SubnetMappings:
        - AllocationId: !GetAtt 
            - FirstEIP
            - AllocationId
          SubnetId: !Ref FirstSubnet
        - AllocationId: !GetAtt 
            - SecondEIP
            - AllocationId
          SubnetId: !Ref SecondSubnet
      Type: !Ref ELBType
      IpAddressType: !Ref ELBIpAddressType
  FirstEIP:
    Type: 'AWS::EC2::EIP'
    Properties:
      Domain: vpc
  SecondEIP:
    Type: 'AWS::EC2::EIP'
    Properties:
      Domain: vpc
```