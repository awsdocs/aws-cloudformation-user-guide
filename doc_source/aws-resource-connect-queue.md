# AWS::Connect::Queue<a name="aws-resource-connect-queue"></a>

Contains information about a queue\.

## Syntax<a name="aws-resource-connect-queue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-connect-queue-syntax.json"></a>

```
{
  "Type" : "AWS::Connect::Queue",
  "Properties" : {
      "[Description](#cfn-connect-queue-description)" : String,
      "[HoursOfOperationArn](#cfn-connect-queue-hoursofoperationarn)" : String,
      "[InstanceArn](#cfn-connect-queue-instancearn)" : String,
      "[MaxContacts](#cfn-connect-queue-maxcontacts)" : Integer,
      "[Name](#cfn-connect-queue-name)" : String,
      "[OutboundCallerConfig](#cfn-connect-queue-outboundcallerconfig)" : OutboundCallerConfig,
      "[QuickConnectArns](#cfn-connect-queue-quickconnectarns)" : [ String, ... ],
      "[Status](#cfn-connect-queue-status)" : String,
      "[Tags](#cfn-connect-queue-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-connect-queue-syntax.yaml"></a>

```
Type: AWS::Connect::Queue
Properties: 
  [Description](#cfn-connect-queue-description): String
  [HoursOfOperationArn](#cfn-connect-queue-hoursofoperationarn): String
  [InstanceArn](#cfn-connect-queue-instancearn): String
  [MaxContacts](#cfn-connect-queue-maxcontacts): Integer
  [Name](#cfn-connect-queue-name): String
  [OutboundCallerConfig](#cfn-connect-queue-outboundcallerconfig): 
    OutboundCallerConfig
  [QuickConnectArns](#cfn-connect-queue-quickconnectarns): 
    - String
  [Status](#cfn-connect-queue-status): String
  [Tags](#cfn-connect-queue-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-connect-queue-properties"></a>

`Description`  <a name="cfn-connect-queue-description"></a>
The description of the queue\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `250`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HoursOfOperationArn`  <a name="cfn-connect-queue-hoursofoperationarn"></a>
The Amazon Resource Name \(ARN\) of the hours of operation\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceArn`  <a name="cfn-connect-queue-instancearn"></a>
The identifier of the Amazon Connect instance\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxContacts`  <a name="cfn-connect-queue-maxcontacts"></a>
The maximum number of contacts that can be in the queue before it is considered full\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-connect-queue-name"></a>
The name of the queue\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `127`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutboundCallerConfig`  <a name="cfn-connect-queue-outboundcallerconfig"></a>
The outbound caller ID name, number, and outbound whisper flow\.  
*Required*: No  
*Type*: [OutboundCallerConfig](aws-properties-connect-queue-outboundcallerconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QuickConnectArns`  <a name="cfn-connect-queue-quickconnectarns"></a>
The Amazon Resource Names \(ARN\) of the of the quick connects available to agents who are working the queue\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-connect-queue-status"></a>
The status of the queue\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-connect-queue-tags"></a>
The tags used to organize, track, or control access for this resource\. For example, \{ "tags": \{"key1":"value1", "key2":"value2"\} \}\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-connect-queue-return-values"></a>

### Ref<a name="aws-resource-connect-queue-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the queue name\. For example:

`{ "Ref": "myQueueName" }`

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-connect-queue-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-connect-queue-return-values-fn--getatt-fn--getatt"></a>

`QueueArn`  <a name="QueueArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the queue\.

`Type`  <a name="Type-fn::getatt"></a>
The type of queue\.