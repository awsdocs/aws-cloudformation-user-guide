# AWS::GlobalAccelerator::EndpointGroup PortOverride<a name="aws-properties-globalaccelerator-endpointgroup-portoverride"></a>

Override specific listener ports used to route traffic to endpoints that are part of an endpoint group\. For example, you can create a port override in which the listener receives user traffic on ports 80 and 443, but your accelerator routes that traffic to ports 1080 and 1443, respectively, on the endpoints\.

For more information, see [ Port overrides](https://docs.aws.amazon.com/global-accelerator/latest/dg/about-endpoint-groups-port-override.html) in the *AWS Global Accelerator Developer Guide*\.

## Syntax<a name="aws-properties-globalaccelerator-endpointgroup-portoverride-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-globalaccelerator-endpointgroup-portoverride-syntax.json"></a>

```
{
  "[EndpointPort](#cfn-globalaccelerator-endpointgroup-portoverride-endpointport)" : Integer,
  "[ListenerPort](#cfn-globalaccelerator-endpointgroup-portoverride-listenerport)" : Integer
}
```

### YAML<a name="aws-properties-globalaccelerator-endpointgroup-portoverride-syntax.yaml"></a>

```
  [EndpointPort](#cfn-globalaccelerator-endpointgroup-portoverride-endpointport): Integer
  [ListenerPort](#cfn-globalaccelerator-endpointgroup-portoverride-listenerport): Integer
```

## Properties<a name="aws-properties-globalaccelerator-endpointgroup-portoverride-properties"></a>

`EndpointPort`  <a name="cfn-globalaccelerator-endpointgroup-portoverride-endpointport"></a>
The endpoint port that you want a listener port to be mapped to\. This is the port on the endpoint, such as the Application Load Balancer or Amazon EC2 instance\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ListenerPort`  <a name="cfn-globalaccelerator-endpointgroup-portoverride-listenerport"></a>
The listener port that you want to map to a specific endpoint port\. This is the port that user traffic arrives to the Global Accelerator on\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)