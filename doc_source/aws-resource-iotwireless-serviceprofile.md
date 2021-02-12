# AWS::IoTWireless::ServiceProfile<a name="aws-resource-iotwireless-serviceprofile"></a>

Creates a new service profile\.

## Syntax<a name="aws-resource-iotwireless-serviceprofile-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotwireless-serviceprofile-syntax.json"></a>

```
{
  "Type" : "AWS::IoTWireless::ServiceProfile",
  "Properties" : {
      "[LoRaWAN](#cfn-iotwireless-serviceprofile-lorawan)" : LoRaWANServiceProfile,
      "[Name](#cfn-iotwireless-serviceprofile-name)" : String,
      "[Tags](#cfn-iotwireless-serviceprofile-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-iotwireless-serviceprofile-syntax.yaml"></a>

```
Type: AWS::IoTWireless::ServiceProfile
Properties: 
  [LoRaWAN](#cfn-iotwireless-serviceprofile-lorawan): 
    LoRaWANServiceProfile
  [Name](#cfn-iotwireless-serviceprofile-name): String
  [Tags](#cfn-iotwireless-serviceprofile-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iotwireless-serviceprofile-properties"></a>

`LoRaWAN`  <a name="cfn-iotwireless-serviceprofile-lorawan"></a>
LoRaWANServiceProfile object\.  
*Required*: No  
*Type*: [LoRaWANServiceProfile](aws-properties-iotwireless-serviceprofile-lorawanserviceprofile.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-iotwireless-serviceprofile-name"></a>
The name of the new resource\. The maximum length is 256 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iotwireless-serviceprofile-tags"></a>
An array of key\-value pairs to apply to this resource\. Tags can have a minimum of 0 and a maximum of 50 items\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iotwireless-serviceprofile-return-values"></a>

### Ref<a name="aws-resource-iotwireless-serviceprofile-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the service profile ID\.

### Fn::GetAtt<a name="aws-resource-iotwireless-serviceprofile-return-values-fn--getatt"></a>

#### <a name="aws-resource-iotwireless-serviceprofile-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the service profile created\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the service profile created\.

`LoRaWANResponse`  <a name="LoRaWANResponse-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.