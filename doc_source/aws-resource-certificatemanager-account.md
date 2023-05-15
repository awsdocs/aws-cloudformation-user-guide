# AWS::CertificateManager::Account<a name="aws-resource-certificatemanager-account"></a>

The `AWS::CertificateManager::Account` resource defines the expiry event configuration that determines the number of days prior to expiry when ACM starts generating EventBridge events\.

## Syntax<a name="aws-resource-certificatemanager-account-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-certificatemanager-account-syntax.json"></a>

```
{
  "Type" : "AWS::CertificateManager::Account",
  "Properties" : {
      "[ExpiryEventsConfiguration](#cfn-certificatemanager-account-expiryeventsconfiguration)" : ExpiryEventsConfiguration
    }
}
```

### YAML<a name="aws-resource-certificatemanager-account-syntax.yaml"></a>

```
Type: AWS::CertificateManager::Account
Properties: 
  [ExpiryEventsConfiguration](#cfn-certificatemanager-account-expiryeventsconfiguration): 
    ExpiryEventsConfiguration
```

## Properties<a name="aws-resource-certificatemanager-account-properties"></a>

`ExpiryEventsConfiguration`  <a name="cfn-certificatemanager-account-expiryeventsconfiguration"></a>
Object containing expiration events options associated with an AWS account\. For more information, see [ExpiryEventsConfiguration](https://docs.aws.amazon.com/acm/latest/APIReference/API_ExpiryEventsConfiguration.html) in the API reference\.  
*Required*: Yes  
*Type*: [ExpiryEventsConfiguration](aws-properties-certificatemanager-account-expiryeventsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-certificatemanager-account-return-values"></a>

### Ref<a name="aws-resource-certificatemanager-account-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the ID of the AWS account that owns the certificate\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-certificatemanager-account-return-values-fn--getatt"></a>

#### <a name="aws-resource-certificatemanager-account-return-values-fn--getatt-fn--getatt"></a>

`AccountId`  <a name="AccountId-fn::getatt"></a>
ID of the AWS account that owns the certificate\.