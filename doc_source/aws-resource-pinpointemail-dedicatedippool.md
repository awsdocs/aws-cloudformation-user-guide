# AWS::PinpointEmail::DedicatedIpPool<a name="aws-resource-pinpointemail-dedicatedippool"></a>

A request to create a new dedicated IP pool\.

## Syntax<a name="aws-resource-pinpointemail-dedicatedippool-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pinpointemail-dedicatedippool-syntax.json"></a>

```
{
  "Type" : "AWS::PinpointEmail::DedicatedIpPool",
  "Properties" : {
      "[PoolName](#cfn-pinpointemail-dedicatedippool-poolname)" : String,
      "[Tags](#cfn-pinpointemail-dedicatedippool-tags)" : [ Tags, ... ]
    }
}
```

### YAML<a name="aws-resource-pinpointemail-dedicatedippool-syntax.yaml"></a>

```
Type: AWS::PinpointEmail::DedicatedIpPool
Properties: 
  [PoolName](#cfn-pinpointemail-dedicatedippool-poolname): String
  [Tags](#cfn-pinpointemail-dedicatedippool-tags): 
    - Tags
```

## Properties<a name="aws-resource-pinpointemail-dedicatedippool-properties"></a>

`PoolName`  <a name="cfn-pinpointemail-dedicatedippool-poolname"></a>
The name of the dedicated IP pool\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-pinpointemail-dedicatedippool-tags"></a>
An object that defines the tags \(keys and values\) that you want to associate with the dedicated IP pool\.  
*Required*: No  
*Type*: [List](aws-properties-pinpointemail-dedicatedippool-tags.md) of [Tags](aws-properties-pinpointemail-dedicatedippool-tags.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-pinpointemail-dedicatedippool-return-values"></a>

### Ref<a name="aws-resource-pinpointemail-dedicatedippool-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

 `{ "Ref": "myDedicatedIpPool" }` 

For the Amazon Pinpoint dedicated IP pool `myDedicatedIpPool`, Ref returns the name of the IP pool\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.