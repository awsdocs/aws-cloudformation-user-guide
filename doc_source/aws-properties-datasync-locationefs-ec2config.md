# AWS::DataSync::LocationEFS Ec2Config<a name="aws-properties-datasync-locationefs-ec2config"></a>

The subnet and security groups that AWS DataSync uses to access your Amazon EFS file system\.

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
Specifies the Amazon Resource Names \(ARNs\) of the security groups associated with an Amazon EFS file system's mount target\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetArn`  <a name="cfn-datasync-locationefs-ec2config-subnetarn"></a>
Specifies the ARN of a subnet where DataSync creates the [network interfaces](datasync/latest/userguide/datasync-network.html#required-network-interfaces) for managing traffic during your transfer\.  
The subnet must be located:  
+ In the same virtual private cloud \(VPC\) as the Amazon EFS file system\.
+ In the same Availability Zone as at least one mount target for the Amazon EFS file system\.
You don't need to specify a subnet that includes a file system mount target\.
*Required*: Yes  
*Type*: String  
*Maximum*: `128`  
*Pattern*: `^arn:(aws|aws-cn|aws-us-gov|aws-iso|aws-iso-b):ec2:[a-z\-0-9]*:[0-9]{12}:subnet/.*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)