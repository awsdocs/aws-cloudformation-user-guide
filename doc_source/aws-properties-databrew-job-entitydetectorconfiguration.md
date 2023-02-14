# AWS::DataBrew::Job EntityDetectorConfiguration<a name="aws-properties-databrew-job-entitydetectorconfiguration"></a>

Configuration of entity detection for a profile job\. When undefined, entity detection is disabled\.

## Syntax<a name="aws-properties-databrew-job-entitydetectorconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-databrew-job-entitydetectorconfiguration-syntax.json"></a>

```
{
  "[AllowedStatistics](#cfn-databrew-job-entitydetectorconfiguration-allowedstatistics)" : AllowedStatistics,
  "[EntityTypes](#cfn-databrew-job-entitydetectorconfiguration-entitytypes)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-databrew-job-entitydetectorconfiguration-syntax.yaml"></a>

```
  [AllowedStatistics](#cfn-databrew-job-entitydetectorconfiguration-allowedstatistics): 
    AllowedStatistics
  [EntityTypes](#cfn-databrew-job-entitydetectorconfiguration-entitytypes): 
    - String
```

## Properties<a name="aws-properties-databrew-job-entitydetectorconfiguration-properties"></a>

`AllowedStatistics`  <a name="cfn-databrew-job-entitydetectorconfiguration-allowedstatistics"></a>
Configuration of statistics that are allowed to be run on columns that contain detected entities\. When undefined, no statistics will be computed on columns that contain detected entities\.  
*Required*: No  
*Type*: [AllowedStatistics](aws-properties-databrew-job-allowedstatistics.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EntityTypes`  <a name="cfn-databrew-job-entitydetectorconfiguration-entitytypes"></a>
Entity types to detect\. Can be any of the following:  
+ USA\_SSN
+ EMAIL
+ USA\_ITIN
+ USA\_PASSPORT\_NUMBER
+ PHONE\_NUMBER
+ USA\_DRIVING\_LICENSE
+ BANK\_ACCOUNT
+ CREDIT\_CARD
+ IP\_ADDRESS
+ MAC\_ADDRESS
+ USA\_DEA\_NUMBER
+ USA\_HCPCS\_CODE
+ USA\_NATIONAL\_PROVIDER\_IDENTIFIER
+ USA\_NATIONAL\_DRUG\_CODE
+ USA\_HEALTH\_INSURANCE\_CLAIM\_NUMBER
+ USA\_MEDICARE\_BENEFICIARY\_IDENTIFIER
+ USA\_CPT\_CODE
+ PERSON\_NAME
+ DATE
The Entity type group USA\_ALL is also supported, and includes all of the above entity types except PERSON\_NAME and DATE\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)