# Amazon EC2 LaunchTemplate Placement<a name="aws-properties-ec2-launchtemplate-placement"></a>

<a name="aws-properties-ec2-launchtemplate-placement-description"></a>The `Placement` property type specifies the placement for the instance in an Amazon EC2 launch template\.

<a name="aws-properties-ec2-launchtemplate-placement-inheritance"></a> `Placement` is a property of the [Amazon EC2 LaunchTemplate LaunchTemplateData](aws-properties-ec2-launchtemplate-launchtemplatedata.md) property type\.

## Syntax<a name="aws-properties-ec2-launchtemplate-placement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-placement-syntax.json"></a>

```
{
  "[GroupName](#cfn-ec2-launchtemplate-placement-groupname)" : String,
  "[Tenancy](#cfn-ec2-launchtemplate-placement-tenancy)" : String,
  "[AvailabilityZone](#cfn-ec2-launchtemplate-placement-availabilityzone)" : String,
  "[Affinity](#cfn-ec2-launchtemplate-placement-affinity)" : String,
  "[HostId](#cfn-ec2-launchtemplate-placement-hostid)" : String
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-placement-syntax.yaml"></a>

```
[GroupName](#cfn-ec2-launchtemplate-placement-groupname): String
[Tenancy](#cfn-ec2-launchtemplate-placement-tenancy): String
[AvailabilityZone](#cfn-ec2-launchtemplate-placement-availabilityzone): String
[Affinity](#cfn-ec2-launchtemplate-placement-affinity): String
[HostId](#cfn-ec2-launchtemplate-placement-hostid): String
```

## Properties<a name="aws-properties-ec2-launchtemplate-placement-properties"></a>

`Affinity`  <a name="cfn-ec2-launchtemplate-placement-affinity"></a>
The affinity setting for an instance on a Dedicated Host\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`AvailabilityZone`  <a name="cfn-ec2-launchtemplate-placement-availabilityzone"></a>
The Availability Zone for the instance\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`GroupName`  <a name="cfn-ec2-launchtemplate-placement-groupname"></a>
The name of the placement group for the instance\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`HostId`  <a name="cfn-ec2-launchtemplate-placement-hostid"></a>
The ID of the Dedicated Host for the instance\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Tenancy`  <a name="cfn-ec2-launchtemplate-placement-tenancy"></a>
The tenancy of the instance \(if the instance is running in a VPC\)\. An instance with a tenancy of dedicated runs on single\-tenant hardware\.  
Valid values include `default`, `dedicated`, and `host`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ec2-launchtemplate-placement-seealso"></a>
+ [LaunchTemplatePlacementRequest](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_LaunchTemplatePlacementRequest.html) in the *Amazon EC2 API Reference*