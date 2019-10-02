# AWS::SSM::PatchBaseline PatchSource<a name="aws-properties-ssm-patchbaseline-patchsource"></a>

 `PatchSource` is the property type for the `Sources` resource of the [AWS::SSM::PatchBaseline](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-patchbaseline.html) resource\.

The AWS CloudFormation `AWS::SSM::PatchSource` resource is used to provide information about the patches to use to update target instances, including target operating systems and source repository\. Applies to Linux instances only\.

## Syntax<a name="aws-properties-ssm-patchbaseline-patchsource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-patchbaseline-patchsource-syntax.json"></a>

```
{
  "[Configuration](#cfn-ssm-patchbaseline-patchsource-configuration)" : String,
  "[Name](#cfn-ssm-patchbaseline-patchsource-name)" : String,
  "[Products](#cfn-ssm-patchbaseline-patchsource-products)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-ssm-patchbaseline-patchsource-syntax.yaml"></a>

```
  [Configuration](#cfn-ssm-patchbaseline-patchsource-configuration): String
  [Name](#cfn-ssm-patchbaseline-patchsource-name): String
  [Products](#cfn-ssm-patchbaseline-patchsource-products): 
    - String
```

## Properties<a name="aws-properties-ssm-patchbaseline-patchsource-properties"></a>

`Configuration`  <a name="cfn-ssm-patchbaseline-patchsource-configuration"></a>
The value of the yum repo configuration\. For example:  
 `[main]`   
 `cachedir=/var/cache/yum/$basesearch$releasever`   
 `keepcache=0`   
 `debuglevel=2`   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-ssm-patchbaseline-patchsource-name"></a>
The name specified to identify the patch source\.  
*Required*: No  
*Type*: String  
*Pattern*: `^[a-zA-Z0-9_\-.]{3,50}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Products`  <a name="cfn-ssm-patchbaseline-patchsource-products"></a>
The specific operating system versions a patch repository applies to, such as "Ubuntu16\.04", "AmazonLinux2016\.09", "RedhatEnterpriseLinux7\.2" or "Suse12\.7"\. For lists of supported product values, see [PatchFilter](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_PatchFilter.html) in the *AWS Systems Manager API Reference*\.   
*Required*: No  
*Type*: List of String  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
