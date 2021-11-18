# AWS::DeviceFarm::DevicePool<a name="aws-resource-devicefarm-devicepool"></a>

Represents a request to the create device pool operation\.

## Syntax<a name="aws-resource-devicefarm-devicepool-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-devicefarm-devicepool-syntax.json"></a>

```
{
  "Type" : "AWS::DeviceFarm::DevicePool",
  "Properties" : {
      "[Description](#cfn-devicefarm-devicepool-description)" : String,
      "[MaxDevices](#cfn-devicefarm-devicepool-maxdevices)" : Integer,
      "[Name](#cfn-devicefarm-devicepool-name)" : String,
      "[ProjectArn](#cfn-devicefarm-devicepool-projectarn)" : String,
      "[Rules](#cfn-devicefarm-devicepool-rules)" : [ Rule, ... ],
      "[Tags](#cfn-devicefarm-devicepool-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-devicefarm-devicepool-syntax.yaml"></a>

```
Type: AWS::DeviceFarm::DevicePool
Properties: 
  [Description](#cfn-devicefarm-devicepool-description): String
  [MaxDevices](#cfn-devicefarm-devicepool-maxdevices): Integer
  [Name](#cfn-devicefarm-devicepool-name): String
  [ProjectArn](#cfn-devicefarm-devicepool-projectarn): String
  [Rules](#cfn-devicefarm-devicepool-rules): 
    - Rule
  [Tags](#cfn-devicefarm-devicepool-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-devicefarm-devicepool-properties"></a>

`Description`  <a name="cfn-devicefarm-devicepool-description"></a>
The device pool's description\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `16384`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxDevices`  <a name="cfn-devicefarm-devicepool-maxdevices"></a>
The number of devices that Device Farm can add to your device pool\. Device Farm adds devices that are available and meet the criteria that you assign for the `rules` parameter\. Depending on how many devices meet these constraints, your device pool might contain fewer devices than the value for this parameter\.  
By specifying the maximum number of devices, you can control the costs that you incur by running tests\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-devicefarm-devicepool-name"></a>
The device pool's name\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProjectArn`  <a name="cfn-devicefarm-devicepool-projectarn"></a>
The ARN of the project for the device pool\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `32`  
*Maximum*: `1011`  
*Pattern*: `^arn:.+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Rules`  <a name="cfn-devicefarm-devicepool-rules"></a>
The device pool's rules\.  
*Required*: Yes  
*Type*: List of [Rule](aws-properties-devicefarm-devicepool-rule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-devicefarm-devicepool-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html) in the *AWS CloudFormation resource type reference guide*\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-devicefarm-devicepool-return-values"></a>

### Ref<a name="aws-resource-devicefarm-devicepool-return-values-ref"></a>

Not supported for this resource\.

### Fn::GetAtt<a name="aws-resource-devicefarm-devicepool-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-devicefarm-devicepool-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the device pool\. See [Amazon resource names](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) in the *General Reference guide*\.