# AWS::Config::RemediationConfiguration ExecutionControls<a name="aws-properties-config-remediationconfiguration-executioncontrols"></a>

The controls that AWS Config uses for executing remediations\.

## Syntax<a name="aws-properties-config-remediationconfiguration-executioncontrols-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-config-remediationconfiguration-executioncontrols-syntax.json"></a>

```
{
  "[SsmControls](#cfn-config-remediationconfiguration-executioncontrols-ssmcontrols)" : [SsmControls](aws-properties-config-remediationconfiguration-ssmcontrols.md)
}
```

### YAML<a name="aws-properties-config-remediationconfiguration-executioncontrols-syntax.yaml"></a>

```
  [SsmControls](#cfn-config-remediationconfiguration-executioncontrols-ssmcontrols): 
    [SsmControls](aws-properties-config-remediationconfiguration-ssmcontrols.md)
```

## Properties<a name="aws-properties-config-remediationconfiguration-executioncontrols-properties"></a>

`SsmControls`  <a name="cfn-config-remediationconfiguration-executioncontrols-ssmcontrols"></a>
A SsmControls object\.  
*Required*: No  
*Type*: [SsmControls](aws-properties-config-remediationconfiguration-ssmcontrols.md)  
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
