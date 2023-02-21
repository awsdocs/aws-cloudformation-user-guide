# AWS::IoTTwinMaker::ComponentType<a name="aws-resource-iottwinmaker-componenttype"></a>

Use the `AWS::IoTTwinMaker::ComponentType` resource to declare a component type\.

## Syntax<a name="aws-resource-iottwinmaker-componenttype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iottwinmaker-componenttype-syntax.json"></a>

```
{
  "Type" : "AWS::IoTTwinMaker::ComponentType",
  "Properties" : {
      "[ComponentTypeId](#cfn-iottwinmaker-componenttype-componenttypeid)" : String,
      "[Description](#cfn-iottwinmaker-componenttype-description)" : String,
      "[ExtendsFrom](#cfn-iottwinmaker-componenttype-extendsfrom)" : [ String, ... ],
      "[Functions](#cfn-iottwinmaker-componenttype-functions)" : {Key : Value, ...},
      "[IsSingleton](#cfn-iottwinmaker-componenttype-issingleton)" : Boolean,
      "[PropertyDefinitions](#cfn-iottwinmaker-componenttype-propertydefinitions)" : {Key : Value, ...},
      "[PropertyGroups](#cfn-iottwinmaker-componenttype-propertygroups)" : {Key : Value, ...},
      "[Tags](#cfn-iottwinmaker-componenttype-tags)" : {Key : Value, ...},
      "[WorkspaceId](#cfn-iottwinmaker-componenttype-workspaceid)" : String
    }
}
```

### YAML<a name="aws-resource-iottwinmaker-componenttype-syntax.yaml"></a>

```
Type: AWS::IoTTwinMaker::ComponentType
Properties: 
  [ComponentTypeId](#cfn-iottwinmaker-componenttype-componenttypeid): String
  [Description](#cfn-iottwinmaker-componenttype-description): String
  [ExtendsFrom](#cfn-iottwinmaker-componenttype-extendsfrom): 
    - String
  [Functions](#cfn-iottwinmaker-componenttype-functions): 
    Key : Value
  [IsSingleton](#cfn-iottwinmaker-componenttype-issingleton): Boolean
  [PropertyDefinitions](#cfn-iottwinmaker-componenttype-propertydefinitions): 
    Key : Value
  [PropertyGroups](#cfn-iottwinmaker-componenttype-propertygroups): 
    Key : Value
  [Tags](#cfn-iottwinmaker-componenttype-tags): 
    Key : Value
  [WorkspaceId](#cfn-iottwinmaker-componenttype-workspaceid): String
```

## Properties<a name="aws-resource-iottwinmaker-componenttype-properties"></a>

`ComponentTypeId`  <a name="cfn-iottwinmaker-componenttype-componenttypeid"></a>
The ID of the component type\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-iottwinmaker-componenttype-description"></a>
The description of the component type\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExtendsFrom`  <a name="cfn-iottwinmaker-componenttype-extendsfrom"></a>
The name of the parent component type that this component type extends\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Functions`  <a name="cfn-iottwinmaker-componenttype-functions"></a>
An object that maps strings to the functions in the component type\. Each string in the mapping must be unique to this object\.  
For information on the FunctionResponse object see the [FunctionResponse](https://docs.aws.amazon.com/iot-twinmaker/latest/apireference/API_FunctionResponse.html) API reference\.  
*Required*: No  
*Type*: Map of [Function](aws-properties-iottwinmaker-componenttype-function.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsSingleton`  <a name="cfn-iottwinmaker-componenttype-issingleton"></a>
A boolean value that specifies whether an entity can have more than one component of this type\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PropertyDefinitions`  <a name="cfn-iottwinmaker-componenttype-propertydefinitions"></a>
An object that maps strings to the property definitions in the component type\. Each string in the mapping must be unique to this object\.  
For information about the PropertyDefinitionResponse object, see the [PropertyDefinitionResponse](https://docs.aws.amazon.com/iot-twinmaker/latest/apireference/API_PropertyDefinitionResponse.html) API reference\.  
*Required*: No  
*Type*: Map of [PropertyDefinition](aws-properties-iottwinmaker-componenttype-propertydefinition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PropertyGroups`  <a name="cfn-iottwinmaker-componenttype-propertygroups"></a>
An object that maps strings to the property groups in the component type\. Each string in the mapping must be unique to this object\.  
*Required*: No  
*Type*: Map of [PropertyGroup](aws-properties-iottwinmaker-componenttype-propertygroup.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iottwinmaker-componenttype-tags"></a>
The ComponentType tags\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WorkspaceId`  <a name="cfn-iottwinmaker-componenttype-workspaceid"></a>
The ID of the workspace\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-iottwinmaker-componenttype-return-values"></a>

### Ref<a name="aws-resource-iottwinmaker-componenttype-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the workspace Id and the ComponentType Id\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-iottwinmaker-componenttype-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iottwinmaker-componenttype-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the component type\.

`CreationDateTime`  <a name="CreationDateTime-fn::getatt"></a>
The date and time when the component type was created\.

`IsAbstract`  <a name="IsAbstract-fn::getatt"></a>
A boolean value that specifies whether the component type is abstract\.

`IsSchemaInitialized`  <a name="IsSchemaInitialized-fn::getatt"></a>
A boolean value that specifies whether the component type has a schema initializer and that the schema initializer has run\.

`Status`  <a name="Status-fn::getatt"></a>
Property description not available\.

`Status.Error`  <a name="Status.Error-fn::getatt"></a>
Property description not available\.

`Status.Error.Code`  <a name="Status.Error.Code-fn::getatt"></a>
Property description not available\.

`Status.Error.Message`  <a name="Status.Error.Message-fn::getatt"></a>
Property description not available\.

`Status.State`  <a name="Status.State-fn::getatt"></a>
Property description not available\.

`UpdateDateTime`  <a name="UpdateDateTime-fn::getatt"></a>
The component type the update time\.