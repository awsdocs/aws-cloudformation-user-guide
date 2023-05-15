# AWS::S3ObjectLambda::AccessPointPolicy<a name="aws-resource-s3objectlambda-accesspointpolicy"></a>

The `AWS::S3ObjectLambda::AccessPointPolicy` resource specifies the Object Lambda Access Point resource policy document\.

## Syntax<a name="aws-resource-s3objectlambda-accesspointpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-s3objectlambda-accesspointpolicy-syntax.json"></a>

```
{
  "Type" : "AWS::S3ObjectLambda::AccessPointPolicy",
  "Properties" : {
      "[ObjectLambdaAccessPoint](#cfn-s3objectlambda-accesspointpolicy-objectlambdaaccesspoint)" : String,
      "[PolicyDocument](#cfn-s3objectlambda-accesspointpolicy-policydocument)" : Json
    }
}
```

### YAML<a name="aws-resource-s3objectlambda-accesspointpolicy-syntax.yaml"></a>

```
Type: AWS::S3ObjectLambda::AccessPointPolicy
Properties: 
  [ObjectLambdaAccessPoint](#cfn-s3objectlambda-accesspointpolicy-objectlambdaaccesspoint): String
  [PolicyDocument](#cfn-s3objectlambda-accesspointpolicy-policydocument): Json
```

## Properties<a name="aws-resource-s3objectlambda-accesspointpolicy-properties"></a>

`ObjectLambdaAccessPoint`  <a name="cfn-s3objectlambda-accesspointpolicy-objectlambdaaccesspoint"></a>
An access point with an attached AWS Lambda function used to access transformed data from an Amazon S3 bucket\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PolicyDocument`  <a name="cfn-s3objectlambda-accesspointpolicy-policydocument"></a>
Object Lambda Access Point resource policy document\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-s3objectlambda-accesspointpolicy-return-values"></a>

### Ref<a name="aws-resource-s3objectlambda-accesspointpolicy-return-values-ref"></a>

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.