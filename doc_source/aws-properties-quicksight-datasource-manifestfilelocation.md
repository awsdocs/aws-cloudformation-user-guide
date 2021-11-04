# AWS::QuickSight::DataSource ManifestFileLocation<a name="aws-properties-quicksight-datasource-manifestfilelocation"></a>

Amazon S3 manifest file location\.

## Syntax<a name="aws-properties-quicksight-datasource-manifestfilelocation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-datasource-manifestfilelocation-syntax.json"></a>

```
{
  "[Bucket](#cfn-quicksight-datasource-manifestfilelocation-bucket)" : String,
  "[Key](#cfn-quicksight-datasource-manifestfilelocation-key)" : String
}
```

### YAML<a name="aws-properties-quicksight-datasource-manifestfilelocation-syntax.yaml"></a>

```
  [Bucket](#cfn-quicksight-datasource-manifestfilelocation-bucket): String
  [Key](#cfn-quicksight-datasource-manifestfilelocation-key): String
```

## Properties<a name="aws-properties-quicksight-datasource-manifestfilelocation-properties"></a>

`Bucket`  <a name="cfn-quicksight-datasource-manifestfilelocation-bucket"></a>
Amazon S3 bucket\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Key`  <a name="cfn-quicksight-datasource-manifestfilelocation-key"></a>
Amazon S3 key that identifies an object\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)