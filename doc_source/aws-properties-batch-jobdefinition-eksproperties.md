# AWS::Batch::JobDefinition EksProperties<a name="aws-properties-batch-jobdefinition-eksproperties"></a>

An object that contains the properties for the Kubernetes resources of a job\.

## Syntax<a name="aws-properties-batch-jobdefinition-eksproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-eksproperties-syntax.json"></a>

```
{
  "[PodProperties](#cfn-batch-jobdefinition-eksproperties-podproperties)" : PodProperties
}
```

### YAML<a name="aws-properties-batch-jobdefinition-eksproperties-syntax.yaml"></a>

```
  [PodProperties](#cfn-batch-jobdefinition-eksproperties-podproperties): 
    PodProperties
```

## Properties<a name="aws-properties-batch-jobdefinition-eksproperties-properties"></a>

`PodProperties`  <a name="cfn-batch-jobdefinition-eksproperties-podproperties"></a>
The properties for the Kubernetes pod resources of a job\.  
*Required*: No  
*Type*: [PodProperties](aws-properties-batch-jobdefinition-podproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)