# AWS::GlobalAccelerator::EndpointGroup<a name="aws-resource-globalaccelerator-endpointgroup"></a>

The `AWS::GlobalAccelerator::EndpointGroup` resource is a Global Accelerator resource type that contains information about how you create an endpoint group for the specified listener\. An endpoint group is a collection of endpoints in one AWS Region\.

## Syntax<a name="aws-resource-globalaccelerator-endpointgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-globalaccelerator-endpointgroup-syntax.json"></a>

```
{
  "Type" : "AWS::GlobalAccelerator::EndpointGroup",
  "Properties" : {
      "[EndpointConfigurations](#cfn-globalaccelerator-endpointgroup-endpointconfigurations)" : [ EndpointConfiguration, ... ],
      "[EndpointGroupRegion](#cfn-globalaccelerator-endpointgroup-endpointgroupregion)" : String,
      "[HealthCheckIntervalSeconds](#cfn-globalaccelerator-endpointgroup-healthcheckintervalseconds)" : Integer,
      "[HealthCheckPath](#cfn-globalaccelerator-endpointgroup-healthcheckpath)" : String,
      "[HealthCheckPort](#cfn-globalaccelerator-endpointgroup-healthcheckport)" : Integer,
      "[HealthCheckProtocol](#cfn-globalaccelerator-endpointgroup-healthcheckprotocol)" : String,
      "[ListenerArn](#cfn-globalaccelerator-endpointgroup-listenerarn)" : String,
      "[PortOverrides](#cfn-globalaccelerator-endpointgroup-portoverrides)" : [ PortOverride, ... ],
      "[ThresholdCount](#cfn-globalaccelerator-endpointgroup-thresholdcount)" : Integer,
      "[TrafficDialPercentage](#cfn-globalaccelerator-endpointgroup-trafficdialpercentage)" : Double
    }
}
```

### YAML<a name="aws-resource-globalaccelerator-endpointgroup-syntax.yaml"></a>

```
Type: AWS::GlobalAccelerator::EndpointGroup
Properties: 
  [EndpointConfigurations](#cfn-globalaccelerator-endpointgroup-endpointconfigurations): 
    - EndpointConfiguration
  [EndpointGroupRegion](#cfn-globalaccelerator-endpointgroup-endpointgroupregion): String
  [HealthCheckIntervalSeconds](#cfn-globalaccelerator-endpointgroup-healthcheckintervalseconds): Integer
  [HealthCheckPath](#cfn-globalaccelerator-endpointgroup-healthcheckpath): String
  [HealthCheckPort](#cfn-globalaccelerator-endpointgroup-healthcheckport): Integer
  [HealthCheckProtocol](#cfn-globalaccelerator-endpointgroup-healthcheckprotocol): String
  [ListenerArn](#cfn-globalaccelerator-endpointgroup-listenerarn): String
  [PortOverrides](#cfn-globalaccelerator-endpointgroup-portoverrides): 
    - PortOverride
  [ThresholdCount](#cfn-globalaccelerator-endpointgroup-thresholdcount): Integer
  [TrafficDialPercentage](#cfn-globalaccelerator-endpointgroup-trafficdialpercentage): Double
```

## Properties<a name="aws-resource-globalaccelerator-endpointgroup-properties"></a>

