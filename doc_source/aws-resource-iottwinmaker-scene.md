# AWS::IoTTwinMaker::Scene<a name="aws-resource-iottwinmaker-scene"></a>

Use the `AWS::IoTTwinMaker::Scene` resource to declare a scene\.

## Syntax<a name="aws-resource-iottwinmaker-scene-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iottwinmaker-scene-syntax.json"></a>

```
{
  "Type" : "AWS::IoTTwinMaker::Scene",
  "Properties" : {
      "[Capabilities](#cfn-iottwinmaker-scene-capabilities)" : [ String, ... ],
      "[ContentLocation](#cfn-iottwinmaker-scene-contentlocation)" : String,
      "[Description](#cfn-iottwinmaker-scene-description)" : String,
      "[SceneId](#cfn-iottwinmaker-scene-sceneid)" : String,
      "[Tags](#cfn-iottwinmaker-scene-tags)" : {Key : Value, ...},
      "[WorkspaceId](#cfn-iottwinmaker-scene-workspaceid)" : String
    }
}
```

### YAML<a name="aws-resource-iottwinmaker-scene-syntax.yaml"></a>

```
Type: AWS::IoTTwinMaker::Scene
Properties: 
  [Capabilities](#cfn-iottwinmaker-scene-capabilities): 
    - String
  [ContentLocation](#cfn-iottwinmaker-scene-contentlocation): String
  [Description](#cfn-iottwinmaker-scene-description): String
  [SceneId](#cfn-iottwinmaker-scene-sceneid): String
  [Tags](#cfn-iottwinmaker-scene-tags): 
    Key : Value
  [WorkspaceId](#cfn-iottwinmaker-scene-workspaceid): String
```

## Properties<a name="aws-resource-iottwinmaker-scene-properties"></a>

`Capabilities`  <a name="cfn-iottwinmaker-scene-capabilities"></a>
A list of capabilities that the scene uses to render\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ContentLocation`  <a name="cfn-iottwinmaker-scene-contentlocation"></a>
The relative path that specifies the location of the content definition file\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-iottwinmaker-scene-description"></a>
The description of this scene\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SceneId`  <a name="cfn-iottwinmaker-scene-sceneid"></a>
The scene ID\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-iottwinmaker-scene-tags"></a>
The ComponentType tags\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WorkspaceId`  <a name="cfn-iottwinmaker-scene-workspaceid"></a>
The ID of the workspace\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-iottwinmaker-scene-return-values"></a>

### Ref<a name="aws-resource-iottwinmaker-scene-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the workspace Id and the sence Id\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-iottwinmaker-scene-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iottwinmaker-scene-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The scene ARN\.

`CreationDateTime`  <a name="CreationDateTime-fn::getatt"></a>
The date and time when the scene was created\.

`UpdateDateTime`  <a name="UpdateDateTime-fn::getatt"></a>
The scene the update time\.