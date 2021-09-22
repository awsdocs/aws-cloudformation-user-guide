# AWS::HealthLake::FHIRDatastore PreloadDataConfig<a name="aws-properties-healthlake-fhirdatastore-preloaddataconfig"></a>

Optional parameter to preload data upon creation of the Data Store\. Currently, the only supported preloaded data is synthetic data generated from Synthea\.

## Syntax<a name="aws-properties-healthlake-fhirdatastore-preloaddataconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-healthlake-fhirdatastore-preloaddataconfig-syntax.json"></a>

```
{
  "[PreloadDataType](#cfn-healthlake-fhirdatastore-preloaddataconfig-preloaddatatype)" : String
}
```

### YAML<a name="aws-properties-healthlake-fhirdatastore-preloaddataconfig-syntax.yaml"></a>

```
  [PreloadDataType](#cfn-healthlake-fhirdatastore-preloaddataconfig-preloaddatatype): String
```

## Properties<a name="aws-properties-healthlake-fhirdatastore-preloaddataconfig-properties"></a>

`PreloadDataType`  <a name="cfn-healthlake-fhirdatastore-preloaddataconfig-preloaddatatype"></a>
The type of preloaded data\. Only Synthea preloaded data is supported\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `SYNTHEA`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)