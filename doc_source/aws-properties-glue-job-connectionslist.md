# AWS Glue Job ConnectionsList<a name="aws-properties-glue-job-connectionslist"></a>

<a name="aws-properties-glue-job-connectionslist-description"></a>The `ConnectionsList` property type specifies the connections that are used by an AWS Glue job\.

<a name="aws-properties-glue-job-connectionslist-inheritance"></a> `ConnectionsList` is the property type for the `Connections` property of the [AWS::Glue::Job](aws-resource-glue-job.md) resource\.

## Syntax<a name="aws-properties-glue-job-connectionslist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-job-connectionslist-syntax.json"></a>

```
{
  "[Connections](#cfn-glue-job-connectionslist-connections)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-glue-job-connectionslist-syntax.yaml"></a>

```
[Connections](#cfn-glue-job-connectionslist-connections): 
  - String
```

## Properties<a name="aws-properties-glue-job-connectionslist-properties"></a>

For more information, see [ConnectionsList Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-jobs-job.html#aws-glue-api-jobs-job-ConnectionsList) in the *AWS Glue Developer Guide*\.

`Connections`  <a name="cfn-glue-job-connectionslist-connections"></a>
A list of UTF\-8 strings that specifies the connections that are used by the job\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 