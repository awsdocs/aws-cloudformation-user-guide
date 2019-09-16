# AWS::IoTThingsGraph::FlowTemplate<a name="aws-resource-iotthingsgraph-flowtemplate"></a>

Represents a workflow template\. Workflows can be created only in the user's namespace\. \(The public namespace contains only entities\.\) The workflow can contain only entities in the specified namespace\. The workflow is validated against the entities in the latest version of the user's namespace unless another namespace version is specified in the request\.

## Syntax<a name="aws-resource-iotthingsgraph-flowtemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotthingsgraph-flowtemplate-syntax.json"></a>

```
{
  "Type" : "AWS::IoTThingsGraph::FlowTemplate",
  "Properties" : {
      "[CompatibleNamespaceVersion](#cfn-iotthingsgraph-flowtemplate-compatiblenamespaceversion)" : Double,
      "[Definition](#cfn-iotthingsgraph-flowtemplate-definition)" : [DefinitionDocument](aws-properties-iotthingsgraph-flowtemplate-definitiondocument.md)
    }
}
```

### YAML<a name="aws-resource-iotthingsgraph-flowtemplate-syntax.yaml"></a>

```
Type: AWS::IoTThingsGraph::FlowTemplate
Properties: 
  [CompatibleNamespaceVersion](#cfn-iotthingsgraph-flowtemplate-compatiblenamespaceversion): Double
  [Definition](#cfn-iotthingsgraph-flowtemplate-definition): 
    [DefinitionDocument](aws-properties-iotthingsgraph-flowtemplate-definitiondocument.md)
```

## Properties<a name="aws-resource-iotthingsgraph-flowtemplate-properties"></a>

`CompatibleNamespaceVersion`  <a name="cfn-iotthingsgraph-flowtemplate-compatiblenamespaceversion"></a>
The version of the user's namespace against which the workflow was validated\. Use this value in your system instance\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Definition`  <a name="cfn-iotthingsgraph-flowtemplate-definition"></a>
A workflow's definition document\.  
*Required*: Yes  
*Type*: [DefinitionDocument](aws-properties-iotthingsgraph-flowtemplate-definitiondocument.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-iotthingsgraph-flowtemplate-return-values"></a>

### Ref<a name="aws-resource-iotthingsgraph-flowtemplate-return-values-ref"></a>

 `{ "Ref": "summary" }` 

Ref returns the `FlowTemplateSummary` that describes the workflow\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.