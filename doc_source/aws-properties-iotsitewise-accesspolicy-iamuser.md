# AWS::IoTSiteWise::AccessPolicy IamUser<a name="aws-properties-iotsitewise-accesspolicy-iamuser"></a>

Contains information about an AWS Identity and Access Management user\.

## Syntax<a name="aws-properties-iotsitewise-accesspolicy-iamuser-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotsitewise-accesspolicy-iamuser-syntax.json"></a>

```
{
  "[arn](#cfn-iotsitewise-accesspolicy-iamuser-arn)" : String
}
```

### YAML<a name="aws-properties-iotsitewise-accesspolicy-iamuser-syntax.yaml"></a>

```
  [arn](#cfn-iotsitewise-accesspolicy-iamuser-arn): String
```

## Properties<a name="aws-properties-iotsitewise-accesspolicy-iamuser-properties"></a>

`arn`  <a name="cfn-iotsitewise-accesspolicy-iamuser-arn"></a>
The ARN of the IAM user\. For more information, see [IAM ARNs](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_identifiers.html) in the *IAM User Guide*\.  
If you delete the IAM user, access policies that contain this identity include an empty `arn`\. You can delete the access policy for the IAM user that no longer exists\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)