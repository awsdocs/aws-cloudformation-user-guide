# AWS::Glue::Crawler SchemaChangePolicy<a name="aws-properties-glue-crawler-schemachangepolicy"></a>

The policy that specifies update and delete behaviors for the crawler\. The policy tells the crawler what to do in the event that it detects a change in a table that already exists in the customer's database at the time of the crawl\. The `SchemaChangePolicy` does not affect whether or how new tables and partitions are added\. New tables and partitions are always created regardless of the `SchemaChangePolicy` on a crawler\.

The SchemaChangePolicy consists of two components, `UpdateBehavior` and `DeleteBehavior`\.

## Syntax<a name="aws-properties-glue-crawler-schemachangepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-crawler-schemachangepolicy-syntax.json"></a>

```
{
  "[DeleteBehavior](#cfn-glue-crawler-schemachangepolicy-deletebehavior)" : String,
  "[UpdateBehavior](#cfn-glue-crawler-schemachangepolicy-updatebehavior)" : String
}
```

### YAML<a name="aws-properties-glue-crawler-schemachangepolicy-syntax.yaml"></a>

```
  [DeleteBehavior](#cfn-glue-crawler-schemachangepolicy-deletebehavior): String
  [UpdateBehavior](#cfn-glue-crawler-schemachangepolicy-updatebehavior): String
```

## Properties<a name="aws-properties-glue-crawler-schemachangepolicy-properties"></a>

`DeleteBehavior`  <a name="cfn-glue-crawler-schemachangepolicy-deletebehavior"></a>
The deletion behavior when the crawler finds a deleted object\.  
A value of `LOG` specifies that if a table or partition is found to no longer exist, do not delete it, only log that it was found to no longer exist\.  
A value of `DELETE_FROM_DATABASE` specifies that if a table or partition is found to have been removed, delete it from the database\.  
A value of `DEPRECATE_IN_DATABASE` specifies that if a table has been found to no longer exist, to add a property to the table that says "DEPRECATED" and includes a timestamp with the time of deprecation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UpdateBehavior`  <a name="cfn-glue-crawler-schemachangepolicy-updatebehavior"></a>
The update behavior when the crawler finds a changed schema\.  
A value of `LOG` specifies that if a table or a partition already exists, and a change is detected, do not update it, only log that a change was detected\. Add new tables and new partitions \(including on existing tables\)\.  
A value of `UPDATE_IN_DATABASE` specifies that if a table or partition already exists, and a change is detected, update it\. Add new tables and partitions\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)