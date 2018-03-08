# AWS Glue Crawler SchemaChangePolicy<a name="aws-properties-glue-crawler-schemachangepolicy"></a>

<a name="aws-properties-glue-crawler-schemachangepolicy-description"></a>The `SchemaChangePolicy` property type specifies update and delete behaviors for an AWS Glue crawler\.

<a name="aws-properties-glue-crawler-schemachangepolicy-inheritance"></a> `SchemaChangePolicy` is a property of the [AWS::Glue::Crawler](aws-resource-glue-crawler.md) resource\.

## Syntax<a name="aws-properties-glue-crawler-schemachangepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-crawler-schemachangepolicy-syntax.json"></a>

```
{
  "[UpdateBehavior](#cfn-glue-crawler-schemachangepolicy-updatebehavior)" : String,
  "[DeleteBehavior](#cfn-glue-crawler-schemachangepolicy-deletebehavior)" : String
}
```

### YAML<a name="aws-properties-glue-crawler-schemachangepolicy-syntax.yaml"></a>

```
[UpdateBehavior](#cfn-glue-crawler-schemachangepolicy-updatebehavior): String
[DeleteBehavior](#cfn-glue-crawler-schemachangepolicy-deletebehavior): String
```

## Properties<a name="aws-properties-glue-crawler-schemachangepolicy-properties"></a>

For more information, see [SchemaChangePolicy Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-crawler-crawling.html#aws-glue-api-crawler-crawling-SchemaChangePolicy) in the *AWS Glue Developer Guide*\.

`UpdateBehavior`  <a name="cfn-glue-crawler-schemachangepolicy-updatebehavior"></a>
The update behavior\. Valid values are `LOG` or `UPDATE_IN_DATABASE`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DeleteBehavior`  <a name="cfn-glue-crawler-schemachangepolicy-deletebehavior"></a>
The deletion behavior\. Valid values are `LOG`, `DELETE_FROM_DATABASE`, or `DEPRECATE_IN_DATABASE`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 