# AWS::DataSync::LocationEFS Ec2Config<a name="aws-properties-datasync-locationefs-ec2config"></a>

The subnet and the security group that DataSync uses to access the target EFS file system\. The subnet must have at least one mount target for that file system\. The security group that you provide must be able to communicate with the security group on the mount target in the subnet specified\. 

## Syntax<a name="aws-properties-datasync-locationefs-ec2config-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-datasync-locationefs-ec2config-syntax.json"></a>

```
{
  "[SecurityGroupArns](#cfn-datasync-locationefs-ec2config-securitygrouparns)" : [ String, ... ],
  "[SubnetArn](#cfn-datasync-locationefs-ec2config-subnetarn)" : String
}
```

### YAML<a name="aws-properties-datasync-locationefs-ec2config-syntax.yaml"></a>

```
  [SecurityGroupArns](#cfn-datasync-locationefs-ec2config-securitygrouparns): 
    - String
  [SubnetArn](#cfn-datasync-locationefs-ec2config-subnetarn): String
```

## Properties<a name="aws-properties-datasync-locationefs-ec2config-properties"></a>

`SecurityGroupArns`  <a name="cfn-datasync-locationefs-ec2config-securitygrouparns"></a>
The Amazon Resource Names \(ARNs\) of the security groups that are configured for the Amazon EC2 resource\.  
*Pattern*: `^arn:(aws|aws-cn|aws-us-gov|aws-iso|aws-iso-b):ec2:[a-z\-0-9]*:[0-9]{12}:security-group/.*$`  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetArn`  <a name="cfn-datasync-locationefs-ec2config-subnetarn"></a>
The Amazon Resource Name \(ARN\) of the subnet that DataSync uses to access the target EFS file system\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `128`  
*Pattern*: `^arn:(aws|aws-cn|aws-us-gov|aws-iso|aws-iso-b):ec2:[a-z\-0-9]*:[0-9]{12}:subnet/.*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)