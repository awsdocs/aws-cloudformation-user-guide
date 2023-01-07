# AWS::GroundStation::Config<a name="aws-resource-groundstation-config"></a>

 Creates a `Config` with the specified parameters\. 

 Config objects provide Ground Station with the details necessary in order to schedule and execute satellite contacts\. 

## Syntax<a name="aws-resource-groundstation-config-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-groundstation-config-syntax.json"></a>

```
{
  "Type" : "AWS::GroundStation::Config",
  "Properties" : {
      "[ConfigData](#cfn-groundstation-config-configdata)" : ConfigData,
      "[Name](#cfn-groundstation-config-name)" : String,
      "[Tags](#cfn-groundstation-config-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-groundstation-config-syntax.yaml"></a>

```
Type: AWS::GroundStation::Config
Properties: 
  [ConfigData](#cfn-groundstation-config-configdata): 
    ConfigData
  [Name](#cfn-groundstation-config-name): String
  [Tags](#cfn-groundstation-config-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-groundstation-config-properties"></a>

`ConfigData`  <a name="cfn-groundstation-config-configdata"></a>
 Object containing the parameters of a config\. Only one subtype may be specified per config\. See the subtype definitions for a description of each config subtype\.   
*Required*: Yes  
*Type*: [ConfigData](aws-properties-groundstation-config-configdata.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-groundstation-config-name"></a>
 The name of the config object\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-groundstation-config-tags"></a>
 Tags assigned to a resource\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-groundstation-config-return-values"></a>

### Ref<a name="aws-resource-groundstation-config-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the config\. For example: 

 `{ "Ref": "Config" }` 

 For the Ground Station config, `Ref` returns the ARN of the config\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-groundstation-config-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-groundstation-config-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the config, such as `arn:aws:groundstation:us-east-2:1234567890:config/tracking/9940bf3b-d2ba-427e-9906-842b5e5d2296`\. 

`Id`  <a name="Id-fn::getatt"></a>
The ID of the config, such as `9940bf3b-d2ba-427e-9906-842b5e5d2296`\. 

`Type`  <a name="Type-fn::getatt"></a>
The type of the config, such as `tracking`\. 