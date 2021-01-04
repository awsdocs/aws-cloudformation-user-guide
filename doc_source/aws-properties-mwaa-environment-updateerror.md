# AWS::MWAA::Environment UpdateError<a name="aws-properties-mwaa-environment-updateerror"></a>

The error that occurred for the update\.

## Syntax<a name="aws-properties-mwaa-environment-updateerror-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mwaa-environment-updateerror-syntax.json"></a>

```
{
  "[ErrorCode](#cfn-mwaa-environment-updateerror-errorcode)" : String,
  "[ErrorMessage](#cfn-mwaa-environment-updateerror-errormessage)" : String
}
```

### YAML<a name="aws-properties-mwaa-environment-updateerror-syntax.yaml"></a>

```
  [ErrorCode](#cfn-mwaa-environment-updateerror-errorcode): String
  [ErrorMessage](#cfn-mwaa-environment-updateerror-errormessage): String
```

## Properties<a name="aws-properties-mwaa-environment-updateerror-properties"></a>

`ErrorCode`  <a name="cfn-mwaa-environment-updateerror-errorcode"></a>
The code for the error with the update\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ErrorMessage`  <a name="cfn-mwaa-environment-updateerror-errormessage"></a>
The error message associated with the update error\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)