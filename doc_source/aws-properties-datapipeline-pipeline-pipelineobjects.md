# AWS Data Pipeline PipelineObject<a name="aws-properties-datapipeline-pipeline-pipelineobjects"></a>

`PipelineObjects` is a property of the [AWS::DataPipeline::Pipeline](aws-resource-datapipeline-pipeline.md) resource that describes a data pipeline object\.

## Syntax<a name="w3ab2c21c14d566b5"></a>

### JSON<a name="aws-properties-datapipeline-pipeline-pipelineobjects-syntax.json"></a>

```
{
  "[Fields](#cfn-datapipeline-pipeline-pipelineobjects-fields)" : [ Field type ],
  "[Id](#cfn-datapipeline-pipeline-pipelineobjects-id)" : String,
  "[Name](#cfn-datapipeline-pipeline-pipelineobjects-name)" : String
}
```

### YAML<a name="aws-properties-datapipeline-pipeline-pipelineobjects-syntax.yaml"></a>

```
[Fields](#cfn-datapipeline-pipeline-pipelineobjects-fields):
  - Field type
[Id](#cfn-datapipeline-pipeline-pipelineobjects-id): String
[Name](#cfn-datapipeline-pipeline-pipelineobjects-name): String
```

## Properties<a name="w3ab2c21c14d566b7"></a>

`Fields`  <a name="cfn-datapipeline-pipeline-pipelineobjects-fields"></a>
Key\-value pairs that define the properties of the object\. Duplicates allowed\. You can use the same key multiple times within a field to define array attributes\.  
*Required*: Yes  
*Type*: List of [AWS Data Pipeline Pipeline Field](aws-properties-datapipeline-pipeline-pipelineobjects-fields.md)

`Id`  <a name="cfn-datapipeline-pipeline-pipelineobjects-id"></a>
Identifier of the object\.  
*Required*: Yes  
*Type*: String

`Name`  <a name="cfn-datapipeline-pipeline-pipelineobjects-name"></a>
Name of the object\.  
*Required*: Yes  
*Type*: String

## Examples<a name="aws-properties-datapipeline-pipeline-pipelineobjects-examples"></a>

### <a name="aws-properties-datapipeline-pipeline-pipelineobjects-example1"></a>

The following snippet shows how to use the same key for fields in the `PipelineObjects` property for an `AWS::DataPipeline::Pipeline` resource\.

#### JSON<a name="aws-properties-datapipeline-pipeline-pipelineobjects-example1.json"></a>

```
"PipelineObjects": [
  {
    "Id": "ResourceId_I1mCc",
    "Name": "ReleaseLabelCluster",
    "Fields": [
      {
        "Key": "releaseLabel",
        "StringValue": "emr-4.1.0"
      },
      {
        "Key": "applications",
        "StringValue": "spark"
      },
      {
        "Key": "applications",
        "StringValue": "hive"
      },
      {
        "Key": "applications",
        "StringValue": "pig"
      },
      {
        "Key": "type",
        "StringValue": "EmrCluster"
      },
      {
        "Key": "configuration",
        "RefValue": "coresite"
      }
    ]
  },
  {
    "Id": "coresite",
    "Name": "coresite",
    "Fields": [
      {
        "Key": "type",
        "StringValue": "EmrConfiguration"
      },
      {
        "Key": "classification",
        "StringValue": "core-site"
      },
      {
        "Key": "property",
        "RefValue": "io-file-buffer-size"
      },
      {
        "Key": "property",
        "RefValue": "fs-s3-block-size"
      }
    ]
  },
  ...
]
```

#### YAML<a name="aws-properties-datapipeline-pipeline-pipelineobjects-example1.yaml"></a>

```
PipelineObjects:
  - Id: ResourceId_I1mCc
    Name: ReleaseLabelCluster
    Fields:
      - Key: releaseLabel
        StringValue: emr-4.1.0
      - Key: applications
        StringValue: spark
      - Key: applications
        StringValue: hive
      - Key: applications
        StringValue: pig
      - Key: type
        StringValue: EmrCluster
      - Key: configuration
        RefValue: coresite
  - Id: coresite
    Name: coresite
    Fields:
      - Key: type
        StringValue: EmrConfiguration
      - Key: classification
        StringValue: core-site
      - Key: property
        RefValue: io-file-buffer-size
      - Key: property
        RefValue: fs-s3-block-size
  ...
```