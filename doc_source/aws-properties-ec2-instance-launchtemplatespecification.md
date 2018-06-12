# Amazon EC2 Instance LaunchTemplateSpecification<a name="aws-properties-ec2-instance-launchtemplatespecification"></a>

<a name="aws-properties-ec2-instance-launchtemplatespecification-description"></a>The `LaunchTemplateSpecification` property type specifies the launch template to use\. You must specify either the launch template ID or launch template name\.

<a name="aws-properties-ec2-instance-launchtemplatespecification-inheritance"></a> `LaunchTemplateSpecification` is a property of the [AWS::EC2::Instance](aws-properties-ec2-instance.md) resource\.

## Syntax<a name="aws-properties-ec2-launchtemplate-ipv6add-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-ipv6add-syntax.json"></a>

```
{
  "[LaunchTemplateId](#cfn-ec2-instance-launchtemplatespecification-launchtemplateid)" : String,
  "[LaunchTemplateName](#cfn-ec2-instance-launchtemplatespecification-launchtemplatename)" : String,
  "[Version](#cfn-ec2-instance-launchtemplatespecification-version)" : String
}
```

### YAML<a name="aws-properties-dynamodb-table-pointintimerecoveryspecification-syntax.yaml"></a>

```
[LaunchTemplateId](#cfn-ec2-instance-launchtemplatespecification-launchtemplateid): String
[LaunchTemplateName](#cfn-ec2-instance-launchtemplatespecification-launchtemplatename): String
[Version](#cfn-ec2-instance-launchtemplatespecification-version): String
```

## Properties<a name="aws-properties-ec2-instance-launchtemplatespecification-properties"></a>

`LaunchTemplateId`  <a name="cfn-ec2-instance-launchtemplatespecification-launchtemplateid"></a>
The ID of the launch template\. You must specify either a template ID or a template name\.   
Minimum length of 1\. Maximum length of 255\. IDs must fit the following pattern:   
`[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`LaunchTemplateName`  <a name="cfn-ec2-instance-launchtemplatespecification-launchtemplatename"></a>
The name of the launch template\. You must specify either a template name or a template ID\.  
Minimum length of 3\. Maximum length of 128\. Names must fit the following pattern:   
`[a-zA-Z0-9\(\)\.-/_]+ `  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Version`  <a name="cfn-ec2-instance-launchtemplatespecification-version"></a>
The version number\. AWS CloudFormation does not support specifying `$Latest`, or `$Default` for the template version number\.  
Minimum length of 1\. Maximum length of 255\. Versions must fit the following pattern:   
`[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]* `  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ec2-instance-launchtemplatespecification-seealso"></a>
+ [LaunchTemplateSpecification](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_LaunchTemplateSpecification.html) in the *Amazon EC2 API Reference*