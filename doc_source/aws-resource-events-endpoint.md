# AWS::Events::Endpoint<a name="aws-resource-events-endpoint"></a>

A global endpoint used to improve your application's availability by making it regional\-fault tolerant\. For more information about global endpoints, see [Making applications Regional\-fault tolerant with global endpoints and event replication](https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-global-endpoints.html) in the *Amazon EventBridge User Guide*\.

## Syntax<a name="aws-resource-events-endpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-events-endpoint-syntax.json"></a>

```
{
  "Type" : "AWS::Events::Endpoint",
  "Properties" : {
      "[Description](#cfn-events-endpoint-description)" : String,
      "[EventBuses](#cfn-events-endpoint-eventbuses)" : [ EndpointEventBus, ... ],
      "[Name](#cfn-events-endpoint-name)" : String,
      "[ReplicationConfig](#cfn-events-endpoint-replicationconfig)" : ReplicationConfig,
      "[RoleArn](#cfn-events-endpoint-rolearn)" : String,
      "[RoutingConfig](#cfn-events-endpoint-routingconfig)" : RoutingConfig
    }
}
```

### YAML<a name="aws-resource-events-endpoint-syntax.yaml"></a>

```
Type: AWS::Events::Endpoint
Properties: 
  [Description](#cfn-events-endpoint-description): String
  [EventBuses](#cfn-events-endpoint-eventbuses): 
    - EndpointEventBus
  [Name](#cfn-events-endpoint-name): String
  [ReplicationConfig](#cfn-events-endpoint-replicationconfig): 
    ReplicationConfig
  [RoleArn](#cfn-events-endpoint-rolearn): String
  [RoutingConfig](#cfn-events-endpoint-routingconfig): 
    RoutingConfig
```

## Properties<a name="aws-resource-events-endpoint-properties"></a>

