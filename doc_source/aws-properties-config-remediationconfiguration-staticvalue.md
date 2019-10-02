# AWS::Config::RemediationConfiguration StaticValue<a name="aws-properties-config-remediationconfiguration-staticvalue"></a>

The static value of the resource\.

## Syntax<a name="aws-properties-config-remediationconfiguration-staticvalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-config-remediationconfiguration-staticvalue-syntax.json"></a>

```
{
  "[Values](#cfn-config-remediationconfiguration-staticvalue-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-config-remediationconfiguration-staticvalue-syntax.yaml"></a>

```
  [Values](#cfn-config-remediationconfiguration-staticvalue-values): 
    - String
```

## Properties<a name="aws-properties-config-remediationconfiguration-staticvalue-properties"></a>

`Values`  <a name="cfn-config-remediationconfiguration-staticvalue-values"></a>
A list of values\. For example, the ARN of the assumed role\.   
*Required*: No  
*Type*: List of String  
*Maximum*: `25`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-east-1`
- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-north-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-gov-east-1`
- `us-gov-west-1`
- `us-west-1`
- `us-west-2`
