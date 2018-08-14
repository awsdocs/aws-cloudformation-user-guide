# AWS::Logs::LogGroup<a name="aws-resource-logs-loggroup"></a>

The `AWS::Logs::LogGroup` resource creates an Amazon CloudWatch Logs log group that defines common properties for log streams, such as their retention and access control rules\. Each log stream must belong to one log group\.

**Topics**
+ [Syntax](#aws-resource-logs-loggroup-syntax)
+ [Properties](#w3ab2c21c10d872b9)
+ [Return Values](#w3ab2c21c10d872c11)
+ [Examples](#w3ab2c21c10d872c13)
+ [Additional Information](#w3ab2c21c10d872c15)

## Syntax<a name="aws-resource-logs-loggroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-logs-loggroup-syntax.json"></a>

```
{
  "Type" : "AWS::Logs::LogGroup",
  "Properties" : {
    "[LogGroupName](#cfn-cwl-loggroup-loggroupname)" : String,
    "[RetentionInDays](#cfn-cwl-loggroup-retentionindays)" : Integer
  }
}
```

### YAML<a name="aws-resource-logs-loggroup-syntax.yaml"></a>

```
Type: "AWS::Logs::LogGroup"
Properties: 
  [LogGroupName](#cfn-cwl-loggroup-loggroupname): String
  [RetentionInDays](#cfn-cwl-loggroup-retentionindays): Integer
```

## Properties<a name="w3ab2c21c10d872b9"></a>

`LogGroupName`  <a name="cfn-cwl-loggroup-loggroupname"></a>
A name for the log group\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the log group\. For more information, see [Name Type](aws-properties-name.md)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`RetentionInDays`  <a name="cfn-cwl-loggroup-retentionindays"></a>
The number of days log events are kept in CloudWatch Logs\. When a log event expires, CloudWatch Logs automatically deletes it\. For valid values, see [PutRetentionPolicy](http://docs.aws.amazon.com/AmazonCloudWatchLogs/latest/APIReference/API_PutRetentionPolicy.html) in the *Amazon CloudWatch Logs API Reference*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w3ab2c21c10d872c11"></a>

### Ref<a name="w3ab2c21c10d872c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d872c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Arn`  
The Amazon resource name \(ARN\) of the CloudWatch Logs log group, such as `arn:aws:logs:us-east-1:123456789012:log-group:/mystack-testgroup-12ABC1AB12A1:*`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Examples<a name="w3ab2c21c10d872c13"></a>

### <a name="w3ab2c21c10d872c13b2"></a>

The following example creates a CloudWatch Logs log group that retains events for 7 days\.

#### JSON<a name="aws-resource-logs-loggroup-example.json"></a>

```
"myLogGroup": {
    "Type": "AWS::Logs::LogGroup",
    "Properties": {
        "RetentionInDays": 7
    }
}
```

#### YAML<a name="aws-resource-logs-loggroup-example.yaml"></a>

```
myLogGroup: 
  Type: "AWS::Logs::LogGroup"
  Properties: 
    RetentionInDays: 7
```

## Additional Information<a name="w3ab2c21c10d872c15"></a>

For an additional sample template, see [Amazon CloudWatch Logs Template Snippets](quickref-cloudwatchlogs.md)\.