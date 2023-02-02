# AWS::Events::Endpoint RoutingConfig<a name="aws-properties-events-endpoint-routingconfig"></a>

The routing configuration of the endpoint\.

## Syntax<a name="aws-properties-events-endpoint-routingconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-endpoint-routingconfig-syntax.json"></a>

```
{
  "[FailoverConfig](#cfn-events-endpoint-routingconfig-failoverconfig)" : FailoverConfig
}
```

### YAML<a name="aws-properties-events-endpoint-routingconfig-syntax.yaml"></a>

```
  [FailoverConfig](#cfn-events-endpoint-routingconfig-failoverconfig): 
    FailoverConfig
```

## Properties<a name="aws-properties-events-endpoint-routingconfig-properties"></a>

`FailoverConfig`  <a name="cfn-events-endpoint-routingconfig-failoverconfig"></a>
The failover configuration for an endpoint\. This includes what triggers failover and what happens when it's triggered\.  
*Required*: Yes  
*Type*: [FailoverConfig](aws-properties-events-endpoint-failoverconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)