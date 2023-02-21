# AWS::ImageBuilder::DistributionConfiguration AmiDistributionConfiguration<a name="aws-properties-imagebuilder-distributionconfiguration-amidistributionconfiguration"></a>

 Define and configure the output AMIs of the pipeline\.

## Syntax<a name="aws-properties-imagebuilder-distributionconfiguration-amidistributionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-imagebuilder-distributionconfiguration-amidistributionconfiguration-syntax.json"></a>

```
{
  "[AmiTags](#cfn-imagebuilder-distributionconfiguration-amidistributionconfiguration-amitags)" : {Key : Value, ...},
  "[Description](#cfn-imagebuilder-distributionconfiguration-amidistributionconfiguration-description)" : String,
  "[KmsKeyId](#cfn-imagebuilder-distributionconfiguration-amidistributionconfiguration-kmskeyid)" : String,
  "[LaunchPermissionConfiguration](#cfn-imagebuilder-distributionconfiguration-amidistributionconfiguration-launchpermissionconfiguration)" : LaunchPermissionConfiguration,
  "[Name](#cfn-imagebuilder-distributionconfiguration-amidistributionconfiguration-name)" : String,
  "[TargetAccountIds](#cfn-imagebuilder-distributionconfiguration-amidistributionconfiguration-targetaccountids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-imagebuilder-distributionconfiguration-amidistributionconfiguration-syntax.yaml"></a>

```
  [AmiTags](#cfn-imagebuilder-distributionconfiguration-amidistributionconfiguration-amitags): 
    Key : Value
  [Description](#cfn-imagebuilder-distributionconfiguration-amidistributionconfiguration-description): String
  [KmsKeyId](#cfn-imagebuilder-distributionconfiguration-amidistributionconfiguration-kmskeyid): String
  [LaunchPermissionConfiguration](#cfn-imagebuilder-distributionconfiguration-amidistributionconfiguration-launchpermissionconfiguration): 
    LaunchPermissionConfiguration
  [Name](#cfn-imagebuilder-distributionconfiguration-amidistributionconfiguration-name): String
  [TargetAccountIds](#cfn-imagebuilder-distributionconfiguration-amidistributionconfiguration-targetaccountids): 
    - String
```

## Properties<a name="aws-properties-imagebuilder-distributionconfiguration-amidistributionconfiguration-properties"></a>

`AmiTags`  <a name="cfn-imagebuilder-distributionconfiguration-amidistributionconfiguration-amitags"></a>
The tags to apply to AMIs distributed to this Region\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-imagebuilder-distributionconfiguration-amidistributionconfiguration-description"></a>
The description of the AMI distribution configuration\. Minimum and maximum length are in characters\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyId`  <a name="cfn-imagebuilder-distributionconfiguration-amidistributionconfiguration-kmskeyid"></a>
The KMS key identifier used to encrypt the distributed image\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchPermissionConfiguration`  <a name="cfn-imagebuilder-distributionconfiguration-amidistributionconfiguration-launchpermissionconfiguration"></a>
 Launch permissions can be used to configure which AWS accounts can use the AMI to launch instances\.  
*Required*: No  
*Type*: [LaunchPermissionConfiguration](aws-properties-imagebuilder-distributionconfiguration-launchpermissionconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-imagebuilder-distributionconfiguration-amidistributionconfiguration-name"></a>
The name of the output AMI\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `127`  
*Pattern*: `^[-_A-Za-z0-9{][-_A-Za-z0-9\s:{}\.]+[-_A-Za-z0-9}]$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetAccountIds`  <a name="cfn-imagebuilder-distributionconfiguration-amidistributionconfiguration-targetaccountids"></a>
The ID of an account to which you want to distribute an image\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `1536`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)