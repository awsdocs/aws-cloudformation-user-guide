# AWS::Proton::ServiceTemplate<a name="aws-resource-proton-servicetemplate"></a>

Create a service template\. The administrator creates a service template to define standardized infrastructure and an optional CI/CD service pipeline\. Developers, in turn, select the service template from AWS Proton\. If the selected service template includes a service pipeline definition, they provide a link to their source code repository\. AWS Proton then deploys and manages the infrastructure defined by the selected service template\. For more information, see [AWS Proton templates](https://docs.aws.amazon.com/proton/latest/userguide/ag-templates.html) in the *AWS Proton User Guide*\.

## Syntax<a name="aws-resource-proton-servicetemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-proton-servicetemplate-syntax.json"></a>

```
{
  "Type" : "AWS::Proton::ServiceTemplate",
  "Properties" : {
      "[Description](#cfn-proton-servicetemplate-description)" : String,
      "[DisplayName](#cfn-proton-servicetemplate-displayname)" : String,
      "[EncryptionKey](#cfn-proton-servicetemplate-encryptionkey)" : String,
      "[Name](#cfn-proton-servicetemplate-name)" : String,
      "[PipelineProvisioning](#cfn-proton-servicetemplate-pipelineprovisioning)" : String,
      "[Tags](#cfn-proton-servicetemplate-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-proton-servicetemplate-syntax.yaml"></a>

```
Type: AWS::Proton::ServiceTemplate
Properties: 
  [Description](#cfn-proton-servicetemplate-description): String
  [DisplayName](#cfn-proton-servicetemplate-displayname): String
  [EncryptionKey](#cfn-proton-servicetemplate-encryptionkey): String
  [Name](#cfn-proton-servicetemplate-name): String
  [PipelineProvisioning](#cfn-proton-servicetemplate-pipelineprovisioning): String
  [Tags](#cfn-proton-servicetemplate-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-proton-servicetemplate-properties"></a>

`Description`  <a name="cfn-proton-servicetemplate-description"></a>
A description of the service template\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `500`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisplayName`  <a name="cfn-proton-servicetemplate-displayname"></a>
The service template name as displayed in the developer interface\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EncryptionKey`  <a name="cfn-proton-servicetemplate-encryptionkey"></a>
The customer provided service template encryption key that's used to encrypt data\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `200`  
*Pattern*: `^arn:(aws|aws-cn|aws-us-gov):[a-zA-Z0-9-]+:[a-zA-Z0-9-]*:\d{12}:([\w+=,.@-]+[/:])*[\w+=,.@-]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-proton-servicetemplate-name"></a>
The name of the service template\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[0-9A-Za-z]+[0-9A-Za-z_\-]*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PipelineProvisioning`  <a name="cfn-proton-servicetemplate-pipelineprovisioning"></a>
If `pipelineProvisioning` is `true`, a service pipeline is included in the service template\. Otherwise, a service pipeline *isn't* included in the service template\.  
*Required*: No  
*Type*: String  
*Allowed values*: `CUSTOMER_MANAGED`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-proton-servicetemplate-tags"></a>
An object that includes the template bundle S3 bucket path and name for the new version of a service template\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-proton-servicetemplate-return-values"></a>

### Ref<a name="aws-resource-proton-servicetemplate-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the service template\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-proton-servicetemplate-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-proton-servicetemplate-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the service template ARN\.