`Description`  <a name="cfn-events-endpoint-description"></a>
A description for the endpoint\.  
*Required*: No  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventBuses`  <a name="cfn-events-endpoint-eventbuses"></a>
The event buses being used by the endpoint\.  
*Exactly*: `2`  
*Required*: Yes  
*Type*: List of [EndpointEventBus](aws-properties-events-endpoint-endpointeventbus.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-events-endpoint-name"></a>
The name of the endpoint\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `[\.\-_A-Za-z0-9]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ReplicationConfig`  <a name="cfn-events-endpoint-replicationconfig"></a>
Whether event replication was enabled or disabled for this endpoint\. The default state is `ENABLED` which means you must supply a `RoleArn`\. If you don't have a `RoleArn` or you don't want event replication enabled, set the state to `DISABLED`\.  
*Required*: No  
*Type*: [ReplicationConfig](aws-properties-events-endpoint-replicationconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-events-endpoint-rolearn"></a>
The ARN of the role used by event replication for the endpoint\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^arn:aws[a-z-]*:iam::\d{12}:role\/[\w+=,.@/-]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoutingConfig`  <a name="cfn-events-endpoint-routingconfig"></a>
The routing configuration of the endpoint\.  
*Required*: Yes  
*Type*: [RoutingConfig](aws-properties-events-endpoint-routingconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-events-endpoint-return-values"></a>

### Ref<a name="aws-resource-events-endpoint-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns Endpoint ID, such as `mystack-Endpoint-ABCDEFGHIJK`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-events-endpoint-return-values-fn--getatt"></a>

#### <a name="aws-resource-events-endpoint-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the endpoint\.

`EndpointId`  <a name="EndpointId-fn::getatt"></a>
The ID of the endpoint\.

`EndpointUrl`  <a name="EndpointUrl-fn::getatt"></a>
The URL of the endpoint\.

`State`  <a name="State-fn::getatt"></a>
The current state of the endpoint\.

`StateReason`  <a name="StateReason-fn::getatt"></a>
The reason the endpoint is in its current state\.

## Examples<a name="aws-resource-events-endpoint--examples"></a>



### Create a global endpoint with event replication<a name="aws-resource-events-endpoint--examples--Create_a_global_endpoint_with_event_replication"></a>

The following example creates a global endpoint with event replication enabled\.

#### JSON<a name="aws-resource-events-endpoint--examples--Create_a_global_endpoint_with_event_replication--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Description": "This template will create an Endpoint resource",
  "Resources": {
    "SampleEndpoint": {
      "Type": "AWS::Events::Endpoint",
      "Properties": {
        "Name": "CreateExampleEndpoint",
        "RoutingConfig": {
          "FailoverConfig": {
            "Primary": {
              "HealthCheck": {
                  "arn:aws:route53:::healthcheck/0123456789abc"
              }
            },
            "Secondary": {
              "Route": {
                  "us-east-1"
              }
            }
          }
        },
        "ReplicationConfig": {
          "State": "ENABLED"
        },
        "RoleArn": {
          "arn:aws:iam::123456789012:role/EndpointReplicationRole"
        },
        "EventBuses": [
          {
            "EventBusArn": {
              "arn:aws:events:us-west-2:123456789012:event-bus/ExampleEventBus"
            }
          },
          {
            "EventBusArn": {
              "arn:aws:events:us-east-1:123456789012:event-bus/ExampleEventBus"
            }
          }
        ]
      }
    }
  },
  "Outputs": {
    "SampleEndpointName": {
      "Value": {
        "Ref": "SampleEndpoint"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-events-endpoint--examples--Create_a_global_endpoint_with_event_replication--yaml"></a>

```
  AWSTemplateFormatVersion: "2010-09-09"
  Description: "This template will create an Endpoint resource"
  Resources:
    SampleEndpoint:
      Type: AWS::Events::Endpoint
      Properties:
        Name: CreateExampleEndpoint
        RoutingConfig:
          FailoverConfig:
            Primary:
              HealthCheck: "arn:aws:route53:::healthcheck/0123456789abc"
            Secondary:
              Route: "us-east-1"
        ReplicationConfig:
          State: "ENABLED"
        RoleArn: "arn:aws:iam::123456789012:role/EndpointReplicationRole"
        EventBuses:
          - EventBusArn: "arn:aws:events:us-west-2:123456789012:event-bus/ExampleEventBus"
          - EventBusArn: "arn:aws:events:us-east-1:123456789012:event-bus/ExampleEventBus"
   
  Outputs:
    SampleEndpointName:
      Value: !Ref SampleEndpoint
```

### Create a global endpoint without event replication<a name="aws-resource-events-endpoint--examples--Create_a_global_endpoint_without_event_replication"></a>

The following example creates a global endpoint with event replication disabled\.

#### JSON<a name="aws-resource-events-endpoint--examples--Create_a_global_endpoint_without_event_replication--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Description": "This template will create an Endpoint resource",
  "Resources": {
    "SampleEndpoint": {
      "Type": "AWS::Events::Endpoint",
      "Properties": {
        "Name": "CreateExampleEndpoint",
        "RoutingConfig": {
          "FailoverConfig": {
            "Primary": {
              "HealthCheck": {
                  "arn:aws:route53:::healthcheck/0123456789abc"
              }
            },
            "Secondary": {
              "Route": {
                  "us-east-1"
              }
            }
          }
        },
        "ReplicationConfig": {
          "State": "DISABLED"
        },
        "EventBuses": [
          {
            "EventBusArn": {
              "arn:aws:events:us-west-2:123456789012:event-bus/ExampleEventBus"
            }
          },
          {
            "EventBusArn": {
              "arn:aws:events:us-east-1:123456789012:event-bus/ExampleEventBus"
            }
          }
        ]
      }
    }
  },
  "Outputs": {
    "SampleEndpointName": {
      "Value": {
        "Ref": "SampleEndpoint"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-events-endpoint--examples--Create_a_global_endpoint_without_event_replication--yaml"></a>

```
  AWSTemplateFormatVersion: "2010-09-09"
  Description: "This template will create an Endpoint resource"
  Resources:
    SampleEndpoint:
      Type: AWS::Events::Endpoint
      Properties:
        Name: CreateExampleEndpoint
        RoutingConfig:
          FailoverConfig:
            Primary:
              HealthCheck: "arn:aws:route53:::healthcheck/0123456789abc"
            Secondary:
              Route: "us-east-1"
        ReplicationConfig:
          State: "DISABLED"
        EventBuses:
          - EventBusArn: "arn:aws:events:us-west-2:123456789012:event-bus/ExampleEventBus"
          - EventBusArn: "arn:aws:events:us-east-1:123456789012:event-bus/ExampleEventBus"
   
  Outputs:
    SampleEndpointName:
      Value: !Ref SampleEndpoint
```