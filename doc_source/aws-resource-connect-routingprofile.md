# AWS::Connect::RoutingProfile<a name="aws-resource-connect-routingprofile"></a>

Creates a new routing profile\.

## Syntax<a name="aws-resource-connect-routingprofile-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-connect-routingprofile-syntax.json"></a>

```
{
  "Type" : "AWS::Connect::RoutingProfile",
  "Properties" : {
      "[DefaultOutboundQueueArn](#cfn-connect-routingprofile-defaultoutboundqueuearn)" : String,
      "[Description](#cfn-connect-routingprofile-description)" : String,
      "[InstanceArn](#cfn-connect-routingprofile-instancearn)" : String,
      "[MediaConcurrencies](#cfn-connect-routingprofile-mediaconcurrencies)" : [ MediaConcurrency, ... ],
      "[Name](#cfn-connect-routingprofile-name)" : String,
      "[QueueConfigs](#cfn-connect-routingprofile-queueconfigs)" : [ RoutingProfileQueueConfig, ... ],
      "[Tags](#cfn-connect-routingprofile-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-connect-routingprofile-syntax.yaml"></a>

```
Type: AWS::Connect::RoutingProfile
Properties: 
  [DefaultOutboundQueueArn](#cfn-connect-routingprofile-defaultoutboundqueuearn): String
  [Description](#cfn-connect-routingprofile-description): String
  [InstanceArn](#cfn-connect-routingprofile-instancearn): String
  [MediaConcurrencies](#cfn-connect-routingprofile-mediaconcurrencies): 
    - MediaConcurrency
  [Name](#cfn-connect-routingprofile-name): String
  [QueueConfigs](#cfn-connect-routingprofile-queueconfigs): 
    - RoutingProfileQueueConfig
  [Tags](#cfn-connect-routingprofile-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-connect-routingprofile-properties"></a>

`DefaultOutboundQueueArn`  <a name="cfn-connect-routingprofile-defaultoutboundqueuearn"></a>
The Amazon Resource Name \(ARN\) of the default outbound queue for the routing profile\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-connect-routingprofile-description"></a>
The description of the routing profile\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `250`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceArn`  <a name="cfn-connect-routingprofile-instancearn"></a>
The identifier of the Amazon Connect instance\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MediaConcurrencies`  <a name="cfn-connect-routingprofile-mediaconcurrencies"></a>
The channels agents can handle in the Contact Control Panel \(CCP\) for this routing profile\.  
*Required*: Yes  
*Type*: List of [MediaConcurrency](aws-properties-connect-routingprofile-mediaconcurrency.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-connect-routingprofile-name"></a>
The name of the routing profile\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `127`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueueConfigs`  <a name="cfn-connect-routingprofile-queueconfigs"></a>
The inbound queues associated with the routing profile\. If no queue is added, the agent can make only outbound calls\.  
*Required*: No  
*Type*: List of [RoutingProfileQueueConfig](aws-properties-connect-routingprofile-routingprofilequeueconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-connect-routingprofile-tags"></a>
The tags used to organize, track, or control access for this resource\. For example, \{ "tags": \{"key1":"value1", "key2":"value2"\} \}\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-connect-routingprofile-return-values"></a>

### Ref<a name="aws-resource-connect-routingprofile-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the routing profile name\. For example:

`{ "Ref": "myRoutingProfileName" }`

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-connect-routingprofile-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-connect-routingprofile-return-values-fn--getatt-fn--getatt"></a>

`RoutingProfileArn`  <a name="RoutingProfileArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the routing profile\.