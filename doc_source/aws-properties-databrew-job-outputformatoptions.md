# AWS::DataBrew::Job OutputFormatOptions<a name="aws-properties-databrew-job-outputformatoptions"></a>

Represents a set of options that define the structure of comma\-separated \(CSV\) job output\.

## Syntax<a name="aws-properties-databrew-job-outputformatoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-databrew-job-outputformatoptions-syntax.json"></a>

```
{
  "[Csv](#cfn-databrew-job-outputformatoptions-csv)" : CsvOutputOptions
}
```

### YAML<a name="aws-properties-databrew-job-outputformatoptions-syntax.yaml"></a>

```
  [Csv](#cfn-databrew-job-outputformatoptions-csv): 
    CsvOutputOptions
```

## Properties<a name="aws-properties-databrew-job-outputformatoptions-properties"></a>

`Csv`  <a name="cfn-databrew-job-outputformatoptions-csv"></a>
Represents a set of options that define the structure of comma\-separated value \(CSV\) job output\.  
*Required*: No  
*Type*: [CsvOutputOptions](aws-properties-databrew-job-csvoutputoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)