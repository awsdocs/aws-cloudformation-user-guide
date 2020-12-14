# AWS::Lambda::Version ProvisionedConcurrencyConfiguration<a name="aws-properties-lambda-version-provisionedconcurrencyconfiguration"></a>

A provisioned concurrency configuration for a function's version\.

## Syntax<a name="aws-properties-lambda-version-provisionedconcurrencyconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-version-provisionedconcurrencyconfiguration-syntax.json"></a>

```
{
  "[ProvisionedConcurrentExecutions](#cfn-lambda-version-provisionedconcurrencyconfiguration-provisionedconcurrentexecutions)" : Integer
}
```

### YAML<a name="aws-properties-lambda-version-provisionedconcurrencyconfiguration-syntax.yaml"></a>

```
  [ProvisionedConcurrentExecutions](#cfn-lambda-version-provisionedconcurrencyconfiguration-provisionedconcurrentexecutions): Integer
```

## Properties<a name="aws-properties-lambda-version-provisionedconcurrencyconfiguration-properties"></a>

`ProvisionedConcurrentExecutions`  <a name="cfn-lambda-version-provisionedconcurrencyconfiguration-provisionedconcurrentexecutions"></a>
The amount of provisioned concurrency to allocate for the version\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-lambda-version-provisionedconcurrencyconfiguration--examples"></a>



### Provisioned Concurrency Configuration<a name="aws-properties-lambda-version-provisionedconcurrencyconfiguration--examples--Provisioned_Concurrency_Configuration"></a>

Allocate 20 provisioned concurrency for a version\.

#### YAML<a name="aws-properties-lambda-version-provisionedconcurrencyconfiguration--examples--Provisioned_Concurrency_Configuration--yaml"></a>

```
      ProvisionedConcurrencyConfig:
        ProvisionedConcurrentExecutions: 20
```