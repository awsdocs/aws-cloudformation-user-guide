# PatchSource<a name="aws-properties-ssm-patchbaseline-patchsource"></a>

`PatchSource` is the property type for the `Sources` resource of the [AWS::SSM::PatchBaseline](aws-resource-ssm-patchbaseline.md) resource\.

The AWS CloudFormation `AWS::SSM::PatchSource` resource is used to provide information about the patches to use to update target instances, including target operating systems and source repository\. Applies to Linux instances only\.

## Syntax<a name="aws-properties-ssm-patchbaseline-patchsource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-patchbaseline-patchsource-syntax.json"></a>

```
{
  "[Configuration](#cfn-ssm-patchbaseline-patchsource-configuration)" : String,
  "[Name](#cfn-ssm-patchbaseline-patchsource-name)" : String,
  "[Products](#cfn-ssm-patchbaseline-patchsource-products)" : { String:String, ... }
}
```

### YAML<a name="aws-properties-ssm-patchbaseline-patchsource-syntax.yaml"></a>

```
[Configuration](#cfn-ssm-patchbaseline-patchsource-configuration): String
[Name](#cfn-ssm-patchbaseline-patchsource-name): String
[Products](#cfn-ssm-patchbaseline-patchsource-products): String: String
```

## Properties<a name="w13ab1c21c10d231c31c27b9"></a>

`Configuration`  <a name="cfn-ssm-patchbaseline-patchsource-configuration"></a>
The value of the yum repo configuration\.  
*Required*: Yes  
*Type*: String

`Name`  <a name="cfn-ssm-patchbaseline-patchsource-name"></a>
The name specified to identify the patch source\.  
*Required*: No  
*Type*: String

`Products`  <a name="cfn-ssm-patchbaseline-patchsource-products"></a>
The specific operating system versions a patch repository applies to, such as "Ubuntu16\.04", "AmazonLinux2016\.09", "RedhatEnterpriseLinux7\.2" or "Suse12\.7"\. For lists of supported product values, see [PatchFilter](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_PatchFilter.html) in the *AWS Systems Manager API Reference*\.   
*Required*: Yes  
*Type*: String to String map