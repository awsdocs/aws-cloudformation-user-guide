# AWS::XRay::ResourcePolicy<a name="aws-resource-xray-resourcepolicy"></a>

Use `AWS::XRay::ResourcePolicy` to specify an X\-Ray resource\-based policy, which grants one or more AWS services and accounts permissions to access X\-Ray\. Each resource\-based policy is associated with a specific AWS account\.

## Syntax<a name="aws-resource-xray-resourcepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-xray-resourcepolicy-syntax.json"></a>

```
{
  "Type" : "AWS::XRay::ResourcePolicy",
  "Properties" : {
      "[BypassPolicyLockoutCheck](#cfn-xray-resourcepolicy-bypasspolicylockoutcheck)" : Boolean,
      "[PolicyDocument](#cfn-xray-resourcepolicy-policydocument)" : String,
      "[PolicyName](#cfn-xray-resourcepolicy-policyname)" : String
    }
}
```

### YAML<a name="aws-resource-xray-resourcepolicy-syntax.yaml"></a>

```
Type: AWS::XRay::ResourcePolicy
Properties: 
  [BypassPolicyLockoutCheck](#cfn-xray-resourcepolicy-bypasspolicylockoutcheck): Boolean
  [PolicyDocument](#cfn-xray-resourcepolicy-policydocument): String
  [PolicyName](#cfn-xray-resourcepolicy-policyname): String
```

## Properties<a name="aws-resource-xray-resourcepolicy-properties"></a>

`BypassPolicyLockoutCheck`  <a name="cfn-xray-resourcepolicy-bypasspolicylockoutcheck"></a>
A flag to indicate whether to bypass the resource\-based policy lockout safety check\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyDocument`  <a name="cfn-xray-resourcepolicy-policydocument"></a>
The resource\-based policy document, which can be up to 5kb in size\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyName`  <a name="cfn-xray-resourcepolicy-policyname"></a>
The name of the resource\-based policy\. Must be unique within a specific AWS account\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-xray-resourcepolicy-return-values"></a>

### Ref<a name="aws-resource-xray-resourcepolicy-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the policy name\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-xray-resourcepolicy--examples"></a>



### Create resource\-based policy<a name="aws-resource-xray-resourcepolicy--examples--Create_resource-based_policy"></a>

This example creates a resource\-based policy called MySnsActiveTracingPolicy, which configures Amazon SNS active tracing\.

#### JSON<a name="aws-resource-xray-resourcepolicy--examples--Create_resource-based_policy--json"></a>

```
{
   "AWSTemplateFormatVersion": "2010-09-09",
   "Resources": {
      "MyResourcePolicy": {
         "Type": "AWS::XRay::ResourcePolicy",
         "Properties": {
            "BypassPolicyLockoutCheck": "false",
            "PolicyDocument": "{
                \"Version\": \"2012-10-17\",
                \"Statement\": [
                  {
                    \"Sid\": \"SNSAccess\",
                    \"Effect\": \"Allow\",
                    \"Principal\": {
                      \"Service\": \"sns.amazonaws.com\"
                    },
                    \"Action\": [
                      \"xray:PutTraceSegments\",
                      \"xray:GetSamplingRules\",
                      \"xray:GetSamplingTargets\"
                    ],
                    \"Resource\": \"*\",
                    \"Condition\": {
                      \"StringEquals\": {
                        \"aws:SourceAccount\": \"my-account-id\"
                      },
                      \"StringLike\": {
                        \"aws:SourceArn\": \"arn:$my-partition:sns:$my-region:$my-account-id:my-topic-name\"
                      }
                    }
                  }
                ]
              }",
            "PolicyName": "MySnsActiveTracingPolicy"
            }
         }
      }
   }
}
```

#### YAML<a name="aws-resource-xray-resourcepolicy--examples--Create_resource-based_policy--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  MyResourcePolicy:
    Type: AWS::XRay::ResourcePolicy
    Properties:
      BypassPolicyLockoutCheck: false
      PolicyDocument: "{
          \"Version\": \"2012-10-17\",
          \"Statement\": [
            {
              \"Sid\": \"SNSAccess\",
              \"Effect\": \"Allow\",
              \"Principal\": {
                \"Service\": \"sns.amazonaws.com\"
              },
              \"Action\": [
                \"xray:PutTraceSegments\",
                \"xray:GetSamplingRules\",
                \"xray:GetSamplingTargets\"
              ],
              \"Resource\": \"*\",
              \"Condition\": {
                \"StringEquals\": {
                  \"aws:SourceAccount\": \"my-account-id\"
                },
                \"StringLike\": {
                  \"aws:SourceArn\": \"arn:$my-partition:sns:$my-region:$my-account-id:my-topic-name\"
                }
              }
            }
          ]
        }"
      PolicyName: "MySNSActiveTracingPolicy"
```

## See also<a name="aws-resource-xray-resourcepolicy--seealso"></a>
+ [X\-Ray resource\-based policies](https://docs.aws.amazon.com/xray/latest/devguide/security_iam_service-with-iam.html#security_iam_service-with-iam-resource-based-policies)
+ [Identity\-based policies and resource\-based policies](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_identity-vs-resource.html)
+ [PutResourcePolicy](https://docs.aws.amazon.com/xray/latest/api/API_PutResourcePolicy.html) action in the X\-Ray API Reference

