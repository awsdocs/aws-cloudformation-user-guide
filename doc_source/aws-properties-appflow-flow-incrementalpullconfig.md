# AWS::AppFlow::Flow IncrementalPullConfig<a name="aws-properties-appflow-flow-incrementalpullconfig"></a>

 Specifies the configuration used when importing incremental records from the source\. 

## Syntax<a name="aws-properties-appflow-flow-incrementalpullconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-flow-incrementalpullconfig-syntax.json"></a>

```
{
  "[DatetimeTypeFieldName](#cfn-appflow-flow-incrementalpullconfig-datetimetypefieldname)" : String
}
```

### YAML<a name="aws-properties-appflow-flow-incrementalpullconfig-syntax.yaml"></a>

```
  [DatetimeTypeFieldName](#cfn-appflow-flow-incrementalpullconfig-datetimetypefieldname): String
```

## Properties<a name="aws-properties-appflow-flow-incrementalpullconfig-properties"></a>

`DatetimeTypeFieldName`  <a name="cfn-appflow-flow-incrementalpullconfig-datetimetypefieldname"></a>
 A field that specifies the date time or timestamp field as the criteria to use when importing incremental records from the source\.   
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)