# AWS::Config::RemediationConfiguration RemediationParameterValue<a name="aws-properties-config-remediationconfiguration-remediationparametervalue"></a>

The value is either a dynamic \(resource\) value or a static value\. You must select either a dynamic value or a static value\.

## Syntax<a name="aws-properties-config-remediationconfiguration-remediationparametervalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-config-remediationconfiguration-remediationparametervalue-syntax.json"></a>

```
{
  "[ResourceValue](#cfn-config-remediationconfiguration-remediationparametervalue-resourcevalue)" : [ResourceValue](aws-properties-config-remediationconfiguration-resourcevalue.md),
  "[StaticValue](#cfn-config-remediationconfiguration-remediationparametervalue-staticvalue)" : [StaticValue](aws-properties-config-remediationconfiguration-staticvalue.md)
}
```

### YAML<a name="aws-properties-config-remediationconfiguration-remediationparametervalue-syntax.yaml"></a>

```
  [ResourceValue](#cfn-config-remediationconfiguration-remediationparametervalue-resourcevalue): 
    [ResourceValue](aws-properties-config-remediationconfiguration-resourcevalue.md)
  [StaticValue](#cfn-config-remediationconfiguration-remediationparametervalue-staticvalue): 
    [StaticValue](aws-properties-config-remediationconfiguration-staticvalue.md)
```

## Properties<a name="aws-properties-config-remediationconfiguration-remediationparametervalue-properties"></a>

`ResourceValue`  <a name="cfn-config-remediationconfiguration-remediationparametervalue-resourcevalue"></a>
The value is dynamic and changes at run\-time\.  
*Required*: No  
*Type*: [ResourceValue](aws-properties-config-remediationconfiguration-resourcevalue.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StaticValue`  <a name="cfn-config-remediationconfiguration-remediationparametervalue-staticvalue"></a>
The value is static and does not change at run\-time\.  
*Required*: No  
*Type*: [StaticValue](aws-properties-config-remediationconfiguration-staticvalue.md)  
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
