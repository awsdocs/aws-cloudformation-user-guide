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

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
