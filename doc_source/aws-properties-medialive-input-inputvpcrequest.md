# AWS::MediaLive::Input InputVpcRequest<a name="aws-properties-medialive-input-inputvpcrequest"></a>

The settings for an Amazon VPC input\. 

## Syntax<a name="aws-properties-medialive-input-inputvpcrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-input-inputvpcrequest-syntax.json"></a>

```
{
  "[SecurityGroupIds](#cfn-medialive-input-inputvpcrequest-securitygroupids)" : [ String, ... ],
  "[SubnetIds](#cfn-medialive-input-inputvpcrequest-subnetids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-medialive-input-inputvpcrequest-syntax.yaml"></a>

```
  [SecurityGroupIds](#cfn-medialive-input-inputvpcrequest-securitygroupids): 
    - String
  [SubnetIds](#cfn-medialive-input-inputvpcrequest-subnetids): 
    - String
```

## Properties<a name="aws-properties-medialive-input-inputvpcrequest-properties"></a>

`SecurityGroupIds`  <a name="cfn-medialive-input-inputvpcrequest-securitygroupids"></a>
The list of up to five VPC security group IDs to attach to the input VPC network interfaces\. The security groups require subnet IDs\. If none are specified, MediaLive uses the VPC default security group\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetIds`  <a name="cfn-medialive-input-inputvpcrequest-subnetids"></a>
The list of two VPC subnet IDs from the same VPC\. You must associate subnet IDs to two unique Availability Zones\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)