# AWS::IoT::BillingGroup<a name="aws-resource-iot-billinggroup"></a>

Creates a new billing group\.

Requires permission to access the [CreateBillingGroup](https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions) action\.

## Syntax<a name="aws-resource-iot-billinggroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iot-billinggroup-syntax.json"></a>

```
{
  "Type" : "AWS::IoT::BillingGroup",
  "Properties" : {
      "[BillingGroupName](#cfn-iot-billinggroup-billinggroupname)" : String,
      "[BillingGroupProperties](#cfn-iot-billinggroup-billinggroupproperties)" : BillingGroupProperties,
      "[Tags](#cfn-iot-billinggroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-iot-billinggroup-syntax.yaml"></a>

```
Type: AWS::IoT::BillingGroup
Properties: 
  [BillingGroupName](#cfn-iot-billinggroup-billinggroupname): String
  [BillingGroupProperties](#cfn-iot-billinggroup-billinggroupproperties): 
    BillingGroupProperties
  [Tags](#cfn-iot-billinggroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iot-billinggroup-properties"></a>

`BillingGroupName`  <a name="cfn-iot-billinggroup-billinggroupname"></a>
The name of the billing group\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BillingGroupProperties`  <a name="cfn-iot-billinggroup-billinggroupproperties"></a>
The properties of the billing group\.  
*Required*: No  
*Type*: [BillingGroupProperties](aws-properties-iot-billinggroup-billinggroupproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iot-billinggroup-tags"></a>
Metadata which can be used to manage the billing group\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iot-billinggroup-return-values"></a>

### Ref<a name="aws-resource-iot-billinggroup-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the billing group id\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-iot-billinggroup-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iot-billinggroup-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the billing group\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the billing group\.