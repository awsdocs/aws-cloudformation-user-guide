# AWS::AppFlow::Connector LambdaConnectorProvisioningConfig<a name="aws-properties-appflow-connector-lambdaconnectorprovisioningconfig"></a>

Contains information about the configuration of the lambda which is being registered as the connector\.

## Syntax<a name="aws-properties-appflow-connector-lambdaconnectorprovisioningconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connector-lambdaconnectorprovisioningconfig-syntax.json"></a>

```
{
  "[LambdaArn](#cfn-appflow-connector-lambdaconnectorprovisioningconfig-lambdaarn)" : String
}
```

### YAML<a name="aws-properties-appflow-connector-lambdaconnectorprovisioningconfig-syntax.yaml"></a>

```
  [LambdaArn](#cfn-appflow-connector-lambdaconnectorprovisioningconfig-lambdaarn): String
```

## Properties<a name="aws-properties-appflow-connector-lambdaconnectorprovisioningconfig-properties"></a>

`LambdaArn`  <a name="cfn-appflow-connector-lambdaconnectorprovisioningconfig-lambdaarn"></a>
Lambda ARN of the connector being registered\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `arn:aws:.*:.*:[0-9]+:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)