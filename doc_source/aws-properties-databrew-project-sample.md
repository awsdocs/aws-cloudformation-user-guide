# AWS::DataBrew::Project Sample<a name="aws-properties-databrew-project-sample"></a>

Represents the sample size and sampling type for DataBrew to use for interactive data analysis\.

## Syntax<a name="aws-properties-databrew-project-sample-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-databrew-project-sample-syntax.json"></a>

```
{
  "[Size](#cfn-databrew-project-sample-size)" : Integer,
  "[Type](#cfn-databrew-project-sample-type)" : String
}
```

### YAML<a name="aws-properties-databrew-project-sample-syntax.yaml"></a>

```
  [Size](#cfn-databrew-project-sample-size): Integer
  [Type](#cfn-databrew-project-sample-type): String
```

## Properties<a name="aws-properties-databrew-project-sample-properties"></a>

`Size`  <a name="cfn-databrew-project-sample-size"></a>
The number of rows in the sample\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `5000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-databrew-project-sample-type"></a>
The way in which DataBrew obtains rows from a dataset\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `FIRST_N | LAST_N | RANDOM`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)