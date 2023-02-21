# AWS::CustomerProfiles::Integration<a name="aws-resource-customerprofiles-integration"></a>

Specifies an Amazon Connect Customer Profiles Integration\.

## Syntax<a name="aws-resource-customerprofiles-integration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-customerprofiles-integration-syntax.json"></a>

```
{
  "Type" : "AWS::CustomerProfiles::Integration",
  "Properties" : {
      "[DomainName](#cfn-customerprofiles-integration-domainname)" : String,
      "[FlowDefinition](#cfn-customerprofiles-integration-flowdefinition)" : FlowDefinition,
      "[ObjectTypeName](#cfn-customerprofiles-integration-objecttypename)" : String,
      "[ObjectTypeNames](#cfn-customerprofiles-integration-objecttypenames)" : [ ObjectTypeMapping, ... ],
      "[Tags](#cfn-customerprofiles-integration-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Uri](#cfn-customerprofiles-integration-uri)" : String
    }
}
```

### YAML<a name="aws-resource-customerprofiles-integration-syntax.yaml"></a>

```
Type: AWS::CustomerProfiles::Integration
Properties: 
  [DomainName](#cfn-customerprofiles-integration-domainname): String
  [FlowDefinition](#cfn-customerprofiles-integration-flowdefinition): 
    FlowDefinition
  [ObjectTypeName](#cfn-customerprofiles-integration-objecttypename): String
  [ObjectTypeNames](#cfn-customerprofiles-integration-objecttypenames): 
    - ObjectTypeMapping
  [Tags](#cfn-customerprofiles-integration-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Uri](#cfn-customerprofiles-integration-uri): String
```

## Properties<a name="aws-resource-customerprofiles-integration-properties"></a>

`DomainName`  <a name="cfn-customerprofiles-integration-domainname"></a>
The unique name of the domain\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FlowDefinition`  <a name="cfn-customerprofiles-integration-flowdefinition"></a>
The configuration that controls how Customer Profiles retrieves data from the source\.  
*Required*: No  
*Type*: [FlowDefinition](aws-properties-customerprofiles-integration-flowdefinition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ObjectTypeName`  <a name="cfn-customerprofiles-integration-objecttypename"></a>
The name of the profile object type mapping to use\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ObjectTypeNames`  <a name="cfn-customerprofiles-integration-objecttypenames"></a>
The object type mapping\.  
*Required*: No  
*Type*: List of [ObjectTypeMapping](aws-properties-customerprofiles-integration-objecttypemapping.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-customerprofiles-integration-tags"></a>
The tags used to organize, track, or control access for this resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Uri`  <a name="cfn-customerprofiles-integration-uri"></a>
The URI of the S3 bucket or any other type of data source\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-customerprofiles-integration-return-values"></a>

### Ref<a name="aws-resource-customerprofiles-integration-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the DomainName and the Uri of the integration\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-customerprofiles-integration-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-customerprofiles-integration-return-values-fn--getatt-fn--getatt"></a>

`CreatedAt`  <a name="CreatedAt-fn::getatt"></a>
The timestamp of when the integration was created\.

`LastUpdatedAt`  <a name="LastUpdatedAt-fn::getatt"></a>
The timestamp of when the integration was most recently edited\.

## Examples<a name="aws-resource-customerprofiles-integration--examples"></a>

The following example creates an integration if Domain existed\.

### <a name="aws-resource-customerprofiles-integration--examples--"></a>

#### YAML<a name="aws-resource-customerprofiles-integration--examples----yaml"></a>

```
Type: "AWS::CustomerProfiles::Integration"
Properties: 
    DomainName: "ExampleDomain" 
    ObjectTypeName: "CTR" 
    Uri: "arn:aws:connect:us-east-1:123456789012:instance/11111111-1111-1111-1111-111111111111"
```

#### JSON<a name="aws-resource-customerprofiles-integration--examples----json"></a>

```
"Type": "AWS::CustomerProfiles::Integration", 
"Properties": { 
    "DomainName": "ExampleDomain",
    "ObjectTypeName": "CTR", 
    "Uri": "arn:aws:connect:us-east-1:123456789012:instance/11111111-1111-1111-1111-111111111111" } } }
}
```