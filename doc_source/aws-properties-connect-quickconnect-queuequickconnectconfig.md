# AWS::Connect::QuickConnect QueueQuickConnectConfig<a name="aws-properties-connect-quickconnect-queuequickconnectconfig"></a>

Contains information about a queue for a quick connect\. The flow must be of type Transfer to Queue\.

## Syntax<a name="aws-properties-connect-quickconnect-queuequickconnectconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-quickconnect-queuequickconnectconfig-syntax.json"></a>

```
{
  "[ContactFlowArn](#cfn-connect-quickconnect-queuequickconnectconfig-contactflowarn)" : String,
  "[QueueArn](#cfn-connect-quickconnect-queuequickconnectconfig-queuearn)" : String
}
```

### YAML<a name="aws-properties-connect-quickconnect-queuequickconnectconfig-syntax.yaml"></a>

```
  [ContactFlowArn](#cfn-connect-quickconnect-queuequickconnectconfig-contactflowarn): String
  [QueueArn](#cfn-connect-quickconnect-queuequickconnectconfig-queuearn): String
```

## Properties<a name="aws-properties-connect-quickconnect-queuequickconnectconfig-properties"></a>

`ContactFlowArn`  <a name="cfn-connect-quickconnect-queuequickconnectconfig-contactflowarn"></a>
The Amazon Resource Name \(ARN\) of the flow\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `500`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueueArn`  <a name="cfn-connect-quickconnect-queuequickconnectconfig-queuearn"></a>
The Amazon Resource Name \(ARN\) of the queue\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)