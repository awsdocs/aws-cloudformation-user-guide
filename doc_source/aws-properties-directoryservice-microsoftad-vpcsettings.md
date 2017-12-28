# AWS Directory Service MicrosoftAD VpcSettings<a name="aws-properties-directoryservice-microsoftad-vpcsettings"></a>

`VpcSettings` is a property of the [AWS::DirectoryService::MicrosoftAD](aws-resource-directoryservice-microsoftad.md) resource that specifies the VPC settings for a Microsoft directory server\.

## Syntax<a name="w3ab2c21c14d508b5"></a>

### JSON<a name="aws-properties-directoryservice-microsoftad-vpcsettings-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-microsoftad-vpcsettings-subnetids)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-microsoftad-vpcsettings-vpcid)" : String
}
```

### YAML<a name="aws-properties-directoryservice-microsoftad-vpcsettings-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-microsoftad-vpcsettings-subnetids):
  - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-microsoftad-vpcsettings-vpcid): String
```

## Properties<a name="w3ab2c21c14d508b7"></a>

`SubnetIds`  
A list of two subnet IDs for the directory servers\. Each subnet must be in different Availability Zones \(AZs\)\. AWS Directory Service creates a directory server and a DNS server in each subnet\.  
*Required: *Yes  
*Type*: List of String values

`VpcId`  
The VPC ID in which to create the Microsoft Active Directory server\.  
*Required: *Yes  
*Type*: String