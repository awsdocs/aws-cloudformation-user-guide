# AWS::KinesisAnalyticsV2::Application VpcConfiguration<a name="aws-properties-kinesisanalyticsv2-application-vpcconfiguration"></a>

Describes the parameters of a VPC used by the application\.

## Syntax<a name="aws-properties-kinesisanalyticsv2-application-vpcconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesisanalyticsv2-application-vpcconfiguration-syntax.json"></a>

```
{
  "[SecurityGroupIds](#cfn-kinesisanalyticsv2-application-vpcconfiguration-securitygroupids)" : [ String, ... ],
  "[SubnetIds](#cfn-kinesisanalyticsv2-application-vpcconfiguration-subnetids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-kinesisanalyticsv2-application-vpcconfiguration-syntax.yaml"></a>

```
  [SecurityGroupIds](#cfn-kinesisanalyticsv2-application-vpcconfiguration-securitygroupids): 
    - String
  [SubnetIds](#cfn-kinesisanalyticsv2-application-vpcconfiguration-subnetids): 
    - String
```

## Properties<a name="aws-properties-kinesisanalyticsv2-application-vpcconfiguration-properties"></a>

`SecurityGroupIds`  <a name="cfn-kinesisanalyticsv2-application-vpcconfiguration-securitygroupids"></a>
The array of [SecurityGroup](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_SecurityGroup.html) IDs used by the VPC configuration\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetIds`  <a name="cfn-kinesisanalyticsv2-application-vpcconfiguration-subnetids"></a>
The array of [Subnet](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_Subnet.html) IDs used by the VPC configuration\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `16`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)