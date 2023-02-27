# AWS::Connect::QuickConnect<a name="aws-resource-connect-quickconnect"></a>

Specifies a quick connect for an Amazon Connect instance\.

## Syntax<a name="aws-resource-connect-quickconnect-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-connect-quickconnect-syntax.json"></a>

```
{
  "Type" : "AWS::Connect::QuickConnect",
  "Properties" : {
      "[Description](#cfn-connect-quickconnect-description)" : String,
      "[InstanceArn](#cfn-connect-quickconnect-instancearn)" : String,
      "[Name](#cfn-connect-quickconnect-name)" : String,
      "[QuickConnectConfig](#cfn-connect-quickconnect-quickconnectconfig)" : QuickConnectConfig,
      "[Tags](#cfn-connect-quickconnect-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-connect-quickconnect-syntax.yaml"></a>

```
Type: AWS::Connect::QuickConnect
Properties: 
  [Description](#cfn-connect-quickconnect-description): String
  [InstanceArn](#cfn-connect-quickconnect-instancearn): String
  [Name](#cfn-connect-quickconnect-name): String
  [QuickConnectConfig](#cfn-connect-quickconnect-quickconnectconfig): 
    QuickConnectConfig
  [Tags](#cfn-connect-quickconnect-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-connect-quickconnect-properties"></a>

`Description`  <a name="cfn-connect-quickconnect-description"></a>
The description of the quick connect\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `250`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceArn`  <a name="cfn-connect-quickconnect-instancearn"></a>
The Amazon Resource Name \(ARN\) of the instance\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-connect-quickconnect-name"></a>
The name of the quick connect\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `127`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QuickConnectConfig`  <a name="cfn-connect-quickconnect-quickconnectconfig"></a>
Contains information about the quick connect\.  
*Required*: Yes  
*Type*: [QuickConnectConfig](aws-properties-connect-quickconnect-quickconnectconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-connect-quickconnect-tags"></a>
The tags used to organize, track, or control access for this resource\. For example, \{ "tags": \{"key1":"value1", "key2":"value2"\} \}\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-connect-quickconnect-return-values"></a>

### Ref<a name="aws-resource-connect-quickconnect-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the quick connect name\. For example:

`{ "Ref": "myQuickConnectName" }`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-connect-quickconnect-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-connect-quickconnect-return-values-fn--getatt-fn--getatt"></a>

`QuickConnectArn`  <a name="QuickConnectArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the quick connect\.