`EndpointConfigurations`  <a name="cfn-globalaccelerator-endpointgroup-endpointconfigurations"></a>
The list of endpoint objects\.  
*Required*: No  
*Type*: List of [EndpointConfiguration](aws-properties-globalaccelerator-endpointgroup-endpointconfiguration.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndpointGroupRegion`  <a name="cfn-globalaccelerator-endpointgroup-endpointgroupregion"></a>
The AWS Region where the endpoint group is located\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `255`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`HealthCheckIntervalSeconds`  <a name="cfn-globalaccelerator-endpointgroup-healthcheckintervalseconds"></a>
The time—10 seconds or 30 seconds—between health checks for each endpoint\. The default value is 30\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `10`  
*Maximum*: `30`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HealthCheckPath`  <a name="cfn-globalaccelerator-endpointgroup-healthcheckpath"></a>
If the protocol is HTTP/S, then this value provides the ping path that Global Accelerator uses for the destination on the endpoints for health checks\. The default is slash \(/\)\.  
*Required*: No  
*Type*: String  
*Maximum*: `255`  
*Pattern*: `^/[-a-zA-Z0-9@:%_\\+.~#?&/=]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HealthCheckPort`  <a name="cfn-globalaccelerator-endpointgroup-healthcheckport"></a>
The port that Global Accelerator uses to perform health checks on endpoints that are part of this endpoint group\.   
The default port is the port for the listener that this endpoint group is associated with\. If the listener port is a list, Global Accelerator uses the first specified port in the list of ports\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HealthCheckProtocol`  <a name="cfn-globalaccelerator-endpointgroup-healthcheckprotocol"></a>
The protocol that Global Accelerator uses to perform health checks on endpoints that are part of this endpoint group\. The default value is TCP\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HTTP | HTTPS | TCP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ListenerArn`  <a name="cfn-globalaccelerator-endpointgroup-listenerarn"></a>
The Amazon Resource Name \(ARN\) of the listener\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `255`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PortOverrides`  <a name="cfn-globalaccelerator-endpointgroup-portoverrides"></a>
Allows you to override the destination ports used to route traffic to an endpoint\. Using a port override lets you to map a list of external destination ports \(that your users send traffic to\) to a list of internal destination ports that you want an application endpoint to receive traffic on\.   
*Required*: No  
*Type*: List of [PortOverride](aws-properties-globalaccelerator-endpointgroup-portoverride.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThresholdCount`  <a name="cfn-globalaccelerator-endpointgroup-thresholdcount"></a>
The number of consecutive health checks required to set the state of a healthy endpoint to unhealthy, or to set an unhealthy endpoint to healthy\. The default value is 3\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrafficDialPercentage`  <a name="cfn-globalaccelerator-endpointgroup-trafficdialpercentage"></a>
The percentage of traffic to send to an AWS Region\. Additional traffic is distributed to other endpoint groups for this listener\.   
Use this action to increase \(dial up\) or decrease \(dial down\) traffic to a specific Region\. The percentage is applied to the traffic that would otherwise have been routed to the Region based on optimal routing\.  
The default value is 100\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-globalaccelerator-endpointgroup-return-values"></a>

### Ref<a name="aws-resource-globalaccelerator-endpointgroup-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the endpoint group, such as `arn:aws:globalaccelerator::012345678901:accelerator/1234abcd-abcd-1234-abcd-1234abcdefgh/listener/0123vxyz/endpoint-group/098765zyxwvu`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-globalaccelerator-endpointgroup-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-globalaccelerator-endpointgroup-return-values-fn--getatt-fn--getatt"></a>

`EndpointGroupArn`  <a name="EndpointGroupArn-fn::getatt"></a>
The ARN of the endpoint group, such as `arn:aws:globalaccelerator::012345678901:accelerator/1234abcd-abcd-1234-abcd-1234abcdefgh/listener/0123vxyz/endpoint-group/098765zyxwvu`\.

## Examples<a name="aws-resource-globalaccelerator-endpointgroup--examples"></a>



### Add an endpoint group<a name="aws-resource-globalaccelerator-endpointgroup--examples--Add_an_endpoint_group"></a>

These are examples to specify an endpoint group\.

#### JSON<a name="aws-resource-globalaccelerator-endpointgroup--examples--Add_an_endpoint_group--json"></a>

```
"Resources": {
        "EndpointGroup": {
        "Type": "AWS::GlobalAccelerator::EndpointGroup",
        "Properties": {
            "ListenerArn": {
                "Ref": "Listener"
            },
            "EndpointGroupRegion": {
                "Ref": "EndpointRegion"
            },
            "TrafficDialPercentage": 100.0,
            "EndpointConfigurations": [
                {
                    "EndpointId": {
                        "Ref": "EndpointId"
                    }
                }
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-globalaccelerator-endpointgroup--examples--Add_an_endpoint_group--yaml"></a>

```
EndpointGroup:
  Type: AWS::GlobalAccelerator::EndpointGroup
  Properties:
    ListenerArn:
      Ref: Listener
    EndpointGroupRegion:
      Ref: EndpointRegion
    TrafficDialPercentage: 100
    EndpointConfigurations:
    - EndpointId:
        Ref: EndpointId
```