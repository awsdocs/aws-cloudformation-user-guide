# AWS::QuickSight::DataSource AmazonOpenSearchParameters<a name="aws-properties-quicksight-datasource-amazonopensearchparameters"></a>

The parameters for OpenSearch\.

## Syntax<a name="aws-properties-quicksight-datasource-amazonopensearchparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-datasource-amazonopensearchparameters-syntax.json"></a>

```
{
  "[Domain](#cfn-quicksight-datasource-amazonopensearchparameters-domain)" : String
}
```

### YAML<a name="aws-properties-quicksight-datasource-amazonopensearchparameters-syntax.yaml"></a>

```
  [Domain](#cfn-quicksight-datasource-amazonopensearchparameters-domain): String
```

## Properties<a name="aws-properties-quicksight-datasource-amazonopensearchparameters-properties"></a>

`Domain`  <a name="cfn-quicksight-datasource-amazonopensearchparameters-domain"></a>
The OpenSearch domain\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)