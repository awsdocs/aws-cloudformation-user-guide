# AWS::EC2::LaunchTemplate Placement<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-placement"></a>

Specifies the placement of an instance\.

 `Placement` is a property of the [Amazon EC2 LaunchTemplate LaunchTemplateData](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata.html) property type\.

## Syntax<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-placement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-placement-syntax.json"></a>

```
{
  "[Affinity](#cfn-ec2-launchtemplate-launchtemplatedata-placement-affinity)" : String,
  "[AvailabilityZone](#cfn-ec2-launchtemplate-launchtemplatedata-placement-availabilityzone)" : String,
  "[GroupName](#cfn-ec2-launchtemplate-launchtemplatedata-placement-groupname)" : String,
  "[HostId](#cfn-ec2-launchtemplate-launchtemplatedata-placement-hostid)" : String,
  "[Tenancy](#cfn-ec2-launchtemplate-launchtemplatedata-placement-tenancy)" : String
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-placement-syntax.yaml"></a>

```
  [Affinity](#cfn-ec2-launchtemplate-launchtemplatedata-placement-affinity): String
  [AvailabilityZone](#cfn-ec2-launchtemplate-launchtemplatedata-placement-availabilityzone): String
  [GroupName](#cfn-ec2-launchtemplate-launchtemplatedata-placement-groupname): String
  [HostId](#cfn-ec2-launchtemplate-launchtemplatedata-placement-hostid): String
  [Tenancy](#cfn-ec2-launchtemplate-launchtemplatedata-placement-tenancy): String
```

## Properties<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-placement-properties"></a>

`Affinity`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-placement-affinity"></a>
The affinity setting for an instance on a Dedicated Host\.
*Required*: No
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AvailabilityZone`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-placement-availabilityzone"></a>
The Availability Zone for the instance\.
*Required*: No
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GroupName`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-placement-groupname"></a>
The name of the placement group for the instance\.
*Required*: No
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HostId`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-placement-hostid"></a>
The ID of the Dedicated Host for the instance\.
*Required*: No
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tenancy`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-placement-tenancy"></a>
The tenancy of the instance \(if the instance is running in a VPC\)\. An instance with a tenancy of dedicated runs on single\-tenant hardware\.
*Required*: No
*Type*: String
*Allowed Values*: `dedicated | default | host`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-placement--seealso"></a>
+  [ LaunchTemplatePlacementRequest](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_LaunchTemplatePlacementRequest.html) in the *Amazon Elastic Compute Cloud API Reference*
