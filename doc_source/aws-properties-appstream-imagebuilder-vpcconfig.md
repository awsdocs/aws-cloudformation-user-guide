# AWS::AppStream::ImageBuilder VpcConfig<a name="aws-properties-appstream-imagebuilder-vpcconfig"></a>

The VPC configuration for the image builder\.

## Syntax<a name="aws-properties-appstream-imagebuilder-vpcconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appstream-imagebuilder-vpcconfig-syntax.json"></a>

```
{
  "[SecurityGroupIds](#cfn-appstream-imagebuilder-vpcconfig-securitygroupids)" : [ String, ... ],
  "[SubnetIds](#cfn-appstream-imagebuilder-vpcconfig-subnetids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-appstream-imagebuilder-vpcconfig-syntax.yaml"></a>

```
  [SecurityGroupIds](#cfn-appstream-imagebuilder-vpcconfig-securitygroupids): 
    - String
  [SubnetIds](#cfn-appstream-imagebuilder-vpcconfig-subnetids): 
    - String
```

## Properties<a name="aws-properties-appstream-imagebuilder-vpcconfig-properties"></a>

`SecurityGroupIds`  <a name="cfn-appstream-imagebuilder-vpcconfig-securitygroupids"></a>
The identifiers of the security groups for the image builder\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetIds`  <a name="cfn-appstream-imagebuilder-vpcconfig-subnetids"></a>
The identifier of the subnet to which a network interface is attached from the image builder instance\. An image builder instance can use one subnet\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)