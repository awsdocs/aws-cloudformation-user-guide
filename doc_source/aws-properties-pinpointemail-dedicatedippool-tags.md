# AWS::PinpointEmail::DedicatedIpPool Tags<a name="aws-properties-pinpointemail-dedicatedippool-tags"></a>

An object that defines the tags \(keys and values\) that you want to associate with the dedicated IP pool\.

## Syntax<a name="aws-properties-pinpointemail-dedicatedippool-tags-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pinpointemail-dedicatedippool-tags-syntax.json"></a>

```
{
  "[Key](#cfn-pinpointemail-dedicatedippool-tags-key)" : String,
  "[Value](#cfn-pinpointemail-dedicatedippool-tags-value)" : String
}
```

### YAML<a name="aws-properties-pinpointemail-dedicatedippool-tags-syntax.yaml"></a>

```
  [Key](#cfn-pinpointemail-dedicatedippool-tags-key): String
  [Value](#cfn-pinpointemail-dedicatedippool-tags-value): String
```

## Properties<a name="aws-properties-pinpointemail-dedicatedippool-tags-properties"></a>

`Key`  <a name="cfn-pinpointemail-dedicatedippool-tags-key"></a>
One part of a key\-value pair that defines a tag\. The maximum length of a tag key is 128 characters\. The minimum length is 1 character\.  
If you specify tags for the dedicated IP pool, then this value is required\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-pinpointemail-dedicatedippool-tags-value"></a>
The optional part of a key\-value pair that defines a tag\. The maximum length of a tag value is 256 characters\. The minimum length is 0 characters\. If you don’t want a resource to have a specific tag value, don’t specify a value for this parameter\. Amazon Pinpoint will set the value to an empty string\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)