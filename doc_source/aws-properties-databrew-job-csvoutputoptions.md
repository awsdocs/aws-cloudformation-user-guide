# AWS::DataBrew::Job CsvOutputOptions<a name="aws-properties-databrew-job-csvoutputoptions"></a>

Represents a set of options that define how DataBrew will write a comma\-separated value \(CSV\) file\.

## Syntax<a name="aws-properties-databrew-job-csvoutputoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-databrew-job-csvoutputoptions-syntax.json"></a>

```
{
  "[Delimiter](#cfn-databrew-job-csvoutputoptions-delimiter)" : String
}
```

### YAML<a name="aws-properties-databrew-job-csvoutputoptions-syntax.yaml"></a>

```
  [Delimiter](#cfn-databrew-job-csvoutputoptions-delimiter): String
```

## Properties<a name="aws-properties-databrew-job-csvoutputoptions-properties"></a>

`Delimiter`  <a name="cfn-databrew-job-csvoutputoptions-delimiter"></a>
A single character that specifies the delimiter used to create CSV job output\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)