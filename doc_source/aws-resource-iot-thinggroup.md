# AWS::IoT::ThingGroup<a name="aws-resource-iot-thinggroup"></a>

Creates a new thing group\. A dynamic thing group is created if the resource template contains the `QueryString` attribute\. A dynamic thing group will not contain the `ParentGroupName` attribute\. A static thing group and dynamic thing group can't be converted to each other via the addition or removal of the `QueryString` attribute\.

**Note**  
This is a control plane operation\. See [Authorization](https://docs.aws.amazon.com/iot/latest/developerguide/iot-authorization.html) for information about authorizing control plane actions\.

Requires permission to access the [CreateThingGroup](https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions) action\.

## Syntax<a name="aws-resource-iot-thinggroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iot-thinggroup-syntax.json"></a>

```
{
  "Type" : "AWS::IoT::ThingGroup",
  "Properties" : {
      "[ParentGroupName](#cfn-iot-thinggroup-parentgroupname)" : String,
      "[QueryString](#cfn-iot-thinggroup-querystring)" : String,
      "[Tags](#cfn-iot-thinggroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[ThingGroupName](#cfn-iot-thinggroup-thinggroupname)" : String,
      "[ThingGroupProperties](#cfn-iot-thinggroup-thinggroupproperties)" : ThingGroupProperties
    }
}
```

### YAML<a name="aws-resource-iot-thinggroup-syntax.yaml"></a>

```
Type: AWS::IoT::ThingGroup
Properties: 
  [ParentGroupName](#cfn-iot-thinggroup-parentgroupname): String
  [QueryString](#cfn-iot-thinggroup-querystring): 
    String
  [Tags](#cfn-iot-thinggroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [ThingGroupName](#cfn-iot-thinggroup-thinggroupname): String
  [ThingGroupProperties](#cfn-iot-thinggroup-thinggroupproperties): 
    ThingGroupProperties
```

## Properties<a name="aws-resource-iot-thinggroup-properties"></a>

`ParentGroupName`  <a name="cfn-iot-thinggroup-parentgroupname"></a>
The parent thing group name\.  
A Dynamic Thing Group does not have `parentGroupName` defined\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`QueryString`  <a name="cfn-iot-thinggroup-querystring"></a>
The dynamic thing group search query string\.  
The `queryString` attribute *is* required for `CreateDynamicThingGroup`\. The `queryString` attribute *is not* required for `CreateThingGroup`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iot-thinggroup-tags"></a>
Metadata which can be used to manage the thing group or dynamic thing group\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThingGroupName`  <a name="cfn-iot-thinggroup-thinggroupname"></a>
The thing group name\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ThingGroupProperties`  <a name="cfn-iot-thinggroup-thinggroupproperties"></a>
Thing group properties\.  
*Required*: No  
*Type*: [ThingGroupProperties](aws-properties-iot-thinggroup-thinggroupproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iot-thinggroup-return-values"></a>

### Ref<a name="aws-resource-iot-thinggroup-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the thing group id\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-iot-thinggroup-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iot-thinggroup-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The thing group ARN\.

`Id`  <a name="Id-fn::getatt"></a>
The thing group ID\.