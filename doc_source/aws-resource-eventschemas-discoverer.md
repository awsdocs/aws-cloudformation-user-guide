# AWS::EventSchemas::Discoverer<a name="aws-resource-eventschemas-discoverer"></a>

Use the `AWS::EventSchemas::Discoverer` resource to specify a *discoverer* that is associated with an event bus\. A discoverer allows the Amazon EventBridge Schema Registry to automatically generate schemas based on events on an event bus\. 

## Syntax<a name="aws-resource-eventschemas-discoverer-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-eventschemas-discoverer-syntax.json"></a>

```
{
  "Type" : "AWS::EventSchemas::Discoverer",
  "Properties" : {
      "[Description](#cfn-eventschemas-discoverer-description)" : String,
      "[SourceArn](#cfn-eventschemas-discoverer-sourcearn)" : String,
      "[Tags](#cfn-eventschemas-discoverer-tags)" : [ TagsEntry, ... ]
    }
}
```

### YAML<a name="aws-resource-eventschemas-discoverer-syntax.yaml"></a>

```
Type: AWS::EventSchemas::Discoverer
Properties: 
  [Description](#cfn-eventschemas-discoverer-description): String
  [SourceArn](#cfn-eventschemas-discoverer-sourcearn): String
  [Tags](#cfn-eventschemas-discoverer-tags): 
    - TagsEntry
```

## Properties<a name="aws-resource-eventschemas-discoverer-properties"></a>

`Description`  <a name="cfn-eventschemas-discoverer-description"></a>
A description for the discoverer\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceArn`  <a name="cfn-eventschemas-discoverer-sourcearn"></a>
The ARN of the event bus\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-eventschemas-discoverer-tags"></a>
Tags associated with the resource\.  
*Required*: No  
*Type*: List of [TagsEntry](aws-properties-eventschemas-discoverer-tagsentry.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-eventschemas-discoverer-return-values"></a>

### Ref<a name="aws-resource-eventschemas-discoverer-return-values-ref"></a>

When you provide the logical ID of this resource to the `Ref` intrinsic function, `Ref` returns the ARN of the discoverer\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-eventschemas-discoverer-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-eventschemas-discoverer-return-values-fn--getatt-fn--getatt"></a>

`DiscovererArn`  <a name="DiscovererArn-fn::getatt"></a>
The ARN of the discoverer\.

`DiscovererId`  <a name="DiscovererId-fn::getatt"></a>
The ID of the discoverer\.

## Examples<a name="aws-resource-eventschemas-discoverer--examples"></a>

### Generate Schemas for Events on the Default Event Bus<a name="aws-resource-eventschemas-discoverer--examples--Generate_Schemas_for_Events_on_the_Default_Event_Bus"></a>

#### YAML<a name="aws-resource-eventschemas-discoverer--examples--Generate_Schemas_for_Events_on_the_Default_Event_Bus--yaml"></a>

```
Resources:
  MyDiscoverer:
    Type: AWS::EventSchemas::Discoverer
    Properties:
      SourceArn: 'arn:aws:events:us-west-2:012345678910:event-bus/default'
      Description: 'discover all custom schemas'
```