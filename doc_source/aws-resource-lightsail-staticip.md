# AWS::Lightsail::StaticIp<a name="aws-resource-lightsail-staticip"></a>

The `AWS::Lightsail::StaticIp` resource specifies a static IP that can be attached to an Amazon Lightsail instance that is in the same AWS Region and Availability Zone\.

## Syntax<a name="aws-resource-lightsail-staticip-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lightsail-staticip-syntax.json"></a>

```
{
  "Type" : "AWS::Lightsail::StaticIp",
  "Properties" : {
      "[AttachedTo](#cfn-lightsail-staticip-attachedto)" : String,
      "[StaticIpName](#cfn-lightsail-staticip-staticipname)" : String
    }
}
```

### YAML<a name="aws-resource-lightsail-staticip-syntax.yaml"></a>

```
Type: AWS::Lightsail::StaticIp
Properties: 
  [AttachedTo](#cfn-lightsail-staticip-attachedto): String
  [StaticIpName](#cfn-lightsail-staticip-staticipname): String
```

## Properties<a name="aws-resource-lightsail-staticip-properties"></a>

`AttachedTo`  <a name="cfn-lightsail-staticip-attachedto"></a>
The instance that the static IP is attached to\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StaticIpName`  <a name="cfn-lightsail-staticip-staticipname"></a>
The name of the static IP\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-lightsail-staticip-return-values"></a>

### Ref<a name="aws-resource-lightsail-staticip-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a unique identifier for this resource\.

### Fn::GetAtt<a name="aws-resource-lightsail-staticip-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-lightsail-staticip-return-values-fn--getatt-fn--getatt"></a>

`IpAddress`  <a name="IpAddress-fn::getatt"></a>
The IP address of the static IP\.

`IsAttached`  <a name="IsAttached-fn::getatt"></a>
A Boolean value indicating whether the static IP is attached to an instance\.

`StaticIpArn`  <a name="StaticIpArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the static IP \(for example, `arn:aws:lightsail:us-east-2:123456789101:StaticIp/244ad76f-8aad-4741-809f-12345EXAMPLE`\)\.

## Remarks<a name="aws-resource-lightsail-staticip--remarks"></a>

*An instance must be in a running state to attach a static IP*

To attach a static IP to an instance, the instance must be in a `running` state\. If the instance does not come to `running` state within 15 minutes after performing an attach static IP request, the attach static IP request times\-out\.

*You can attach only one static IP to an instance*

You can attach one static IP to a single instance\. You cannot attach multiple static IPs to one instance\. If multiple static IPs have the same instance in the `AttachedTo` parameter, the behavior is unpredictable and any of the static IPs \(but only one\) could be attached to the instance\. This will cause the stack to drift because only one of the static IPs will be attached to the instance but the template will show multiple\.