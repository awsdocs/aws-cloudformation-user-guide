# AWS::Glue::Crawler SchemaChangePolicy<a name="aws-properties-glue-crawler-schemachangepolicy"></a>

A policy that specifies update and deletion behaviors for the crawler\.

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
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UpdateBehavior`  <a name="cfn-glue-crawler-schemachangepolicy-updatebehavior"></a>
The update behavior when the crawler finds a changed schema\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)