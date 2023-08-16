# AWS::Connect::QuickConnect UserQuickConnectConfig<a name="aws-properties-connect-quickconnect-userquickconnectconfig"></a>

Contains information about the quick connect configuration settings for a user\. The contact flow must be of type Transfer to Agent\.

## Syntax<a name="aws-properties-connect-quickconnect-userquickconnectconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-quickconnect-userquickconnectconfig-syntax.json"></a>

```
{
  "[ContactFlowArn](#cfn-connect-quickconnect-userquickconnectconfig-contactflowarn)" : String,
  "[UserArn](#cfn-connect-quickconnect-userquickconnectconfig-userarn)" : String
}
```

### YAML<a name="aws-properties-connect-quickconnect-userquickconnectconfig-syntax.yaml"></a>

```
  [ContactFlowArn](#cfn-connect-quickconnect-userquickconnectconfig-contactflowarn): String
  [UserArn](#cfn-connect-quickconnect-userquickconnectconfig-userarn): String
```

## Properties<a name="aws-properties-connect-quickconnect-userquickconnectconfig-properties"></a>

`ContactFlowArn`  <a name="cfn-connect-quickconnect-userquickconnectconfig-contactflowarn"></a>
The Amazon Resource Name \(ARN\) of the flow\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `500`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserArn`  <a name="cfn-connect-quickconnect-userquickconnectconfig-userarn"></a>
The Amazon Resource Name \(ARN\) of the user\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)