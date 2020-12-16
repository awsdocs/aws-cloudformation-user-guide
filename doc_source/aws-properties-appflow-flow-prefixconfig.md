# AWS::AppFlow::Flow PrefixConfig<a name="aws-properties-appflow-flow-prefixconfig"></a>

 Determines the prefix that Amazon AppFlow applies to the destination folder name\. You can name your destination folders according to the flow frequency and date\. 

## Syntax<a name="aws-properties-appflow-flow-prefixconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-flow-prefixconfig-syntax.json"></a>

```
{
  "[PrefixFormat](#cfn-appflow-flow-prefixconfig-prefixformat)" : String,
  "[PrefixType](#cfn-appflow-flow-prefixconfig-prefixtype)" : String
}
```

### YAML<a name="aws-properties-appflow-flow-prefixconfig-syntax.yaml"></a>

```
  [PrefixFormat](#cfn-appflow-flow-prefixconfig-prefixformat): String
  [PrefixType](#cfn-appflow-flow-prefixconfig-prefixtype): String
```

## Properties<a name="aws-properties-appflow-flow-prefixconfig-properties"></a>

`PrefixFormat`  <a name="cfn-appflow-flow-prefixconfig-prefixformat"></a>
 Determines the format of the prefix, and whether it applies to the file name, file path, or both\.   
*Required*: No  
*Type*: String  
*Allowed values*: `DAY | HOUR | MINUTE | MONTH | YEAR`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrefixType`  <a name="cfn-appflow-flow-prefixconfig-prefixtype"></a>
 Determines the level of granularity that's included in the prefix\.   
*Required*: No  
*Type*: String  
*Allowed values*: `FILENAME | PATH | PATH_AND_FILENAME`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-flow-prefixconfig--seealso"></a>
+ [PrefixConfig](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_PrefixConfig.html) in the *Amazon AppFlow API Reference*\.

