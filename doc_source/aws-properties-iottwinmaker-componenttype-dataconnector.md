# AWS::IoTTwinMaker::ComponentType DataConnector<a name="aws-properties-iottwinmaker-componenttype-dataconnector"></a>

The data connector\.

## Syntax<a name="aws-properties-iottwinmaker-componenttype-dataconnector-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iottwinmaker-componenttype-dataconnector-syntax.json"></a>

```
{
  "[IsNative](#cfn-iottwinmaker-componenttype-dataconnector-isnative)" : Boolean,
  "[Lambda](#cfn-iottwinmaker-componenttype-dataconnector-lambda)" : LambdaFunction
}
```

### YAML<a name="aws-properties-iottwinmaker-componenttype-dataconnector-syntax.yaml"></a>

```
  [IsNative](#cfn-iottwinmaker-componenttype-dataconnector-isnative): Boolean
  [Lambda](#cfn-iottwinmaker-componenttype-dataconnector-lambda): 
    LambdaFunction
```

## Properties<a name="aws-properties-iottwinmaker-componenttype-dataconnector-properties"></a>

`IsNative`  <a name="cfn-iottwinmaker-componenttype-dataconnector-isnative"></a>
A boolean value that specifies whether the data connector is native to IoT TwinMaker\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Lambda`  <a name="cfn-iottwinmaker-componenttype-dataconnector-lambda"></a>
The Lambda function associated with the data connector\.  
*Required*: No  
*Type*: [LambdaFunction](aws-properties-iottwinmaker-componenttype-lambdafunction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)