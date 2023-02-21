# AWS::SageMaker::FeatureGroup OnlineStoreConfig<a name="aws-properties-sagemaker-featuregroup-onlinestoreconfig"></a>

Use this to specify the AWS Key Management Service \(KMS\) Key ID, or `KMSKeyId`, for at rest data encryption\. You can turn `OnlineStore` on or off by specifying the `EnableOnlineStore` flag at General Assembly; the default value is `False`\.

## Syntax<a name="aws-properties-sagemaker-featuregroup-onlinestoreconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-featuregroup-onlinestoreconfig-syntax.json"></a>

```
{
  "[EnableOnlineStore](#cfn-sagemaker-featuregroup-onlinestoreconfig-enableonlinestore)" : Boolean,
  "[SecurityConfig](#cfn-sagemaker-featuregroup-onlinestoreconfig-securityconfig)" : OnlineStoreSecurityConfig
}
```

### YAML<a name="aws-properties-sagemaker-featuregroup-onlinestoreconfig-syntax.yaml"></a>

```
  [EnableOnlineStore](#cfn-sagemaker-featuregroup-onlinestoreconfig-enableonlinestore): Boolean
  [SecurityConfig](#cfn-sagemaker-featuregroup-onlinestoreconfig-securityconfig): 
    OnlineStoreSecurityConfig
```

## Properties<a name="aws-properties-sagemaker-featuregroup-onlinestoreconfig-properties"></a>

`EnableOnlineStore`  <a name="cfn-sagemaker-featuregroup-onlinestoreconfig-enableonlinestore"></a>
Turn `OnlineStore` off by specifying `False` for the `EnableOnlineStore` flag\. Turn `OnlineStore` on by specifying `True` for the `EnableOnlineStore` flag\.   
The default value is `False`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecurityConfig`  <a name="cfn-sagemaker-featuregroup-onlinestoreconfig-securityconfig"></a>
Use to specify KMS Key ID \(`KMSKeyId`\) for at\-rest encryption of your `OnlineStore`\.  
*Required*: No  
*Type*: [OnlineStoreSecurityConfig](aws-properties-sagemaker-featuregroup-onlinestoresecurityconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)