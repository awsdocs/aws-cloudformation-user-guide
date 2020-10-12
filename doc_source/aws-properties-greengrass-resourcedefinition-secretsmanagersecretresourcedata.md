# AWS::Greengrass::ResourceDefinition SecretsManagerSecretResourceData<a name="aws-properties-greengrass-resourcedefinition-secretsmanagersecretresourcedata"></a>

<a name="aws-properties-greengrass-resourcedefinition-secretsmanagersecretresourcedata-description"></a>Settings for a secret resource, which references a secret from AWS Secrets Manager\. AWS IoT Greengrass stores a local, encrypted copy of the secret on the Greengrass core, where it can be securely accessed by connectors and Lambda functions\. For more information, see [Deploy Secrets to the AWS IoT Greengrass Core](https://docs.aws.amazon.com/greengrass/latest/developerguide/secrets.html) in the *AWS IoT Greengrass Developer Guide*\.

<a name="aws-properties-greengrass-resourcedefinition-secretsmanagersecretresourcedata-inheritance"></a> In an AWS CloudFormation template, `SecretsManagerSecretResourceData` can be used in the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-resourcedefinition-resourcedatacontainer.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-resourcedefinition-resourcedatacontainer.html) property type\.

## Syntax<a name="aws-properties-greengrass-resourcedefinition-secretsmanagersecretresourcedata-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-resourcedefinition-secretsmanagersecretresourcedata-syntax.json"></a>

```
{
  "[AdditionalStagingLabelsToDownload](#cfn-greengrass-resourcedefinition-secretsmanagersecretresourcedata-additionalstaginglabelstodownload)" : [ String, ... ],
  "[ARN](#cfn-greengrass-resourcedefinition-secretsmanagersecretresourcedata-arn)" : String
}
```

### YAML<a name="aws-properties-greengrass-resourcedefinition-secretsmanagersecretresourcedata-syntax.yaml"></a>

```
  [AdditionalStagingLabelsToDownload](#cfn-greengrass-resourcedefinition-secretsmanagersecretresourcedata-additionalstaginglabelstodownload): 
    - String
  [ARN](#cfn-greengrass-resourcedefinition-secretsmanagersecretresourcedata-arn): String
```

## Properties<a name="aws-properties-greengrass-resourcedefinition-secretsmanagersecretresourcedata-properties"></a>

`AdditionalStagingLabelsToDownload`  <a name="cfn-greengrass-resourcedefinition-secretsmanagersecretresourcedata-additionalstaginglabelstodownload"></a>
The staging labels whose values you want to make available on the core, in addition to `AWSCURRENT`\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ARN`  <a name="cfn-greengrass-resourcedefinition-secretsmanagersecretresourcedata-arn"></a>
The Amazon Resource Name \(ARN\) of the Secrets Manager secret to make available on the core\. The value of the secret's latest version \(represented by the `AWSCURRENT` staging label\) is included by default\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-greengrass-resourcedefinition-secretsmanagersecretresourcedata--seealso"></a>
+  [SecretsManagerSecretResourceData](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-secretsmanagersecretresourcedata.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 