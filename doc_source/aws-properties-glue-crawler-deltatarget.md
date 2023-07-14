# AWS::Glue::Crawler DeltaTarget<a name="aws-properties-glue-crawler-deltatarget"></a>

Specifies a Delta data store to crawl one or more Delta tables\.

## Syntax<a name="aws-properties-glue-crawler-deltatarget-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-crawler-deltatarget-syntax.json"></a>

```
{
  "[ConnectionName](#cfn-glue-crawler-deltatarget-connectionname)" : String,
  "[CreateNativeDeltaTable](#cfn-glue-crawler-deltatarget-createnativedeltatable)" : Boolean,
  "[DeltaTables](#cfn-glue-crawler-deltatarget-deltatables)" : [ String, ... ],
  "[WriteManifest](#cfn-glue-crawler-deltatarget-writemanifest)" : Boolean
}
```

### YAML<a name="aws-properties-glue-crawler-deltatarget-syntax.yaml"></a>

```
  [ConnectionName](#cfn-glue-crawler-deltatarget-connectionname): String
  [CreateNativeDeltaTable](#cfn-glue-crawler-deltatarget-createnativedeltatable): Boolean
  [DeltaTables](#cfn-glue-crawler-deltatarget-deltatables): 
    - String
  [WriteManifest](#cfn-glue-crawler-deltatarget-writemanifest): Boolean
```

## Properties<a name="aws-properties-glue-crawler-deltatarget-properties"></a>

`ConnectionName`  <a name="cfn-glue-crawler-deltatarget-connectionname"></a>
The name of the connection to use to connect to the Delta table target\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CreateNativeDeltaTable`  <a name="cfn-glue-crawler-deltatarget-createnativedeltatable"></a>
Specifies whether the crawler will create native tables, to allow integration with query engines that support querying of the Delta transaction log directly\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeltaTables`  <a name="cfn-glue-crawler-deltatarget-deltatables"></a>
A list of the Amazon S3 paths to the Delta tables\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WriteManifest`  <a name="cfn-glue-crawler-deltatarget-writemanifest"></a>
Specifies whether to write the manifest files to the Delta table path\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)