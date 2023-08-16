# AWS::OSIS::Pipeline<a name="aws-resource-osis-pipeline"></a>

The AWS::OSIS::Pipeline resource creates an Amazon OpenSearch Ingestion pipeline\.

## Syntax<a name="aws-resource-osis-pipeline-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-osis-pipeline-syntax.json"></a>

```
{
  "Type" : "AWS::OSIS::Pipeline",
  "Properties" : {
      "[LogPublishingOptions](#cfn-osis-pipeline-logpublishingoptions)" : LogPublishingOptions,
      "[MaxUnits](#cfn-osis-pipeline-maxunits)" : Integer,
      "[MinUnits](#cfn-osis-pipeline-minunits)" : Integer,
      "[PipelineConfigurationBody](#cfn-osis-pipeline-pipelineconfigurationbody)" : String,
      "[PipelineName](#cfn-osis-pipeline-pipelinename)" : String,
      "[Tags](#cfn-osis-pipeline-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpcOptions](#cfn-osis-pipeline-vpcoptions)" : VpcOptions
    }
}
```

### YAML<a name="aws-resource-osis-pipeline-syntax.yaml"></a>

```
Type: AWS::OSIS::Pipeline
Properties: 
  [LogPublishingOptions](#cfn-osis-pipeline-logpublishingoptions): 
    LogPublishingOptions
  [MaxUnits](#cfn-osis-pipeline-maxunits): Integer
  [MinUnits](#cfn-osis-pipeline-minunits): Integer
  [PipelineConfigurationBody](#cfn-osis-pipeline-pipelineconfigurationbody): String
  [PipelineName](#cfn-osis-pipeline-pipelinename): String
  [Tags](#cfn-osis-pipeline-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpcOptions](#cfn-osis-pipeline-vpcoptions): 
    VpcOptions
```

## Properties<a name="aws-resource-osis-pipeline-properties"></a>

`LogPublishingOptions`  <a name="cfn-osis-pipeline-logpublishingoptions"></a>
Key\-value pairs that represent log publishing settings\.  
*Required*: No  
*Type*: [LogPublishingOptions](aws-properties-osis-pipeline-logpublishingoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxUnits`  <a name="cfn-osis-pipeline-maxunits"></a>
The maximum pipeline capacity, in Ingestion Compute Units \(ICUs\)\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinUnits`  <a name="cfn-osis-pipeline-minunits"></a>
The minimum pipeline capacity, in Ingestion Compute Units \(ICUs\)\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PipelineConfigurationBody`  <a name="cfn-osis-pipeline-pipelineconfigurationbody"></a>
The Data Prepper pipeline configuration in YAML format\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PipelineName`  <a name="cfn-osis-pipeline-pipelinename"></a>
The name of the pipeline\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-osis-pipeline-tags"></a>
List of tags to add to the pipeline upon creation\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcOptions`  <a name="cfn-osis-pipeline-vpcoptions"></a>
Options that specify the subnets and security groups for an OpenSearch Ingestion VPC endpoint\.  
*Required*: No  
*Type*: [VpcOptions](aws-properties-osis-pipeline-vpcoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-osis-pipeline-return-values"></a>

### Ref<a name="aws-resource-osis-pipeline-return-values-ref"></a>

When the logical ID of this resource is provided to the Ref intrinsic function, Ref returns the resource name, such as `mystack-abc1d2efg3h4`\. For more information about using the Ref function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-osis-pipeline-return-values-fn--getatt"></a>

GetAtt returns a value for a specified attribute of this type\. For more information, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\. The following are the available attributes and sample return values\.

#### <a name="aws-resource-osis-pipeline-return-values-fn--getatt-fn--getatt"></a>

`IngestEndpointUrls`  <a name="IngestEndpointUrls-fn::getatt"></a>
A list of the ingestion endpoints for the pipeline that you can send data to\. Currently, only a single ingestion endpoint is supported for a pipeline\. For example, `my-pipeline-123456789012.us-east-1.osis.amazonaws.com`\.

`PipelineArn`  <a name="PipelineArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the pipeline\.

`VpcEndpoints`  <a name="VpcEndpoints-fn::getatt"></a>
The VPC interface endpoints that have access to the pipeline\.

## Examples<a name="aws-resource-osis-pipeline--examples"></a>

### Create an OpenSearch Ingestion pipeline<a name="aws-resource-osis-pipeline--examples--Create_an_OpenSearch_Ingestion_pipeline"></a>

The following example creates an OpenSearch Ingestion pipeline running version 2\.x of Data Prepper with log publishing enabled\.

#### JSON<a name="aws-resource-osis-pipeline--examples--Create_an_OpenSearch_Ingestion_pipeline--json"></a>

```
{
   "Parameters": {
      "PipelineConfigurationBody": {
         "Type": "String"
      }
   },
   "Resources": {
      "OpenSearchIngestionPipeline": {
         "Type": "AWS::OSIS::Pipeline",
         "Properties": {
            "LogPublishingOptions": {
               "IsLoggingEnabled": true,
               "CloudWatchLogDestination": {
                  "LogGroup": "/aws/OpenSearchService/IngestionService/test-pipeline"
               }
            },
            "MinUnits": 3,
            "MaxUnits": 9,
            "PipelineConfigurationBody": {
               "Value": {
                  "Ref": "PipelineConfigurationBody"
               }
            },
            "PipelineName": "test-pipeline"
         }
      }
   },
   "Outputs": {
      "PipelineArn": {
         "Value": {
            "Ref": "OpenSearchIngestionPipeline"
         }
      },
      "IngestEndpointUrls": {
         "Value": {
            "Fn::Select": [
               0,
               {
                  "Fn::GetAtt": [
                     "OpenSearchIngestionPipeline",
                     "IngestEndpointUrls"
                  ]
               }
            ]
         }
      }
   }
}
```

#### YAML<a name="aws-resource-osis-pipeline--examples--Create_an_OpenSearch_Ingestion_pipeline--yaml"></a>

```
Parameters:
  PipelineConfigurationBody:
    Type: String
Resources:
  OpenSearchIngestionPipeline:
    Type: 'AWS::OSIS::Pipeline'
    Properties:
      LogPublishingOptions:
        IsLoggingEnabled: true
        CloudWatchLogDestination:
          LogGroup: /aws/vendedlogs/test-pipeline
      MinUnits: 3
      MaxUnits: 9
      PipelineConfigurationBody:
        Value:
          Ref: PipelineConfigurationBody
      PipelineName: test-pipeline
Outputs:
  PipelineArn:
    Value:
      Ref: OpenSearchIngestionPipeline
  IngestEndpointUrls:
    Value: !Select [0, !GetAtt OpenSearchIngestionPipeline.IngestEndpointUrls]
```