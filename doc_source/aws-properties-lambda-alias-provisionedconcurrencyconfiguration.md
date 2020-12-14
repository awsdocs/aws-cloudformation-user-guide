# AWS::Lambda::Alias ProvisionedConcurrencyConfiguration<a name="aws-properties-lambda-alias-provisionedconcurrencyconfiguration"></a>

A provisioned concurrency configuration for a function's alias\.

## Syntax<a name="aws-properties-lambda-alias-provisionedconcurrencyconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-alias-provisionedconcurrencyconfiguration-syntax.json"></a>

```
{
  "[ProvisionedConcurrentExecutions](#cfn-lambda-alias-provisionedconcurrencyconfiguration-provisionedconcurrentexecutions)" : Integer
}
```

### YAML<a name="aws-properties-lambda-alias-provisionedconcurrencyconfiguration-syntax.yaml"></a>

```
  [ProvisionedConcurrentExecutions](#cfn-lambda-alias-provisionedconcurrencyconfiguration-provisionedconcurrentexecutions): Integer
```

## Properties<a name="aws-properties-lambda-alias-provisionedconcurrencyconfiguration-properties"></a>

`ProvisionedConcurrentExecutions`  <a name="cfn-lambda-alias-provisionedconcurrencyconfiguration-provisionedconcurrentexecutions"></a>
The amount of provisioned concurrency to allocate for the alias\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-lambda-alias-provisionedconcurrencyconfiguration--examples"></a>



### Provisioned Concurrency<a name="aws-properties-lambda-alias-provisionedconcurrencyconfiguration--examples--Provisioned_Concurrency"></a>

An alias with 20 provisioned concurrency\.

#### YAML<a name="aws-properties-lambda-alias-provisionedconcurrencyconfiguration--examples--Provisioned_Concurrency--yaml"></a>

```
  alias:
    Type: AWS::Lambda::Alias
    Properties:
      FunctionName: !Ref function
      FunctionVersion: !GetAtt newVersion.Version
      Name: BLUE
      ProvisionedConcurrencyConfig:
        ProvisionedConcurrentExecutions: 20
```