# AWS::EventSchemas::Schema<a name="aws-resource-eventschemas-schema"></a>

Use the `AWS::EventSchemas::Schema` resource to specify an event schema\.

## Syntax<a name="aws-resource-eventschemas-schema-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-eventschemas-schema-syntax.json"></a>

```
{
  "Type" : "AWS::EventSchemas::Schema",
  "Properties" : {
      "[Content](#cfn-eventschemas-schema-content)" : String,
      "[Description](#cfn-eventschemas-schema-description)" : String,
      "[RegistryName](#cfn-eventschemas-schema-registryname)" : String,
      "[SchemaName](#cfn-eventschemas-schema-schemaname)" : String,
      "[Tags](#cfn-eventschemas-schema-tags)" : [ TagsEntry, ... ],
      "[Type](#cfn-eventschemas-schema-type)" : String
    }
}
```

### YAML<a name="aws-resource-eventschemas-schema-syntax.yaml"></a>

```
Type: AWS::EventSchemas::Schema
Properties: 
  [Content](#cfn-eventschemas-schema-content): String
  [Description](#cfn-eventschemas-schema-description): String
  [RegistryName](#cfn-eventschemas-schema-registryname): String
  [SchemaName](#cfn-eventschemas-schema-schemaname): String
  [Tags](#cfn-eventschemas-schema-tags): 
    - TagsEntry
  [Type](#cfn-eventschemas-schema-type): String
```

## Properties<a name="aws-resource-eventschemas-schema-properties"></a>

`Content`  <a name="cfn-eventschemas-schema-content"></a>
The source of the schema definition\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-eventschemas-schema-description"></a>
A description of the schema\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RegistryName`  <a name="cfn-eventschemas-schema-registryname"></a>
The name of the schema registry\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SchemaName`  <a name="cfn-eventschemas-schema-schemaname"></a>
The name of the schema\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-eventschemas-schema-tags"></a>
Tags associated with the schema\.  
*Required*: No  
*Type*: List of [TagsEntry](aws-properties-eventschemas-schema-tagsentry.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-eventschemas-schema-type"></a>
The type of schema\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-eventschemas-schema-return-values"></a>

### Ref<a name="aws-resource-eventschemas-schema-return-values-ref"></a>

When you provide the logical ID of this resource to the `Ref` intrinsic function, `Ref` returns the ARN of the schema\. For example:

 `{ "Ref": "MySchema" }`

Returns a value similar to the following:

 `arn:aws:schemas:us-east-1:012345678901:schema/MyRegistry/MySchema` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-eventschemas-schema-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-eventschemas-schema-return-values-fn--getatt-fn--getatt"></a>

`SchemaArn`  <a name="SchemaArn-fn::getatt"></a>
The ARN of the schema\.

`SchemaName`  <a name="SchemaName-fn::getatt"></a>
The name of the schema\.

`SchemaVersion`  <a name="SchemaVersion-fn::getatt"></a>
The version number of the schema\.

## Examples<a name="aws-resource-eventschemas-schema--examples"></a>

### <a name="aws-resource-eventschemas-schema--examples--"></a>

#### YAML<a name="aws-resource-eventschemas-schema--examples----yaml"></a>

```
Resources:
  ExecutionStatusChangeSchema:
    Type: AWS::EventSchemas::Schema
    Properties:Ref
      Registry: 'aws.events'
      Name: ExecutionStatusChange
      Description: 'event emitted when the status of a state machine execution change'
      Type: OpenApi3
      Content: >
        {
          "openapi": "3.0.0",
          "info": {
            "version": "1.0.0",
            "title": "StepFunctionsExecutionStatusChange"
          },
          "components": {
            "schemas": {
              "StepFunctionsExecutionStatusChange": {
                "type": "object",
                "required": [ "output", "input", "executionArn", "name", "stateMachineArn", "startDate", "stopDate", "status" ],
                "properties": {
                  "output": {"type": "string","nullable": true},
                  "input": {"type": "string"},
                  "executionArn": {"type": "string"},
                  "name": {"type": "string"},
                  "stateMachineArn": {"type": "string"},
                  "startDate": {"type": "integer","format": "int64"},
                  "stopDate": {"type": "integer","format": "int64","nullable": true},
                  "status": {"type": "string","enum": [ "FAILED", "RUNNING", "SUCCEEDED", "ABORTED" ]}
                }
              }
            }
          }
        }
```