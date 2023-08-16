# AWS::Omics::AnnotationStore StoreOptions<a name="aws-properties-omics-annotationstore-storeoptions"></a>

The store's file parsing options\.

## Syntax<a name="aws-properties-omics-annotationstore-storeoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-omics-annotationstore-storeoptions-syntax.json"></a>

```
{
  "[TsvStoreOptions](#cfn-omics-annotationstore-storeoptions-tsvstoreoptions)" : TsvStoreOptions
}
```

### YAML<a name="aws-properties-omics-annotationstore-storeoptions-syntax.yaml"></a>

```
  [TsvStoreOptions](#cfn-omics-annotationstore-storeoptions-tsvstoreoptions): 
    TsvStoreOptions
```

## Properties<a name="aws-properties-omics-annotationstore-storeoptions-properties"></a>

`TsvStoreOptions`  <a name="cfn-omics-annotationstore-storeoptions-tsvstoreoptions"></a>
Formatting options for a TSV file\.  
*Required*: Yes  
*Type*: [TsvStoreOptions](aws-properties-omics-annotationstore-tsvstoreoptions.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)