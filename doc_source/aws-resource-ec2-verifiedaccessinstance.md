# AWS::EC2::VerifiedAccessInstance<a name="aws-resource-ec2-verifiedaccessinstance"></a>

Describes a Verified Access instance\.

## Syntax<a name="aws-resource-ec2-verifiedaccessinstance-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-verifiedaccessinstance-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::VerifiedAccessInstance",
  "Properties" : {
      "[Description](#cfn-ec2-verifiedaccessinstance-description)" : String,
      "[LoggingConfigurations](#cfn-ec2-verifiedaccessinstance-loggingconfigurations)" : VerifiedAccessLogs,
      "[Tags](#cfn-ec2-verifiedaccessinstance-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VerifiedAccessTrustProviderIds](#cfn-ec2-verifiedaccessinstance-verifiedaccesstrustproviderids)" : [ String, ... ],
      "[VerifiedAccessTrustProviders](#cfn-ec2-verifiedaccessinstance-verifiedaccesstrustproviders)" : [ VerifiedAccessTrustProvider, ... ]
    }
}
```

### YAML<a name="aws-resource-ec2-verifiedaccessinstance-syntax.yaml"></a>

```
Type: AWS::EC2::VerifiedAccessInstance
Properties: 
  [Description](#cfn-ec2-verifiedaccessinstance-description): String
  [LoggingConfigurations](#cfn-ec2-verifiedaccessinstance-loggingconfigurations): 
    VerifiedAccessLogs
  [Tags](#cfn-ec2-verifiedaccessinstance-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VerifiedAccessTrustProviderIds](#cfn-ec2-verifiedaccessinstance-verifiedaccesstrustproviderids): 
    - String
  [VerifiedAccessTrustProviders](#cfn-ec2-verifiedaccessinstance-verifiedaccesstrustproviders): 
    - VerifiedAccessTrustProvider
```

## Properties<a name="aws-resource-ec2-verifiedaccessinstance-properties"></a>

`Description`  <a name="cfn-ec2-verifiedaccessinstance-description"></a>
A description for the AWS Verified Access instance\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoggingConfigurations`  <a name="cfn-ec2-verifiedaccessinstance-loggingconfigurations"></a>
The current logging configuration for the Verified Access instances\.  
*Required*: No  
*Type*: [VerifiedAccessLogs](aws-properties-ec2-verifiedaccessinstance-verifiedaccesslogs.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ec2-verifiedaccessinstance-tags"></a>
The tags\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VerifiedAccessTrustProviderIds`  <a name="cfn-ec2-verifiedaccessinstance-verifiedaccesstrustproviderids"></a>
The IDs of the AWS Verified Access trust providers\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VerifiedAccessTrustProviders`  <a name="cfn-ec2-verifiedaccessinstance-verifiedaccesstrustproviders"></a>
The IDs of the AWS Verified Access trust providers\.  
*Required*: No  
*Type*: List of [VerifiedAccessTrustProvider](aws-properties-ec2-verifiedaccessinstance-verifiedaccesstrustprovider.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-verifiedaccessinstance-return-values"></a>

### Ref<a name="aws-resource-ec2-verifiedaccessinstance-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the Verified Access instance\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-verifiedaccessinstance-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-verifiedaccessinstance-return-values-fn--getatt-fn--getatt"></a>

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
The creation time\.

`LastUpdatedTime`  <a name="LastUpdatedTime-fn::getatt"></a>
The last updated time\.

`VerifiedAccessInstanceId`  <a name="VerifiedAccessInstanceId-fn::getatt"></a>
The ID of the Verified Access instance\.