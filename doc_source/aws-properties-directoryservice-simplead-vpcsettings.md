# AWS::DirectoryService::SimpleAD VpcSettings<a name="aws-properties-directoryservice-simplead-vpcsettings"></a>

Contains VPC information for the [CreateDirectory](https://docs.aws.amazon.com/directoryservice/latest/devguide/API_CreateDirectory.html) or [CreateMicrosoftAD](https://docs.aws.amazon.com/directoryservice/latest/devguide/API_CreateMicrosoftAD.html) operation\.

## Syntax<a name="aws-properties-directoryservice-simplead-vpcsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-directoryservice-simplead-vpcsettings-syntax.json"></a>

```
{
  "[SubnetIds](#cfn-directoryservice-simplead-vpcsettings-subnetids)" : [ String, ... ],
  "[VpcId](#cfn-directoryservice-simplead-vpcsettings-vpcid)" : String
}
```

### YAML<a name="aws-properties-directoryservice-simplead-vpcsettings-syntax.yaml"></a>

```
  [SubnetIds](#cfn-directoryservice-simplead-vpcsettings-subnetids): 
    - String
  [VpcId](#cfn-directoryservice-simplead-vpcsettings-vpcid): String
```

## Properties<a name="aws-properties-directoryservice-simplead-vpcsettings-properties"></a>

`SubnetIds`  <a name="cfn-directoryservice-simplead-vpcsettings-subnetids"></a>
The identifiers of the subnets for the directory servers\. The two subnets must be in different Availability Zones\. AWS Directory Service specifies a directory server and a DNS server in each of these subnets\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcId`  <a name="cfn-directoryservice-simplead-vpcsettings-vpcid"></a>
The identifier of the VPC in which to create the directory\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^(vpc-[0-9a-f]{8}|vpc-[0-9a-f]{17})$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)