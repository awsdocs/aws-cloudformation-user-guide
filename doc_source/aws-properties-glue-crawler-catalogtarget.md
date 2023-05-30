# AWS::Glue::Crawler CatalogTarget<a name="aws-properties-glue-crawler-catalogtarget"></a>

Specifies an AWS Glue Data Catalog target\.

## Syntax<a name="aws-properties-glue-crawler-catalogtarget-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-crawler-catalogtarget-syntax.json"></a>

```
{
  "[ConnectionName](#cfn-glue-crawler-catalogtarget-connectionname)" : String,
  "[DatabaseName](#cfn-glue-crawler-catalogtarget-databasename)" : String,
  "[DlqEventQueueArn](#cfn-glue-crawler-catalogtarget-dlqeventqueuearn)" : String,
  "[EventQueueArn](#cfn-glue-crawler-catalogtarget-eventqueuearn)" : String,
  "[Tables](#cfn-glue-crawler-catalogtarget-tables)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-glue-crawler-catalogtarget-syntax.yaml"></a>

```
  [ConnectionName](#cfn-glue-crawler-catalogtarget-connectionname): String
  [DatabaseName](#cfn-glue-crawler-catalogtarget-databasename): String
  [DlqEventQueueArn](#cfn-glue-crawler-catalogtarget-dlqeventqueuearn): String
  [EventQueueArn](#cfn-glue-crawler-catalogtarget-eventqueuearn): String
  [Tables](#cfn-glue-crawler-catalogtarget-tables): 
    - String
```

## Properties<a name="aws-properties-glue-crawler-catalogtarget-properties"></a>

`ConnectionName`  <a name="cfn-glue-crawler-catalogtarget-connectionname"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatabaseName`  <a name="cfn-glue-crawler-catalogtarget-databasename"></a>
The name of the database to be synchronized\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DlqEventQueueArn`  <a name="cfn-glue-crawler-catalogtarget-dlqeventqueuearn"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventQueueArn`  <a name="cfn-glue-crawler-catalogtarget-eventqueuearn"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tables`  <a name="cfn-glue-crawler-catalogtarget-tables"></a>
A list of the tables to be synchronized\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)