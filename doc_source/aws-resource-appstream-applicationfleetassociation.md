# AWS::AppStream::ApplicationFleetAssociation<a name="aws-resource-appstream-applicationfleetassociation"></a>

This resource associates the specified application with the specified fleet\. This is only supported for Elastic fleets\.

## Syntax<a name="aws-resource-appstream-applicationfleetassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appstream-applicationfleetassociation-syntax.json"></a>

```
{
  "Type" : "AWS::AppStream::ApplicationFleetAssociation",
  "Properties" : {
      "[ApplicationArn](#cfn-appstream-applicationfleetassociation-applicationarn)" : String,
      "[FleetName](#cfn-appstream-applicationfleetassociation-fleetname)" : String
    }
}
```

### YAML<a name="aws-resource-appstream-applicationfleetassociation-syntax.yaml"></a>

```
Type: AWS::AppStream::ApplicationFleetAssociation
Properties: 
  [ApplicationArn](#cfn-appstream-applicationfleetassociation-applicationarn): String
  [FleetName](#cfn-appstream-applicationfleetassociation-fleetname): String
```

## Properties<a name="aws-resource-appstream-applicationfleetassociation-properties"></a>

`ApplicationArn`  <a name="cfn-appstream-applicationfleetassociation-applicationarn"></a>
The ARN of the application\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^arn:aws(?:\-cn|\-iso\-b|\-iso|\-us\-gov)?:[A-Za-z0-9][A-Za-z0-9_/.-]{0,62}:[A-Za-z0-9_/.-]{0,63}:[A-Za-z0-9_/.-]{0,63}:[A-Za-z0-9][A-Za-z0-9:_/+=,@.\\-]{0,1023}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FleetName`  <a name="cfn-appstream-applicationfleetassociation-fleetname"></a>
The name of the fleet\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-appstream-applicationfleetassociation-return-values"></a>

### Ref<a name="aws-resource-appstream-applicationfleetassociation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a combination of the `FleetName` and `ApplicationArn`, such as `aabcdefgFleet|arn:aws:appstream:us-west-2:123456789123:application/abcdefg`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.