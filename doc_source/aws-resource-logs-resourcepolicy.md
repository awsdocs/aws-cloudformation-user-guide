# AWS::Logs::ResourcePolicy<a name="aws-resource-logs-resourcepolicy"></a>

Creates or updates a resource policy that allows other AWS services to put log events to this account\. An account can have up to 10 resource policies per AWS Region\.

## Syntax<a name="aws-resource-logs-resourcepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-logs-resourcepolicy-syntax.json"></a>

```
{
  "Type" : "AWS::Logs::ResourcePolicy",
  "Properties" : {
      "[PolicyDocument](#cfn-logs-resourcepolicy-policydocument)" : String,
      "[PolicyName](#cfn-logs-resourcepolicy-policyname)" : String
    }
}
```

### YAML<a name="aws-resource-logs-resourcepolicy-syntax.yaml"></a>

```
Type: AWS::Logs::ResourcePolicy
Properties: 
  [PolicyDocument](#cfn-logs-resourcepolicy-policydocument): String
  [PolicyName](#cfn-logs-resourcepolicy-policyname): String
```

## Properties<a name="aws-resource-logs-resourcepolicy-properties"></a>

`PolicyDocument`  <a name="cfn-logs-resourcepolicy-policydocument"></a>
The details of the policy\. It must be formatted in JSON, and you must use backslashes to escape characters that need to be escaped in JSON strings, such as double quote marks\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `5120`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyName`  <a name="cfn-logs-resourcepolicy-policyname"></a>
The name of the resource policy\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-logs-resourcepolicy-return-values"></a>

### Ref<a name="aws-resource-logs-resourcepolicy-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `PolicyName` of the resource policy\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-logs-resourcepolicy--examples"></a>

### Resource policy example<a name="aws-resource-logs-resourcepolicy--examples--Resource_policy_example"></a>

The following example creates a resource policy that allows Route 53 to write log events to a log group that has this policy attached\.

#### JSON<a name="aws-resource-logs-resourcepolicy--examples--Resource_policy_example--json"></a>

```
{
  "Type": "AWS::Logs::ResourcePolicy",
  "Properties": {
    "PolicyName": "MyResourcePolicy",
    "PolicyDocument": "{ \"Version\": \"2012-10-17\", \"Statement\": [ { \"Sid\": \"Route53LogsToCloudWatchLogs\", \"Effect\": \"Allow\", \"Principal\": { \"Service\": [ \"route53.amazonaws.com\" ] }, \"Action\":\"logs:PutLogEvents\", \"Resource\": \"logArn\" } ] }"
  }
}
```

#### YAML<a name="aws-resource-logs-resourcepolicy--examples--Resource_policy_example--yaml"></a>

```
  Type: AWS::Logs::ResourcePolicy
  Properties:
    PolicyName: "MyResourcePolicy"
    PolicyDocument: "{ \"Version\": \"2012-10-17\", \"Statement\": [ { \"Sid\": \"Route53LogsToCloudWatchLogs\", \"Effect\": \"Allow\", \"Principal\": { \"Service\": [ \"route53.amazonaws.com\" ] }, \"Action\":\"logs:PutLogEvents\", \"Resource\": \"logArn\" } ] }"
```