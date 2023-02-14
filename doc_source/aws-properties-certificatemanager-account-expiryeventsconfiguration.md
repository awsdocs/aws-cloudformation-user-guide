# AWS::CertificateManager::Account ExpiryEventsConfiguration<a name="aws-properties-certificatemanager-account-expiryeventsconfiguration"></a>

Object containing expiration events options associated with an AWS account\. For more information, see [ExpiryEventsConfiguration](https://docs.aws.amazon.com/acm/latest/APIReference/API_ExpiryEventsConfiguration.html) in the API reference\.

## Syntax<a name="aws-properties-certificatemanager-account-expiryeventsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-certificatemanager-account-expiryeventsconfiguration-syntax.json"></a>

```
{
  "[DaysBeforeExpiry](#cfn-certificatemanager-account-expiryeventsconfiguration-daysbeforeexpiry)" : Integer
}
```

### YAML<a name="aws-properties-certificatemanager-account-expiryeventsconfiguration-syntax.yaml"></a>

```
  [DaysBeforeExpiry](#cfn-certificatemanager-account-expiryeventsconfiguration-daysbeforeexpiry): Integer
```

## Properties<a name="aws-properties-certificatemanager-account-expiryeventsconfiguration-properties"></a>

`DaysBeforeExpiry`  <a name="cfn-certificatemanager-account-expiryeventsconfiguration-daysbeforeexpiry"></a>
This option specifies the number of days prior to certificate expiration when ACM starts generating `EventBridge` events\. ACM sends one event per day per certificate until the certificate expires\. By default, accounts receive events starting 45 days before certificate expiration\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)