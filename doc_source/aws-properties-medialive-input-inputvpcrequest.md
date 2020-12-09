# AWS::MediaLive::Input InputVpcRequest<a name="aws-properties-medialive-input-inputvpcrequest"></a>

Settings for a private VPC Input\. When this property is specified, the input destination addresses will be created in a VPC rather than with public Internet addresses\. This property requires setting the roleArn property on Input creation\. Not compatible with the inputSecurityGroups property\. 

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
A list of up to 5 EC2 VPC security group IDs to attach to the Input VPC network interfaces\. Requires subnetIds\. If none are specified then the VPC default security group will be used\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetIds`  <a name="cfn-medialive-input-inputvpcrequest-subnetids"></a>
A list of 2 VPC subnet IDs from the same VPC\. Subnet IDs must be mapped to two unique availability zones \(AZ\)\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)