# AWS::EC2::PrefixList<a name="aws-resource-ec2-prefixlist"></a>

Specifies a managed prefix list\. You can add one or more entries to the prefix list\. Each entry consists of a CIDR block and an optional description\.

You must specify the maximum number of entries for the prefix list\. The maximum number of entries cannot be changed later\.

## Syntax<a name="aws-resource-ec2-prefixlist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-prefixlist-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::PrefixList",
  "Properties" : {
      "[AddressFamily](#cfn-ec2-prefixlist-addressfamily)" : String,
      "[Entries](#cfn-ec2-prefixlist-entries)" : [ Entry, ... ],
      "[MaxEntries](#cfn-ec2-prefixlist-maxentries)" : Integer,
      "[PrefixListName](#cfn-ec2-prefixlist-prefixlistname)" : String,
      "[Tags](#cfn-ec2-prefixlist-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ec2-prefixlist-syntax.yaml"></a>

```
Type: AWS::EC2::PrefixList
Properties: 
  [AddressFamily](#cfn-ec2-prefixlist-addressfamily): String
  [Entries](#cfn-ec2-prefixlist-entries): 
    - Entry
  [MaxEntries](#cfn-ec2-prefixlist-maxentries): Integer
  [PrefixListName](#cfn-ec2-prefixlist-prefixlistname): String
  [Tags](#cfn-ec2-prefixlist-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ec2-prefixlist-properties"></a>

`AddressFamily`  <a name="cfn-ec2-prefixlist-addressfamily"></a>
The IP address type\.  
Valid Values: `IPv4` \| `IPv6`   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Entries`  <a name="cfn-ec2-prefixlist-entries"></a>
One or more entries for the prefix list\.  
*Required*: No  
*Type*: List of [Entry](aws-properties-ec2-prefixlist-entry.md)  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxEntries`  <a name="cfn-ec2-prefixlist-maxentries"></a>
The maximum number of entries for the prefix list\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: Updates are not supported\.

`PrefixListName`  <a name="cfn-ec2-prefixlist-prefixlistname"></a>
A name for the prefix list\.  
Constraints: Up to 255 characters in length\. The name cannot start with `com.amazonaws`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ec2-prefixlist-tags"></a>
The tags for the prefix list\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-prefixlist-return-values"></a>

### Ref<a name="aws-resource-ec2-prefixlist-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the prefix list\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-prefixlist-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-prefixlist-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the prefix list\. For example, `arn:aws:ec2:us-east-1:123456789012:prefix-list/pl-0123123123123abcd`\.

`OwnerId`  <a name="OwnerId-fn::getatt"></a>
The ID of the owner of the prefix list\. For example, `123456789012`\.

`PrefixListId`  <a name="PrefixListId-fn::getatt"></a>
The ID of the prefix list\. For example, `pl-0123123123123abcd`\.

`Version`  <a name="Version-fn::getatt"></a>
The version of the prefix list\. For example, `1`\.

## Examples<a name="aws-resource-ec2-prefixlist--examples"></a>

### Creating a prefix list<a name="aws-resource-ec2-prefixlist--examples--Creating_a_prefix_list"></a>

The following example creates an IPv4 prefix list with a maximum of 10 entries, and creates 2 entries in the prefix list\.

#### JSON<a name="aws-resource-ec2-prefixlist--examples--Creating_a_prefix_list--json"></a>

```
{
    "Resources": {
        "NewPrefixList": {
            "Type": "AWS::EC2::PrefixList",
            "Properties": {
                "PrefixListName": "vpc-1-servers",
                "AddressFamily": "IPv4",
                "MaxEntries": 10,
                "Entries": [
                    {
                        "Cidr": "10.0.0.5/32",
                        "Description": "Server 1"
                    },
                    {
                        "Cidr": "10.0.0.10/32",
                        "Description": "Server 2"
                    }
                ],
                "Tags": [
                    {
                        "Key": "Name",
                        "Value": "VPC-1-Servers"
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ec2-prefixlist--examples--Creating_a_prefix_list--yaml"></a>

```
Resources:
  NewPrefixList:
    Type: AWS::EC2::PrefixList
    Properties:
      PrefixListName: "vpc-1-servers"
      AddressFamily: "IPv4"
      MaxEntries: 10
      Entries:
        - Cidr: "10.0.0.5/32"
          Description: "Server 1"
        - Cidr: "10.0.0.10/32"
          Description: "Server 2"
      Tags:
        - Key: "Name"
          Value: "VPC-1-Servers"
```