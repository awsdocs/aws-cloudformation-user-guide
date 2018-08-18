# AWS::EC2::NetworkAclEntry<a name="aws-resource-ec2-network-acl-entry"></a>

Creates an entry \(i\.e\., a rule\) in a network ACL with a rule number you specify\. Each network ACL has a set of numbered ingress rules and a separate set of numbered egress rules\.

**Topics**
+ [Syntax](#aws-resource-ec2-networkaclentry-syntax)
+ [Properties](#w3ab2c21c10d433b9)
+ [Return Values](#w3ab2c21c10d433c11)
+ [Example](#w3ab2c21c10d433c13)
+ [See Also](#w3ab2c21c10d433c15)

## Syntax<a name="aws-resource-ec2-networkaclentry-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-networkaclentry-syntax.json"></a>

```
{
   "Type" : "AWS::EC2::NetworkAclEntry",
   "Properties" : {
      "[CidrBlock](#cfn-ec2-networkaclentry-cidrblock)" : String,
      "[Egress](#cfn-ec2-networkaclentry-egress)" : Boolean,
      "[Icmp](#cfn-ec2-networkaclentry-icmp)" : EC2 ICMP,
      "[Ipv6CidrBlock](#cfn-ec2-networkaclentry-ipv6cidrblock)" : String, 
      "[NetworkAclId](#cfn-ec2-networkaclentry-networkaclid)" : String,
      "[PortRange](#cfn-ec2-networkaclentry-portrange)" : EC2 PortRange,
      "[Protocol](#cfn-ec2-networkaclentry-protocol)" : Integer,
      "[RuleAction](#cfn-ec2-networkaclentry-ruleaction)" : String,
      "[RuleNumber](#cfn-ec2-networkaclentry-rulenumber)" : Integer
   }
}
```

### YAML<a name="aws-resource-ec2-networkaclentry-syntax.yaml"></a>

```
Type: "AWS::EC2::NetworkAclEntry"
Properties: 
  [CidrBlock](#cfn-ec2-networkaclentry-cidrblock): String
  [Egress](#cfn-ec2-networkaclentry-egress): Boolean
  [Icmp](#cfn-ec2-networkaclentry-icmp):
    EC2 ICMP
  [Ipv6CidrBlock](#cfn-ec2-networkaclentry-ipv6cidrblock): String 
  [NetworkAclId](#cfn-ec2-networkaclentry-networkaclid): String
  [PortRange](#cfn-ec2-networkaclentry-portrange):
    EC2 PortRange
  [Protocol](#cfn-ec2-networkaclentry-protocol): Integer
  [RuleAction](#cfn-ec2-networkaclentry-ruleaction) : String
  [RuleNumber](#cfn-ec2-networkaclentry-rulenumber) : Integer
```

## Properties<a name="w3ab2c21c10d433b9"></a>

`CidrBlock`  <a name="cfn-ec2-networkaclentry-cidrblock"></a>
The IPv4 CIDR range to allow or deny, in CIDR notation \(e\.g\., 172\.16\.0\.0/24\)\.  
*Required*: Conditional\. You must specify the `CidrBlock` or `Ipv6CidrBlock` property\.  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Egress`  <a name="cfn-ec2-networkaclentry-egress"></a>
Whether this rule applies to egress traffic from the subnet \(`true`\) or ingress traffic to the subnet \(`false`\)\. By default, AWS CloudFormation specifies `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)\.

`Icmp`  <a name="cfn-ec2-networkaclentry-icmp"></a>
The Internet Control Message Protocol \(ICMP\) code and type\.  
*Required*: Conditional required if specifying 1 \(ICMP\) for the protocol parameter\.  
*Type*: [EC2 NetworkAclEntry Icmp](aws-properties-ec2-networkaclentry-icmp.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Ipv6CidrBlock`  <a name="cfn-ec2-networkaclentry-ipv6cidrblock"></a>
The IPv6 CIDR range to allow or deny, in CIDR notation\.  
*Required*: Conditional\. You must specify the `CidrBlock` or `Ipv6CidrBlock` property\.  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`NetworkAclId`  <a name="cfn-ec2-networkaclentry-networkaclid"></a>
ID of the ACL where the entry will be created\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)\.

`PortRange`  <a name="cfn-ec2-networkaclentry-portrange"></a>
The range of port numbers for the UDP/TCP protocol\.  
*Required*: Conditional Required if specifying 6 \(TCP\) or 17 \(UDP\) for the protocol parameter\.  
*Type*: [EC2 NetworkAclEntry PortRange](aws-properties-ec2-networkaclentry-portrange.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Protocol`  <a name="cfn-ec2-networkaclentry-protocol"></a>
The IP protocol that the rule applies to\. You must specify `-1` or a protocol number \(go to [Protocol Numbers](http://www.iana.org/assignments/protocol-numbers/protocol-numbers.xhtml) at iana\.org\)\. You can specify `-1` for all protocols\.  
If you specify `-1`, all ports are opened and the `PortRange` property is ignored\.
*Required*: Yes  
*Type*: Number  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RuleAction`  <a name="cfn-ec2-networkaclentry-ruleaction"></a>
Whether to allow or deny traffic that matches the rule; valid values are "allow" or "deny"\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RuleNumber`  <a name="cfn-ec2-networkaclentry-rulenumber"></a>
Rule number to assign to the entry, such as `100`\. ACL entries are processed in ascending order by rule number\. Entries can't use the same rule number unless one is an egress rule and the other is an ingress rule\. For valid values, see the [CreateNetworkAclEntry](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateNetworkAclEntry.html) action in the *Amazon EC2 API Reference*\.  
*Required*: Yes  
*Type*: Number  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)\.

## Return Values<a name="w3ab2c21c10d433c11"></a>

### Ref<a name="w3ab2c21c10d433c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d433c13"></a>

### JSON<a name="aws-resource-ec2-networkaclentry-example-1.json"></a>

```
{
   "AWSTemplateFormatVersion" : "2010-09-09",
   "Resources" : {
      "myNetworkAclEntry" : {
         "Type" : "AWS::EC2::NetworkAclEntry",
         "Properties" : {
            "NetworkAclId" : { "Ref" : "myNetworkAcl" },
            "RuleNumber" : "100",
            "Protocol" : "-1",
            "RuleAction" : "allow",
            "Egress" : "true",
            "CidrBlock" : "172.16.0.0/24",
            "Icmp" : { "Code" : "-1", "Type" : "-1" },
            "PortRange" : { "From" : "53", "To" : "53" }
         }
      }
   }
}
```

### YAML<a name="aws-resource-ec2-networkaclentry-example-1.yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  myNetworkAclEntry:
    Type: AWS::EC2::NetworkAclEntry
    Properties:
      NetworkAclId:
        Ref: myNetworkAcl
      RuleNumber: '100'
      Protocol: "-1"
      RuleAction: allow
      Egress: 'true'
      CidrBlock: 172.16.0.0/24
      Icmp:
        Code: "-1"
        Type: "-1"
      PortRange:
        From: '53'
        To: '53'
```

## See Also<a name="w3ab2c21c10d433c15"></a>
+ [NetworkAclEntry](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateNetworkAclEntry.html) in the *Amazon EC2 API Reference*
+ [Network ACLs](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_ACLs.html) in the *Amazon Virtual Private Cloud User Guide*\.