# AWS Directory Service SimpleAD VpcSettings<a name="aws-properties-directoryservice-simplead-vpcsettings"></a>

`VpcSettings` is a property of the [AWS::DirectoryService::SimpleAD](aws-resource-directoryservice-simplead.md) resource that specifies the VPC settings for a directory server\.

## Syntax<a name="w3ab2c21c14d512b5"></a>

### JSON<a name="aws-properties-directoryservice-simplead-vpcsettings-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-simplead-vpcsettings-subnetids)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-simplead-vpcsettings-vpcid)" : String
}
```

### YAML<a name="aws-properties-directoryservice-simplead-vpcsettings-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-simplead-vpcsettings-subnetids):
  - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-simplead-vpcsettings-vpcid): String
```

## Properties<a name="w3ab2c21c14d512b7"></a>

`SubnetIds`  
A list of two subnet IDs for the directory servers\. Each subnet must be in different Availability Zones \(AZ\)\. AWS Directory Service creates a directory server and a DNS server in each subnet\.  
*Required: *Yes  
*Type*: List of String values

`VpcId`  
The VPC ID in which to create the Simple AD directory\.  
*Required: *Yes  
*Type*: String