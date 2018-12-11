# Amazon AppStream 2\.0 Fleet VpcConfig<a name="aws-properties-appstream-fleet-vpcconfig"></a>

<a name="aws-properties-appstream-fleet-vpcconfig-description"></a>The `VpcConfig` property type specifies the VPC configuration information for an Amazon AppStream 2\.0 fleet\.

<a name="aws-properties-appstream-fleet-vpcconfig-inheritance"></a> `VpcConfig` is a property of the [AWS::AppStream::Fleet](aws-resource-appstream-fleet.md) resource\.

## Syntax<a name="aws-properties-appstream-fleet-vpcconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appstream-fleet-vpcconfig-syntax.json"></a>

```
{
  "[SecurityGroupIds](#cfn-appstream-fleet-vpcconfig-securitygroupids)" : [ String, ... ],
  "[SubnetIds](#cfn-appstream-fleet-vpcconfig-subnetids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-appstream-fleet-vpcconfig-syntax.yaml"></a>

```
[SecurityGroupIds](#cfn-appstream-fleet-vpcconfig-securitygroupids): 
  - String
[SubnetIds](#cfn-appstream-fleet-vpcconfig-subnetids): 
  - String
```

## Properties<a name="aws-properties-appstream-fleet-vpcconfig-properties"></a>

`SecurityGroupIds`  <a name="cfn-appstream-fleet-vpcconfig-securitygroupids"></a>
The identifiers of the security groups for the fleet\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SubnetIds`  <a name="cfn-appstream-fleet-vpcconfig-subnetids"></a>
The identifiers of the subnets to which a network interface is attached from the fleet instance\. Fleet instances can use one or two subnets\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 