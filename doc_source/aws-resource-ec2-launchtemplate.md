# AWS::EC2::LaunchTemplate<a name="aws-resource-ec2-launchtemplate"></a>

The `AWS::EC2::LaunchTemplate` resource creates a launch template for an Amazon EC2 instance\. A launch template contains the parameters to launch an instance\. For more information, see [CreateLaunchTemplate](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateLaunchTemplate.html) in the *Amazon EC2 API Reference*\. 

**Topics**
+ [Syntax](#aws-resource-ec2-launchtemplate-syntax)
+ [Properties](#aws-resource-ec2-launchtemplate-properties)
+ [Return Values](#aws-resource-ec2-launchtemplate-returnvalues)
+ [See Also](#aws-resource-ec2-launchtemplate-seealso)

## Syntax<a name="aws-resource-ec2-launchtemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-launchtemplate-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::LaunchTemplate",
  "Properties" : {
    "[LaunchTemplateName](#cfn-ec2-launchtemplate-launchtemplatename)" : String,
    "[LaunchTemplateData](#cfn-ec2-launchtemplate-launchtemplatedata)" : [*LaunchTemplateData*](aws-properties-ec2-launchtemplate-launchtemplatedata.md)
  }
}
```

### YAML<a name="aws-resource-ec2-launchtemplate-syntax.yaml"></a>

```
Type: "AWS::EC2::LaunchTemplate"
Properties:
  [LaunchTemplateName](#cfn-ec2-launchtemplate-launchtemplatename): String
  [LaunchTemplateData](#cfn-ec2-launchtemplate-launchtemplatedata): [*LaunchTemplateData*](aws-properties-ec2-launchtemplate-launchtemplatedata.md)
```

## Properties<a name="aws-resource-ec2-launchtemplate-properties"></a>

`LaunchTemplateName`  <a name="cfn-ec2-launchtemplate-launchtemplatename"></a>
A name for the launch template\.  
Length Constraints: Minimum length of 3\. Maximum length of 128\.  
Pattern: \[a\-zA\-Z0\-9\\\(\\\)\\\.\-/\_\]\+  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`LaunchTemplateData`  <a name="cfn-ec2-launchtemplate-launchtemplatedata"></a>
The information for the launch template\.  
 *Required*: No  
 *Type*: [Amazon EC2 LaunchTemplate LaunchTemplateData](aws-properties-ec2-launchtemplate-launchtemplatedata.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-ec2-launchtemplate-returnvalues"></a>

### Fn::GetAtt<a name="aws-resource-ec2-launchtemplate-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`LatestVersionNumber`  
The latest version of the launch template, such as `5`\. 

`DefaultVersionNumber`  
The default version of the launch template, such as `2`\.   
The default version of a launch template cannot be specified in AWS CloudFormation\. The default version can be set in the Amazon EC2 Console or by using the `modify-launch-template` AWS CLI command\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## See Also<a name="aws-resource-ec2-launchtemplate-seealso"></a>
+ [CreateLaunchTemplate](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateLaunchTemplate.html) in the *Amazon EC2 API Reference*