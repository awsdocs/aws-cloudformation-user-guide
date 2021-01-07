# AWS::Logs::LogGroup<a name="aws-resource-logs-loggroup"></a>

The `AWS::Logs::LogGroup` resource specifies a log group\. A log group defines common properties for log streams, such as their retention and access control rules\. Each log stream must belong to one log group\.

You can create up to 5000 log groups per account\. You must use the following guidelines when naming a log group:
+ Log group names must be unique within a Region for an AWS account\.
+ Log group names can be between 1 and 512 characters long\.
+ Log group names consist of the following characters: a\-z, A\-Z, 0\-9, '\_' \(underscore\), '\-' \(hyphen\), '/' \(forward slash\), and '\.' \(period\)\.

## Syntax<a name="aws-resource-logs-loggroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-logs-loggroup-syntax.json"></a>

```
{
  "Type" : "AWS::Logs::LogGroup",
  "Properties" : {
      "[KmsKeyId](#cfn-logs-loggroup-kmskeyid)" : String,
      "[LogGroupName](#cfn-logs-loggroup-loggroupname)" : String,
      "[RetentionInDays](#cfn-logs-loggroup-retentionindays)" : Integer
    }
}
```

### YAML<a name="aws-resource-logs-loggroup-syntax.yaml"></a>

```
Type: AWS::Logs::LogGroup
Properties: 
  [KmsKeyId](#cfn-logs-loggroup-kmskeyid): String
  [LogGroupName](#cfn-logs-loggroup-loggroupname): String
  [RetentionInDays](#cfn-logs-loggroup-retentionindays): Integer
```

## Properties<a name="aws-resource-logs-loggroup-properties"></a>

`KmsKeyId`  <a name="cfn-logs-loggroup-kmskeyid"></a>
The Amazon Resource Name \(ARN\) of the CMK to use when encrypting log data\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogGroupName`  <a name="cfn-logs-loggroup-loggroupname"></a>
The name of the log group\. If you don't specify a name, AWS CloudFormation generates a unique ID for the log group\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\.\-_/#A-Za-z0-9]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RetentionInDays`  <a name="cfn-logs-loggroup-retentionindays"></a>
The number of days to retain the log events in the specified log group\. Possible values are: 1, 3, 5, 7, 14, 30, 60, 90, 120, 150, 180, 365, 400, 545, 731, 1827, and 3653\.  
If you omit `retentionInDays` in a `PutRetentionPolicy` operation, the events in the log group are always retained and never expire\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-logs-loggroup-return-values"></a>

### Ref<a name="aws-resource-logs-loggroup-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-logs-loggroup-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-logs-loggroup-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the log group, such as `arn:aws:logs:us-west-1:123456789012:log-group:/mystack-testgroup-12ABC1AB12A1:*`

## Examples<a name="aws-resource-logs-loggroup--examples"></a>



### Create a Log Group<a name="aws-resource-logs-loggroup--examples--Create_a_Log_Group"></a>

The following example creates a log group that retains events for 7 days\.

#### JSON<a name="aws-resource-logs-loggroup--examples--Create_a_Log_Group--json"></a>

```
"myLogGroup": {
    "Type": "AWS::Logs::LogGroup",
    "Properties": {
        "RetentionInDays": 7
    }
}
```

#### YAML<a name="aws-resource-logs-loggroup--examples--Create_a_Log_Group--yaml"></a>

```
myLogGroup: 
  Type: AWS::Logs::LogGroup
  Properties: 
    RetentionInDays: 7
```