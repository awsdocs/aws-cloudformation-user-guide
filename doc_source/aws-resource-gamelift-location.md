# AWS::GameLift::Location<a name="aws-resource-gamelift-location"></a>

Creates a custom location for use in an Anywhere fleet\.

## Syntax<a name="aws-resource-gamelift-location-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-gamelift-location-syntax.json"></a>

```
{
  "Type" : "AWS::GameLift::Location",
  "Properties" : {
      "[LocationName](#cfn-gamelift-location-locationname)" : String,
      "[Tags](#cfn-gamelift-location-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-gamelift-location-syntax.yaml"></a>

```
Type: AWS::GameLift::Location
Properties: 
  [LocationName](#cfn-gamelift-location-locationname): String
  [Tags](#cfn-gamelift-location-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-gamelift-location-properties"></a>

`LocationName`  <a name="cfn-gamelift-location-locationname"></a>
The location's name\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `^[A-Za-z0-9\-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-gamelift-location-tags"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-gamelift-location-return-values"></a>

### Ref<a name="aws-resource-gamelift-location-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-gamelift-location-return-values-fn--getatt"></a>

#### <a name="aws-resource-gamelift-location-return-values-fn--getatt-fn--getatt"></a>

`LocationArn`  <a name="LocationArn-fn::getatt"></a>
Property description not available\.