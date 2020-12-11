# AWS::EC2::NetworkAclEntry<a name="aws-resource-ec2-network-acl-entry"></a>

Specifies an entry, known as a rule, in a network ACL with a rule number you specify\. Each network ACL has a set of numbered ingress rules and a separate set of numbered egress rules\.

 For information about the protocol value, see [Protocol Numbers](https://www.iana.org/assignments/protocol-numbers/protocol-numbers.xhtml) on the Internet Assigned Numbers Authority \(IANA\) website\.

## Syntax<a name="aws-resource-ec2-network-acl-entry-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-network-acl-entry-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::NetworkAclEntry",
  "Properties" : {
      "[CidrBlock](#cfn-ec2-networkaclentry-cidrblock)" : String,
      "[Egress](#cfn-ec2-networkaclentry-egress)" : Boolean,
      "[Icmp](#cfn-ec2-networkaclentry-icmp)" : Icmp,
      "[Ipv6CidrBlock](#cfn-ec2-networkaclentry-ipv6cidrblock)" : String,
      "[NetworkAclId](#cfn-ec2-networkaclentry-networkaclid)" : String,
      "[PortRange](#cfn-ec2-networkaclentry-portrange)" : PortRange,
      "[Protocol](#cfn-ec2-networkaclentry-protocol)" : Integer,
      "[RuleAction](#cfn-ec2-networkaclentry-ruleaction)" : String,
      "[RuleNumber](#cfn-ec2-networkaclentry-rulenumber)" : Integer
    }
}
```

### YAML<a name="aws-resource-ec2-network-acl-entry-syntax.yaml"></a>

```
Type: AWS::EC2::NetworkAclEntry
Properties: 
  [CidrBlock](#cfn-ec2-networkaclentry-cidrblock): String
  [Egress](#cfn-ec2-networkaclentry-egress): Boolean
  [Icmp](#cfn-ec2-networkaclentry-icmp): 
    Icmp
  [Ipv6CidrBlock](#cfn-ec2-networkaclentry-ipv6cidrblock): String
  [NetworkAclId](#cfn-ec2-networkaclentry-networkaclid): String
  [PortRange](#cfn-ec2-networkaclentry-portrange): 
    PortRange
  [Protocol](#cfn-ec2-networkaclentry-protocol): Integer
  [RuleAction](#cfn-ec2-networkaclentry-ruleaction): String
  [RuleNumber](#cfn-ec2-networkaclentry-rulenumber): Integer
```

## Properties<a name="aws-resource-ec2-network-acl-entry-properties"></a>

`CidrBlock`  <a name="cfn-ec2-networkaclentry-cidrblock"></a>
The IPv4 CIDR range to allow or deny, in CIDR notation \(for example, 172\.16\.0\.0/24\)\. Requirement is conditional: You must specify the `CidrBlock` or `Ipv6CidrBlock` property\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Egress`  <a name="cfn-ec2-networkaclentry-egress"></a>
Whether this rule applies to egress traffic from the subnet \(`true`\) or ingress traffic to the subnet \(`false`\)\. By default, AWS CloudFormation specifies `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Icmp`  <a name="cfn-ec2-networkaclentry-icmp"></a>
The Internet Control Message Protocol \(ICMP\) code and type\. Requirement is conditional: Required if specifying 1 \(ICMP\) for the protocol parameter\.   
*Required*: No  
*Type*: [Icmp](aws-properties-ec2-networkaclentry-icmp.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ipv6CidrBlock`  <a name="cfn-ec2-networkaclentry-ipv6cidrblock"></a>
The IPv6 network range to allow or deny, in CIDR notation\. Requirement is conditional: You must specify the `CidrBlock` or `Ipv6CidrBlock` property\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkAclId`  <a name="cfn-ec2-networkaclentry-networkaclid"></a>
The ID of the ACL for the entry\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PortRange`  <a name="cfn-ec2-networkaclentry-portrange"></a>
The range of port numbers for the UDP/TCP protocol\. Conditional required if specifying 6 \(TCP\) or 17 \(UDP\) for the protocol parameter\.  
*Required*: No  
*Type*: [PortRange](aws-properties-ec2-networkaclentry-portrange.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-ec2-networkaclentry-protocol"></a>
The IP protocol that the rule applies to\. You must specify \-1 or a protocol number\. You can specify \-1 for all protocols\.  
If you specify \-1, all ports are opened and the `PortRange` property is ignored\.
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleAction`  <a name="cfn-ec2-networkaclentry-ruleaction"></a>
Whether to allow or deny traffic that matches the rule; valid values are "allow" or "deny"\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `allow | deny`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleNumber`  <a name="cfn-ec2-networkaclentry-rulenumber"></a>
Rule number to assign to the entry, such as 100\. ACL entries are processed in ascending order by rule number\. Entries can't use the same rule number unless one is an egress rule and the other is an ingress rule\.   
*Required*: Yes  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-network-acl-entry-return-values"></a>

### Ref<a name="aws-resource-ec2-network-acl-entry-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ec2-network-acl-entry--examples"></a>



### Network ACL entries for inbound and outbound traffic<a name="aws-resource-ec2-network-acl-entry--examples--Network_ACL_entries_for_inbound_and_outbound_traffic"></a>

The following example creates a network ACL, and creates two entries in the NACL\. The first entry allows inbound SSH traffic from the specified network\. The second entry allows all outbound IPv4 traffic\.

#### JSON<a name="aws-resource-ec2-network-acl-entry--examples--Network_ACL_entries_for_inbound_and_outbound_traffic--json"></a>

```
{
    "Resources": {
        "MyNACL": {
            "Type": "AWS::EC2::NetworkAcl",
            "Properties": {
                "VpcId": "vpc-1122334455aabbccd",
                "Tags": [
                    {
                        "Key": "Name",
                        "Value": "NACLforSSHTraffic"
                    }
                ]
            }
        },
        "InboundRule": {
            "Type": "AWS::EC2::NetworkAclEntry",
            "Properties": {
                "NetworkAclId": {
                    "Ref": "MyNACL"
                },
                "RuleNumber": 100,
                "Protocol": 6,
                "RuleAction": "allow",
                "CidrBlock": "172.16.0.0/24",
                "PortRange": {
                    "From": 22,
                    "To": 22
                }
            }
        },
        "OutboundRule": {
            "Type": "AWS::EC2::NetworkAclEntry",
            "Properties": {
                "NetworkAclId": {
                    "Ref": "MyNACL"
                },
                "RuleNumber": 100,
                "Protocol": -1,
                "Egress": true,
                "RuleAction": "allow",
                "CidrBlock": "0.0.0.0/0"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ec2-network-acl-entry--examples--Network_ACL_entries_for_inbound_and_outbound_traffic--yaml"></a>

```
Resources:
  MyNACL:
    Type: AWS::EC2::NetworkAcl
    Properties:
       VpcId: vpc-1122334455aabbccd
       Tags:
       - Key: Name
         Value: NACLforSSHTraffic
  InboundRule:
    Type: AWS::EC2::NetworkAclEntry
    Properties:
       NetworkAclId:
         Ref: MyNACL
       RuleNumber: 100
       Protocol: 6
       RuleAction: allow
       CidrBlock: 172.16.0.0/24
       PortRange:
         From: 22
         To: 22
  OutboundRule:
    Type: AWS::EC2::NetworkAclEntry
    Properties:
       NetworkAclId:
         Ref: MyNACL
       RuleNumber: 100
       Protocol: -1
       Egress: true
       RuleAction: allow
       CidrBlock: 0.0.0.0/0
```

## See also<a name="aws-resource-ec2-network-acl-entry--seealso"></a>
+ [NetworkAclEntry](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/ApiReference-query-CreateNetworkAclEntry.html) in the *Amazon EC2 API Reference*
+ [Network ACLs](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_ACLs.html) in the *Amazon Virtual Private Cloud User Guide*

