# AWS::NetworkFirewall::Firewall<a name="aws-resource-networkfirewall-firewall"></a>

Use the [AWS::NetworkFirewall::Firewall](#aws-resource-networkfirewall-firewall) to provide stateful, managed, network firewall and intrusion detection and prevention filtering for your VPCs in Amazon VPC\. 

The firewall defines the configuration settings for an AWS Network Firewall firewall\. The settings include the firewall policy, the subnets in your VPC to use for the firewall endpoints, and any tags that are attached to the firewall AWS resource\. 

## Syntax<a name="aws-resource-networkfirewall-firewall-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-networkfirewall-firewall-syntax.json"></a>

```
{
  "Type" : "AWS::NetworkFirewall::Firewall",
  "Properties" : {
      "[DeleteProtection](#cfn-networkfirewall-firewall-deleteprotection)" : Boolean,
      "[Description](#cfn-networkfirewall-firewall-description)" : String,
      "[FirewallName](#cfn-networkfirewall-firewall-firewallname)" : String,
      "[FirewallPolicyArn](#cfn-networkfirewall-firewall-firewallpolicyarn)" : String,
      "[FirewallPolicyChangeProtection](#cfn-networkfirewall-firewall-firewallpolicychangeprotection)" : Boolean,
      "[SubnetChangeProtection](#cfn-networkfirewall-firewall-subnetchangeprotection)" : Boolean,
      "[SubnetMappings](#cfn-networkfirewall-firewall-subnetmappings)" : [ SubnetMapping, ... ],
      "[Tags](#cfn-networkfirewall-firewall-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpcId](#cfn-networkfirewall-firewall-vpcid)" : String
    }
}
```

### YAML<a name="aws-resource-networkfirewall-firewall-syntax.yaml"></a>

```
Type: AWS::NetworkFirewall::Firewall
Properties: 
  [DeleteProtection](#cfn-networkfirewall-firewall-deleteprotection): Boolean
  [Description](#cfn-networkfirewall-firewall-description): String
  [FirewallName](#cfn-networkfirewall-firewall-firewallname): String
  [FirewallPolicyArn](#cfn-networkfirewall-firewall-firewallpolicyarn): String
  [FirewallPolicyChangeProtection](#cfn-networkfirewall-firewall-firewallpolicychangeprotection): Boolean
  [SubnetChangeProtection](#cfn-networkfirewall-firewall-subnetchangeprotection): Boolean
  [SubnetMappings](#cfn-networkfirewall-firewall-subnetmappings): 
    - SubnetMapping
  [Tags](#cfn-networkfirewall-firewall-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpcId](#cfn-networkfirewall-firewall-vpcid): String
```

## Properties<a name="aws-resource-networkfirewall-firewall-properties"></a>

`DeleteProtection`  <a name="cfn-networkfirewall-firewall-deleteprotection"></a>
A flag indicating whether it is possible to delete the firewall\. A setting of `TRUE` indicates that the firewall is protected against deletion\. Use this setting to protect against accidentally deleting a firewall that is in use\. When you create a firewall, the operation initializes this flag to `TRUE`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-networkfirewall-firewall-description"></a>
A description of the firewall\.  
*Required*: No  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `^.*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FirewallName`  <a name="cfn-networkfirewall-firewall-firewallname"></a>
The descriptive name of the firewall\. You can't change the name of a firewall after you create it\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[a-zA-Z0-9-]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FirewallPolicyArn`  <a name="cfn-networkfirewall-firewall-firewallpolicyarn"></a>
The Amazon Resource Name \(ARN\) of the firewall policy\.  
The relationship of firewall to firewall policy is many to one\. Each firewall requires one firewall policy association, and you can use the same firewall policy for multiple firewalls\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^arn:aws.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FirewallPolicyChangeProtection`  <a name="cfn-networkfirewall-firewall-firewallpolicychangeprotection"></a>
A setting indicating whether the firewall is protected against a change to the firewall policy association\. Use this setting to protect against accidentally modifying the firewall policy for a firewall that is in use\. When you create a firewall, the operation initializes this setting to `TRUE`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetChangeProtection`  <a name="cfn-networkfirewall-firewall-subnetchangeprotection"></a>
A setting indicating whether the firewall is protected against changes to the subnet associations\. Use this setting to protect against accidentally modifying the subnet associations for a firewall that is in use\. When you create a firewall, the operation initializes this setting to `TRUE`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetMappings`  <a name="cfn-networkfirewall-firewall-subnetmappings"></a>
The public subnets that Network Firewall is using for the firewall\. Each subnet must belong to a different Availability Zone\.   
*Required*: Yes  
*Type*: List of [SubnetMapping](aws-properties-networkfirewall-firewall-subnetmapping.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-networkfirewall-firewall-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcId`  <a name="cfn-networkfirewall-firewall-vpcid"></a>
The unique identifier of the VPC where the firewall is in use\. You can't change the VPC of a firewall after you create the firewall\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^vpc-[0-9a-f]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-networkfirewall-firewall-return-values"></a>

### Ref<a name="aws-resource-networkfirewall-firewall-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the firewall\. For example: 

 `{ "Ref": "arn:aws:network-firewall:us-east-1:012345678901:firewall/myFirewallName" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-networkfirewall-firewall-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-networkfirewall-firewall-return-values-fn--getatt-fn--getatt"></a>

`EndpointIds`  <a name="EndpointIds-fn::getatt"></a>
The unique IDs of the firewall endpoints for all of the subnets that you attached to the firewall\. The subnets are not listed in any particular order\. For example: `["us-west-2c:vpce-111122223333", "us-west-2a:vpce-987654321098", "us-west-2b:vpce-012345678901"]`\. 

`FirewallArn`  <a name="FirewallArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the [AWS::NetworkFirewall::Firewall](#aws-resource-networkfirewall-firewall)\. 

`FirewallId`  <a name="FirewallId-fn::getatt"></a>
The name of the [AWS::NetworkFirewall::Firewall](#aws-resource-networkfirewall-firewall) resource\. 

## Examples<a name="aws-resource-networkfirewall-firewall--examples"></a>



### Create a firewall<a name="aws-resource-networkfirewall-firewall--examples--Create_a_firewall"></a>

The following shows example firewall specifications\. 

#### JSON<a name="aws-resource-networkfirewall-firewall--examples--Create_a_firewall--json"></a>

```
"SampleFirewall": {
    "Type": "AWS::NetworkFirewall::Firewall",
    "Properties": {
        "FirewallName": "SampleFirewallName",
        "FirewallPolicyArn": {
            "Ref": "SampleFirewallPolicy"
        },
        "VpcId": {
            "Ref": "SampleVPC"
        },
        "SubnetMappings": [
            {
                "SubnetId": {
                    "Ref": "SampleSubnet1"
                }
            },
            {
                "SubnetId": {
                    "Ref": "SampleSubnet2"
                }
            }
        ],
        "Description": "Firewall description goes here",
        "Tags": [
            {
                "Key": "Foo",
                "Value": "Bar"
            }
        ]
    }
```

#### YAML<a name="aws-resource-networkfirewall-firewall--examples--Create_a_firewall--yaml"></a>

```
SampleFirewall:
  Type: AWS::NetworkFirewall::Firewall
  Properties:
    FirewallName: SampleFirewallName
    FirewallPolicyArn: !Ref SampleFirewallPolicy
    VpcId: !Ref SampleVPC
    SubnetMappings:
      - SubnetId: !Ref SampleSubnet1
      - SubnetId: !Ref SampleSubnet2
    Description: Firewall description goes here
    Tags:
      - Key: Foo
                Value: Bar
```