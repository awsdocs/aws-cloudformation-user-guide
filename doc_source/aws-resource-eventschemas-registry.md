# AWS::EventSchemas::Registry<a name="aws-resource-eventschemas-registry"></a>

Use the `AWS::EventSchemas::Registry` to specify a schema registry\. Schema registries are containers for Schemas\. Registries collect and organize schemas so that your schemas are in logical groups\.

## Syntax<a name="aws-resource-eventschemas-registry-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-eventschemas-registry-syntax.json"></a>

```
{
  "Type" : "AWS::EventSchemas::Registry",
  "Properties" : {
      "[Description](#cfn-eventschemas-registry-description)" : String,
      "[RegistryName](#cfn-eventschemas-registry-registryname)" : String,
      "[Tags](#cfn-eventschemas-registry-tags)" : [ TagsEntry, ... ]
    }
}
```

### YAML<a name="aws-resource-eventschemas-registry-syntax.yaml"></a>

```
Type: AWS::EventSchemas::Registry
Properties: 
  [Description](#cfn-eventschemas-registry-description): String
  [RegistryName](#cfn-eventschemas-registry-registryname): String
  [Tags](#cfn-eventschemas-registry-tags): 
    - TagsEntry
```

## Properties<a name="aws-resource-eventschemas-registry-properties"></a>

`Description`  <a name="cfn-eventschemas-registry-description"></a>
A description of the registry to be created\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RegistryName`  <a name="cfn-eventschemas-registry-registryname"></a>
The name of the schema registry\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-eventschemas-registry-tags"></a>
Tags to associate with the registry\.  
*Required*: No  
*Type*: List of [TagsEntry](aws-properties-eventschemas-registry-tagsentry.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-eventschemas-registry-return-values"></a>

### Ref<a name="aws-resource-eventschemas-registry-return-values-ref"></a>

When you provide the logical ID of this resource to the `Ref` intrinsic function, `Ref` returns the ARN of the schema\. For example:

 `{ "Ref": "MyRegistry" }`

Returns a value similar to the following:

 `arn:aws:schemas:us-east-1:012345678901:registry/MyRegistry` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-eventschemas-registry-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-eventschemas-registry-return-values-fn--getatt-fn--getatt"></a>

`RegistryArn`  <a name="RegistryArn-fn::getatt"></a>
The ARN of the registry\.

`RegistryName`  <a name="RegistryName-fn::getatt"></a>
The name of the registry\.

## Examples<a name="aws-resource-eventschemas-registry--examples"></a>

### Create a Schema Registry for Events Emitted by AWS Step Functions<a name="aws-resource-eventschemas-registry--examples--Create_a_Schema_Registry_for_Events_Emitted_by_AWS_Step_Functions"></a>

#### YAML<a name="aws-resource-eventschemas-registry--examples--Create_a_Schema_Registry_for_Events_Emitted_by_AWS_Step_Functions--yaml"></a>

```
Resources:
  StatesSchemasRegistry:
    Type: AWS::EventSchemas::Registry
    Properties:
      Name: 'aws.states'
      Description: 'Contains the schemas of events emitted by AWS Step Functions'
```