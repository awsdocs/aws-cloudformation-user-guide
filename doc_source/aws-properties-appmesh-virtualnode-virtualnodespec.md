# AWS::AppMesh::VirtualNode VirtualNodeSpec<a name="aws-properties-appmesh-virtualnode-virtualnodespec"></a>

An object representing the specification of a virtual node\.

## Syntax<a name="aws-properties-appmesh-virtualnode-virtualnodespec-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-virtualnodespec-syntax.json"></a>

```
{
  "[Backends](#cfn-appmesh-virtualnode-virtualnodespec-backends)" : [ [Backend](aws-properties-appmesh-virtualnode-backend.md), ... ],
  "[Listeners](#cfn-appmesh-virtualnode-virtualnodespec-listeners)" : [ [Listener](aws-properties-appmesh-virtualnode-listener.md), ... ],
  "[Logging](#cfn-appmesh-virtualnode-virtualnodespec-logging)" : [Logging](aws-properties-appmesh-virtualnode-logging.md),
  "[ServiceDiscovery](#cfn-appmesh-virtualnode-virtualnodespec-servicediscovery)" : [ServiceDiscovery](aws-properties-appmesh-virtualnode-servicediscovery.md)
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-virtualnodespec-syntax.yaml"></a>

```
  [Backends](#cfn-appmesh-virtualnode-virtualnodespec-backends):
    - [Backend](aws-properties-appmesh-virtualnode-backend.md)
  [Listeners](#cfn-appmesh-virtualnode-virtualnodespec-listeners):
    - [Listener](aws-properties-appmesh-virtualnode-listener.md)
  [Logging](#cfn-appmesh-virtualnode-virtualnodespec-logging):
    [Logging](aws-properties-appmesh-virtualnode-logging.md)
  [ServiceDiscovery](#cfn-appmesh-virtualnode-virtualnodespec-servicediscovery):
    [ServiceDiscovery](aws-properties-appmesh-virtualnode-servicediscovery.md)
```

## Properties<a name="aws-properties-appmesh-virtualnode-virtualnodespec-properties"></a>

`Backends`  <a name="cfn-appmesh-virtualnode-virtualnodespec-backends"></a>
The backends that the virtual node is expected to send outbound traffic to\.
*Required*: No
*Type*: List of [Backend](aws-properties-appmesh-virtualnode-backend.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Listeners`  <a name="cfn-appmesh-virtualnode-virtualnodespec-listeners"></a>
The listeners that the virtual node is expected to receive inbound traffic from\. Currently only one listener is supported per virtual node\.
*Required*: No
*Type*: List of [Listener](aws-properties-appmesh-virtualnode-listener.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Logging`  <a name="cfn-appmesh-virtualnode-virtualnodespec-logging"></a>
The inbound and outbound access logging information for the virtual node\.
*Required*: No
*Type*: [Logging](aws-properties-appmesh-virtualnode-logging.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceDiscovery`  <a name="cfn-appmesh-virtualnode-virtualnodespec-servicediscovery"></a>
The service discovery information for the virtual node\. If your virtual node does not expect ingress traffic, you can omit this parameter\.
*Required*: No
*Type*: [ServiceDiscovery](aws-properties-appmesh-virtualnode-servicediscovery.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
