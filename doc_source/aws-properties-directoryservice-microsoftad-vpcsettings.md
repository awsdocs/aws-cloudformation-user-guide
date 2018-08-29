# AWS Directory Service MicrosoftAD VpcSettings<a name="aws-properties-directoryservice-microsoftad-vpcsettings"></a>

`VpcSettings` is a property of the [AWS::DirectoryService::MicrosoftAD](aws-resource-directoryservice-microsoftad.md) resource that specifies the VPC settings for a Microsoft directory server\.

## Syntax<a name="w3ab2c21c14d590b5"></a>

### JSON<a name="aws-properties-directoryservice-microsoftad-vpcsettings-syntax.json"></a>

```
{
  "[SubnetIds](#cfn-directoryservice-microsoftad-vpcsettings-subnetids)" : [ String, ... ],
  "[VpcId](#cfn-directoryservice-microsoftad-vpcsettings-vpcid)" : String
}
```

### YAML<a name="aws-properties-directoryservice-microsoftad-vpcsettings-syntax.yaml"></a>

```
[SubnetIds](#cfn-directoryservice-microsoftad-vpcsettings-subnetids):
  - String
[VpcId](#cfn-directoryservice-microsoftad-vpcsettings-vpcid): String
```

## Properties<a name="w3ab2c21c14d590b7"></a>

`SubnetIds`  <a name="cfn-directoryservice-microsoftad-vpcsettings-subnetids"></a>
A list of two subnet IDs for the directory servers\. Each subnet must be in different Availability Zones \(AZs\)\. AWS Directory Service creates a directory server and a DNS server in each subnet\.  
*Required*: Yes  
*Type*: List of String values

`VpcId`  <a name="cfn-directoryservice-microsoftad-vpcsettings-vpcid"></a>
The VPC ID in which to create the Microsoft Active Directory server\.  
*Required*: Yes  
*Type*: String