# AWS::HealthLake::FHIRDatastore<a name="aws-resource-healthlake-fhirdatastore"></a>

Creates a Data Store that can ingest and export FHIR formatted data\.

**Important**  
Please note that when a user tries to do an Update operation via CloudFormation, changes to the Data Store name, Type Version, PreloadDataConfig, or SSEConfiguration will delete their existing Data Store for the stack and create a new one\. This will lead to potential loss of data\. 

## Syntax<a name="aws-resource-healthlake-fhirdatastore-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-healthlake-fhirdatastore-syntax.json"></a>

```
{
  "Type" : "AWS::HealthLake::FHIRDatastore",
  "Properties" : {
      "[DatastoreName](#cfn-healthlake-fhirdatastore-datastorename)" : String,
      "[DatastoreTypeVersion](#cfn-healthlake-fhirdatastore-datastoretypeversion)" : String,
      "[PreloadDataConfig](#cfn-healthlake-fhirdatastore-preloaddataconfig)" : PreloadDataConfig,
      "[SseConfiguration](#cfn-healthlake-fhirdatastore-sseconfiguration)" : SseConfiguration,
      "[Tags](#cfn-healthlake-fhirdatastore-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-healthlake-fhirdatastore-syntax.yaml"></a>

```
Type: AWS::HealthLake::FHIRDatastore
Properties: 
  [DatastoreName](#cfn-healthlake-fhirdatastore-datastorename): String
  [DatastoreTypeVersion](#cfn-healthlake-fhirdatastore-datastoretypeversion): String
  [PreloadDataConfig](#cfn-healthlake-fhirdatastore-preloaddataconfig): 
    PreloadDataConfig
  [SseConfiguration](#cfn-healthlake-fhirdatastore-sseconfiguration): 
    SseConfiguration
  [Tags](#cfn-healthlake-fhirdatastore-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-healthlake-fhirdatastore-properties"></a>

`DatastoreName`  <a name="cfn-healthlake-fhirdatastore-datastorename"></a>
The user generated name for the Data Store\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^([\p{L}\p{Z}\p{N}_.:/=+\-%@]*)$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DatastoreTypeVersion`  <a name="cfn-healthlake-fhirdatastore-datastoretypeversion"></a>
The FHIR version of the Data Store\. The only supported version is R4\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `R4`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PreloadDataConfig`  <a name="cfn-healthlake-fhirdatastore-preloaddataconfig"></a>
The preloaded data configuration for the Data Store\. Only data preloaded from Synthea is supported\.  
*Required*: No  
*Type*: [PreloadDataConfig](aws-properties-healthlake-fhirdatastore-preloaddataconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SseConfiguration`  <a name="cfn-healthlake-fhirdatastore-sseconfiguration"></a>
 The server\-side encryption key configuration for a customer provided encryption key specified for creating a Data Store\.   
*Required*: No  
*Type*: [SseConfiguration](aws-properties-healthlake-fhirdatastore-sseconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-healthlake-fhirdatastore-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-healthlake-fhirdatastore-return-values"></a>

### Ref<a name="aws-resource-healthlake-fhirdatastore-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-healthlake-fhirdatastore-return-values-fn--getatt"></a>

#### <a name="aws-resource-healthlake-fhirdatastore-return-values-fn--getatt-fn--getatt"></a>

`CreatedAt`  <a name="CreatedAt-fn::getatt"></a>
Property description not available\.

`CreatedAt.Nanos`  <a name="CreatedAt.Nanos-fn::getatt"></a>
Property description not available\.

`CreatedAt.Seconds`  <a name="CreatedAt.Seconds-fn::getatt"></a>
Property description not available\.

`DatastoreArn`  <a name="DatastoreArn-fn::getatt"></a>
The Data Store ARN is generated during the creation of the Data Store and can be found in the output from the initial Data Store creation request\.

`DatastoreEndpoint`  <a name="DatastoreEndpoint-fn::getatt"></a>
The endpoint for the created Data Store\.

`DatastoreId`  <a name="DatastoreId-fn::getatt"></a>
The Amazon generated Data Store id\. This id is in the output from the initial Data Store creation call\.

`DatastoreStatus`  <a name="DatastoreStatus-fn::getatt"></a>
The status of the FHIR Data Store\. Possible statuses are ‘CREATING’, ‘ACTIVE’, ‘DELETING’, ‘DELETED’\.