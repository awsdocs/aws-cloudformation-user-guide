# AWS::GlobalAccelerator::EndpointGroup EndpointConfiguration<a name="aws-properties-globalaccelerator-endpointgroup-endpointconfiguration"></a>

A complex type for endpoints\. A resource must be valid and active when you add it as an endpoint\.

## Syntax<a name="aws-properties-globalaccelerator-endpointgroup-endpointconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-globalaccelerator-endpointgroup-endpointconfiguration-syntax.json"></a>

```
{
  "[ClientIPPreservationEnabled](#cfn-globalaccelerator-endpointgroup-endpointconfiguration-clientippreservationenabled)" : Boolean,
  "[EndpointId](#cfn-globalaccelerator-endpointgroup-endpointconfiguration-endpointid)" : String,
  "[Weight](#cfn-globalaccelerator-endpointgroup-endpointconfiguration-weight)" : Integer
}
```

### YAML<a name="aws-properties-globalaccelerator-endpointgroup-endpointconfiguration-syntax.yaml"></a>

```
  [ClientIPPreservationEnabled](#cfn-globalaccelerator-endpointgroup-endpointconfiguration-clientippreservationenabled): Boolean
  [EndpointId](#cfn-globalaccelerator-endpointgroup-endpointconfiguration-endpointid): String
  [Weight](#cfn-globalaccelerator-endpointgroup-endpointconfiguration-weight): Integer
```

## Properties<a name="aws-properties-globalaccelerator-endpointgroup-endpointconfiguration-properties"></a>

`ClientIPPreservationEnabled`  <a name="cfn-globalaccelerator-endpointgroup-endpointconfiguration-clientippreservationenabled"></a>
Indicates whether client IP address preservation is enabled for an Application Load Balancer endpoint\. The value is true or false\. The default value is true for new accelerators\.   
If the value is set to true, the client's IP address is preserved in the `X-Forwarded-For` request header as traffic travels to applications on the Application Load Balancer endpoint fronted by the accelerator\.  
For more information, see [ Preserve Client IP Addresses in AWS Global Accelerator](https://docs.aws.amazon.com/global-accelerator/latest/dg/preserve-client-ip-address.html) in the *AWS Global Accelerator Developer Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndpointId`  <a name="cfn-globalaccelerator-endpointgroup-endpointconfiguration-endpointid"></a>
An ID for the endpoint\. If the endpoint is a Network Load Balancer or Application Load Balancer, this is the Amazon Resource Name \(ARN\) of the resource\. If the endpoint is an Elastic IP address, this is the Elastic IP address allocation ID\. For Amazon EC2 instances, this is the EC2 instance ID\. A resource must be valid and active when you add it as an endpoint\.  
An Application Load Balancer can be either internal or internet\-facing\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Weight`  <a name="cfn-globalaccelerator-endpointgroup-endpointconfiguration-weight"></a>
The weight associated with the endpoint\. When you add weights to endpoints, you configure AWS Global Accelerator to route traffic based on proportions that you specify\. For example, you might specify endpoint weights of 4, 5, 5, and 6 \(sum=20\)\. The result is that 4/20 of your traffic, on average, is routed to the first endpoint, 5/20 is routed both to the second and third endpoints, and 6/20 is routed to the last endpoint\. For more information, see [Endpoint Weights](https://docs.aws.amazon.com/global-accelerator/latest/dg/about-endpoints-endpoint-weights.html) in the *AWS Global Accelerator Developer Guide*\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)