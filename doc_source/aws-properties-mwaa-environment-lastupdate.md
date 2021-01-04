# AWS::MWAA::Environment LastUpdate<a name="aws-properties-mwaa-environment-lastupdate"></a>

Last update information for the environment\.

## Syntax<a name="aws-properties-mwaa-environment-lastupdate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mwaa-environment-lastupdate-syntax.json"></a>

```
{
  "[CreatedAt](#cfn-mwaa-environment-lastupdate-createdat)" : String,
  "[Error](#cfn-mwaa-environment-lastupdate-error)" : UpdateError,
  "[Status](#cfn-mwaa-environment-lastupdate-status)" : String
}
```

### YAML<a name="aws-properties-mwaa-environment-lastupdate-syntax.yaml"></a>

```
  [CreatedAt](#cfn-mwaa-environment-lastupdate-createdat): String
  [Error](#cfn-mwaa-environment-lastupdate-error): 
    UpdateError
  [Status](#cfn-mwaa-environment-lastupdate-status): String
```

## Properties<a name="aws-properties-mwaa-environment-lastupdate-properties"></a>

`CreatedAt`  <a name="cfn-mwaa-environment-lastupdate-createdat"></a>
Time that last update occurred\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Error`  <a name="cfn-mwaa-environment-lastupdate-error"></a>
Error string of last update, if applicable\.  
*Required*: No  
*Type*: [UpdateError](aws-properties-mwaa-environment-updateerror.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-mwaa-environment-lastupdate-status"></a>
Status of last update of SUCCESS, FAILED, CREATING, DELETING\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)