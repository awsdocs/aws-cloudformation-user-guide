# AWS::SageMaker::EndpointConfig ClarifyInferenceConfig<a name="aws-properties-sagemaker-endpointconfig-clarifyinferenceconfig"></a>

<a name="aws-properties-sagemaker-endpointconfig-clarifyinferenceconfig-description"></a>The `ClarifyInferenceConfig` property type specifies Property description not available\. for an [AWS::SageMaker::EndpointConfig](aws-resource-sagemaker-endpointconfig.md)\.

## Syntax<a name="aws-properties-sagemaker-endpointconfig-clarifyinferenceconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-endpointconfig-clarifyinferenceconfig-syntax.json"></a>

```
{
  "[ContentTemplate](#cfn-sagemaker-endpointconfig-clarifyinferenceconfig-contenttemplate)" : String,
  "[FeatureHeaders](#cfn-sagemaker-endpointconfig-clarifyinferenceconfig-featureheaders)" : [ ClarifyHeader, ... ],
  "[FeaturesAttribute](#cfn-sagemaker-endpointconfig-clarifyinferenceconfig-featuresattribute)" : String,
  "[FeatureTypes](#cfn-sagemaker-endpointconfig-clarifyinferenceconfig-featuretypes)" : [ ClarifyFeatureType, ... ],
  "[LabelAttribute](#cfn-sagemaker-endpointconfig-clarifyinferenceconfig-labelattribute)" : String,
  "[LabelHeaders](#cfn-sagemaker-endpointconfig-clarifyinferenceconfig-labelheaders)" : [ ClarifyHeader, ... ],
  "[LabelIndex](#cfn-sagemaker-endpointconfig-clarifyinferenceconfig-labelindex)" : Integer,
  "[MaxPayloadInMB](#cfn-sagemaker-endpointconfig-clarifyinferenceconfig-maxpayloadinmb)" : Integer,
  "[MaxRecordCount](#cfn-sagemaker-endpointconfig-clarifyinferenceconfig-maxrecordcount)" : Integer,
  "[ProbabilityAttribute](#cfn-sagemaker-endpointconfig-clarifyinferenceconfig-probabilityattribute)" : String,
  "[ProbabilityIndex](#cfn-sagemaker-endpointconfig-clarifyinferenceconfig-probabilityindex)" : Integer
}
```

### YAML<a name="aws-properties-sagemaker-endpointconfig-clarifyinferenceconfig-syntax.yaml"></a>

```
  [ContentTemplate](#cfn-sagemaker-endpointconfig-clarifyinferenceconfig-contenttemplate): String
  [FeatureHeaders](#cfn-sagemaker-endpointconfig-clarifyinferenceconfig-featureheaders): 
    - ClarifyHeader
  [FeaturesAttribute](#cfn-sagemaker-endpointconfig-clarifyinferenceconfig-featuresattribute): String
  [FeatureTypes](#cfn-sagemaker-endpointconfig-clarifyinferenceconfig-featuretypes): 
    - ClarifyFeatureType
  [LabelAttribute](#cfn-sagemaker-endpointconfig-clarifyinferenceconfig-labelattribute): String
  [LabelHeaders](#cfn-sagemaker-endpointconfig-clarifyinferenceconfig-labelheaders): 
    - ClarifyHeader
  [LabelIndex](#cfn-sagemaker-endpointconfig-clarifyinferenceconfig-labelindex): Integer
  [MaxPayloadInMB](#cfn-sagemaker-endpointconfig-clarifyinferenceconfig-maxpayloadinmb): Integer
  [MaxRecordCount](#cfn-sagemaker-endpointconfig-clarifyinferenceconfig-maxrecordcount): Integer
  [ProbabilityAttribute](#cfn-sagemaker-endpointconfig-clarifyinferenceconfig-probabilityattribute): String
  [ProbabilityIndex](#cfn-sagemaker-endpointconfig-clarifyinferenceconfig-probabilityindex): Integer
```

## Properties<a name="aws-properties-sagemaker-endpointconfig-clarifyinferenceconfig-properties"></a>

`ContentTemplate`  <a name="cfn-sagemaker-endpointconfig-clarifyinferenceconfig-contenttemplate"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FeatureHeaders`  <a name="cfn-sagemaker-endpointconfig-clarifyinferenceconfig-featureheaders"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [ClarifyHeader](aws-properties-sagemaker-endpointconfig-clarifyheader.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FeaturesAttribute`  <a name="cfn-sagemaker-endpointconfig-clarifyinferenceconfig-featuresattribute"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FeatureTypes`  <a name="cfn-sagemaker-endpointconfig-clarifyinferenceconfig-featuretypes"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [ClarifyFeatureType](aws-properties-sagemaker-endpointconfig-clarifyfeaturetype.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LabelAttribute`  <a name="cfn-sagemaker-endpointconfig-clarifyinferenceconfig-labelattribute"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LabelHeaders`  <a name="cfn-sagemaker-endpointconfig-clarifyinferenceconfig-labelheaders"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [ClarifyHeader](aws-properties-sagemaker-endpointconfig-clarifyheader.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LabelIndex`  <a name="cfn-sagemaker-endpointconfig-clarifyinferenceconfig-labelindex"></a>
Property description not available\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MaxPayloadInMB`  <a name="cfn-sagemaker-endpointconfig-clarifyinferenceconfig-maxpayloadinmb"></a>
Property description not available\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MaxRecordCount`  <a name="cfn-sagemaker-endpointconfig-clarifyinferenceconfig-maxrecordcount"></a>
Property description not available\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProbabilityAttribute`  <a name="cfn-sagemaker-endpointconfig-clarifyinferenceconfig-probabilityattribute"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProbabilityIndex`  <a name="cfn-sagemaker-endpointconfig-clarifyinferenceconfig-probabilityindex"></a>
Property description not available\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)