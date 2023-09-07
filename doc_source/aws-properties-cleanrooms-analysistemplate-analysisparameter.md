# AWS::CleanRooms::AnalysisTemplate AnalysisParameter<a name="aws-properties-cleanrooms-analysistemplate-analysisparameter"></a>

Optional\. The member who can query can provide this placeholder for a literal data value in an analysis template\.

## Syntax<a name="aws-properties-cleanrooms-analysistemplate-analysisparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cleanrooms-analysistemplate-analysisparameter-syntax.json"></a>

```
{
  "[DefaultValue](#cfn-cleanrooms-analysistemplate-analysisparameter-defaultvalue)" : String,
  "[Name](#cfn-cleanrooms-analysistemplate-analysisparameter-name)" : String,
  "[Type](#cfn-cleanrooms-analysistemplate-analysisparameter-type)" : String
}
```

### YAML<a name="aws-properties-cleanrooms-analysistemplate-analysisparameter-syntax.yaml"></a>

```
  [DefaultValue](#cfn-cleanrooms-analysistemplate-analysisparameter-defaultvalue): String
  [Name](#cfn-cleanrooms-analysistemplate-analysisparameter-name): String
  [Type](#cfn-cleanrooms-analysistemplate-analysisparameter-type): String
```

## Properties<a name="aws-properties-cleanrooms-analysistemplate-analysisparameter-properties"></a>

`DefaultValue`  <a name="cfn-cleanrooms-analysistemplate-analysisparameter-defaultvalue"></a>
Optional\. The default value that is applied in the analysis template\. The member who can query can override this value in the query editor\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `250`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-cleanrooms-analysistemplate-analysisparameter-name"></a>
The name of the parameter\. The name must use only alphanumeric, underscore \(\_\), or hyphen \(\-\) characters but cannot start or end with a hyphen\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `[0-9a-zA-Z_]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-cleanrooms-analysistemplate-analysisparameter-type"></a>
The type of parameter\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `BIGINT | BOOLEAN | CHAR | DATE | DECIMAL | DOUBLE_PRECISION | INTEGER | REAL | SMALLINT | TIME | TIMESTAMP | TIMESTAMPTZ | TIMETZ | VARBYTE | VARCHAR`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)