# AWS::Glue::Job ConnectionsList<a name="aws-properties-glue-job-connectionslist"></a>

Specifies the connections used by a job\.

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

`Connections`  <a name="cfn-glue-job-connectionslist-connections"></a>
A list of connections used by the job\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)