# AWS::Proton::EnvironmentTemplate<a name="aws-resource-proton-environmenttemplate"></a>

Create an environment template for AWS Proton\. For more information, see [Environment Templates](https://docs.aws.amazon.com/proton/latest/userguide/ag-templates.html) in the *AWS Proton User Guide*\.

You can create an environment template in one of the two following ways:
+ Register and publish a *standard* environment template that instructs AWS Proton to deploy and manage environment infrastructure\.
+ Register and publish a *customer managed* environment template that connects AWS Proton to your existing provisioned infrastructure that you manage\. AWS Proton *doesn't* manage your existing provisioned infrastructure\. To create an environment template for customer provisioned and managed infrastructure, include the `provisioning` parameter and set the value to `CUSTOMER_MANAGED`\. For more information, see [Register and publish an environment template](https://docs.aws.amazon.com/proton/latest/userguide/template-create.html) in the *AWS Proton User Guide*\.

## Syntax<a name="aws-resource-proton-environmenttemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-proton-environmenttemplate-syntax.json"></a>

```
{
  "Type" : "AWS::Proton::EnvironmentTemplate",
  "Properties" : {
      "[Description](#cfn-proton-environmenttemplate-description)" : String,
      "[DisplayName](#cfn-proton-environmenttemplate-displayname)" : String,
      "[EncryptionKey](#cfn-proton-environmenttemplate-encryptionkey)" : String,
      "[Name](#cfn-proton-environmenttemplate-name)" : String,
      "[Provisioning](#cfn-proton-environmenttemplate-provisioning)" : String,
      "[Tags](#cfn-proton-environmenttemplate-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-proton-environmenttemplate-syntax.yaml"></a>

```
Type: AWS::Proton::EnvironmentTemplate
Properties: 
  [Description](#cfn-proton-environmenttemplate-description): String
  [DisplayName](#cfn-proton-environmenttemplate-displayname): String
  [EncryptionKey](#cfn-proton-environmenttemplate-encryptionkey): String
  [Name](#cfn-proton-environmenttemplate-name): String
  [Provisioning](#cfn-proton-environmenttemplate-provisioning): String
  [Tags](#cfn-proton-environmenttemplate-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-proton-environmenttemplate-properties"></a>

`Description`  <a name="cfn-proton-environmenttemplate-description"></a>
A description of the environment template\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `500`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisplayName`  <a name="cfn-proton-environmenttemplate-displayname"></a>
The name of the environment template as displayed in the developer interface\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EncryptionKey`  <a name="cfn-proton-environmenttemplate-encryptionkey"></a>
The customer provided encryption key for the environment template\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `200`  
*Pattern*: `^arn:(aws|aws-cn|aws-us-gov):[a-zA-Z0-9-]+:[a-zA-Z0-9-]*:\d{12}:([\w+=,.@-]+[/:])*[\w+=,.@-]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-proton-environmenttemplate-name"></a>
The name of the environment template\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[0-9A-Za-z]+[0-9A-Za-z_\-]*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Provisioning`  <a name="cfn-proton-environmenttemplate-provisioning"></a>
When included, indicates that the environment template is for customer provisioned and managed infrastructure\.  
*Required*: No  
*Type*: String  
*Allowed values*: `CUSTOMER_MANAGED`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-proton-environmenttemplate-tags"></a>
An optional list of metadata items that you can associate with the AWS Proton environment template\. A tag is a key\-value pair\.  
For more information, see [AWS Proton resources and tagging](https://docs.aws.amazon.com/proton/latest/userguide/resources.html) in the *AWS Proton User Guide*\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-proton-environmenttemplate-return-values"></a>

### Ref<a name="aws-resource-proton-environmenttemplate-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the environment template\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-proton-environmenttemplate-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-proton-environmenttemplate-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the ARN of the environment template\.