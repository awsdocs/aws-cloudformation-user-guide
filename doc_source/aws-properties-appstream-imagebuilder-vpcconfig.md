# Amazon AppStream 2\.0 ImageBuilder VpcConfig<a name="aws-properties-appstream-imagebuilder-vpcconfig"></a>

<a name="aws-properties-appstream-imagebuilder-vpcconfig-description"></a>The `VpcConfig` property type specifies the VPC configuration for an Amazon AppStream 2\.0 image builder\.

<a name="aws-properties-appstream-imagebuilder-vpcconfig-inheritance"></a> `VpcConfig` is a property of the [AWS::AppStream::ImageBuilder](aws-resource-appstream-imagebuilder.md) resource\.

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
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SubnetIds`  <a name="cfn-appstream-imagebuilder-vpcconfig-subnetids"></a>
The identifier of the subnet to which a network interface is attached from the image builder instance\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 