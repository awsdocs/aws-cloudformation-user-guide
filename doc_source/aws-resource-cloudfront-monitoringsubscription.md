# AWS::CloudFront::MonitoringSubscription<a name="aws-resource-cloudfront-monitoringsubscription"></a>

A monitoring subscription\. This structure contains information about whether additional CloudWatch metrics are enabled for a given CloudFront distribution\.

## Syntax<a name="aws-resource-cloudfront-monitoringsubscription-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudfront-monitoringsubscription-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFront::MonitoringSubscription",
  "Properties" : {
      "[DistributionId](#cfn-cloudfront-monitoringsubscription-distributionid)" : String,
      "[MonitoringSubscription](#cfn-cloudfront-monitoringsubscription-monitoringsubscription)" : MonitoringSubscription
    }
}
```

### YAML<a name="aws-resource-cloudfront-monitoringsubscription-syntax.yaml"></a>

```
Type: AWS::CloudFront::MonitoringSubscription
Properties: 
  [DistributionId](#cfn-cloudfront-monitoringsubscription-distributionid): String
  [MonitoringSubscription](#cfn-cloudfront-monitoringsubscription-monitoringsubscription): 
    MonitoringSubscription
```

## Properties<a name="aws-resource-cloudfront-monitoringsubscription-properties"></a>

`DistributionId`  <a name="cfn-cloudfront-monitoringsubscription-distributionid"></a>
The ID of the distribution that you are enabling metrics for\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MonitoringSubscription`  <a name="cfn-cloudfront-monitoringsubscription-monitoringsubscription"></a>
A subscription configuration for additional CloudWatch metrics\.  
*Required*: Yes  
*Type*: [MonitoringSubscription](aws-properties-cloudfront-monitoringsubscription-monitoringsubscription.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cloudfront-monitoringsubscription-return-values"></a>

### Ref<a name="aws-resource-cloudfront-monitoringsubscription-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the unique identifier for the monitoring subscription, which is the same as the distribution ID of the distribution that the subscription is for\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.