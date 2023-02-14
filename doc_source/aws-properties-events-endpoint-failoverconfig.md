# AWS::Events::Endpoint FailoverConfig<a name="aws-properties-events-endpoint-failoverconfig"></a>

The failover configuration for an endpoint\. This includes what triggers failover and what happens when it's triggered\.

## Syntax<a name="aws-properties-events-endpoint-failoverconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-endpoint-failoverconfig-syntax.json"></a>

```
{
  "[Primary](#cfn-events-endpoint-failoverconfig-primary)" : Primary,
  "[Secondary](#cfn-events-endpoint-failoverconfig-secondary)" : Secondary
}
```

### YAML<a name="aws-properties-events-endpoint-failoverconfig-syntax.yaml"></a>

```
  [Primary](#cfn-events-endpoint-failoverconfig-primary): 
    Primary
  [Secondary](#cfn-events-endpoint-failoverconfig-secondary): 
    Secondary
```

## Properties<a name="aws-properties-events-endpoint-failoverconfig-properties"></a>

`Primary`  <a name="cfn-events-endpoint-failoverconfig-primary"></a>
The main Region of the endpoint\.  
*Required*: Yes  
*Type*: [Primary](aws-properties-events-endpoint-primary.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Secondary`  <a name="cfn-events-endpoint-failoverconfig-secondary"></a>
The Region that events are routed to when failover is triggered or event replication is enabled\.  
*Required*: Yes  
*Type*: [Secondary](aws-properties-events-endpoint-secondary.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)