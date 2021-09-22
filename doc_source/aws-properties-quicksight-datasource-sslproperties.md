# AWS::QuickSight::DataSource SslProperties<a name="aws-properties-quicksight-datasource-sslproperties"></a>

Secure Socket Layer \(SSL\) properties that apply when Amazon QuickSight connects to your underlying data source\.

## Syntax<a name="aws-properties-quicksight-datasource-sslproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-datasource-sslproperties-syntax.json"></a>

```
{
  "[DisableSsl](#cfn-quicksight-datasource-sslproperties-disablessl)" : Boolean
}
```

### YAML<a name="aws-properties-quicksight-datasource-sslproperties-syntax.yaml"></a>

```
  [DisableSsl](#cfn-quicksight-datasource-sslproperties-disablessl): Boolean
```

## Properties<a name="aws-properties-quicksight-datasource-sslproperties-properties"></a>

`DisableSsl`  <a name="cfn-quicksight-datasource-sslproperties-disablessl"></a>
A Boolean option to control whether SSL should be disabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)