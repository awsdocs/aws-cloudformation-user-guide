# AWS::GroundStation::DataflowEndpointGroup SocketAddress<a name="aws-properties-groundstation-dataflowendpointgroup-socketaddress"></a>

The address of the endpoint, such as `192.168.1.1`\. 

## Syntax<a name="aws-properties-groundstation-dataflowendpointgroup-socketaddress-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-groundstation-dataflowendpointgroup-socketaddress-syntax.json"></a>

```
{
  "[Name](#cfn-groundstation-dataflowendpointgroup-socketaddress-name)" : String,
  "[Port](#cfn-groundstation-dataflowendpointgroup-socketaddress-port)" : Integer
}
```

### YAML<a name="aws-properties-groundstation-dataflowendpointgroup-socketaddress-syntax.yaml"></a>

```
  [Name](#cfn-groundstation-dataflowendpointgroup-socketaddress-name): String
  [Port](#cfn-groundstation-dataflowendpointgroup-socketaddress-port): Integer
```

## Properties<a name="aws-properties-groundstation-dataflowendpointgroup-socketaddress-properties"></a>

`Name`  <a name="cfn-groundstation-dataflowendpointgroup-socketaddress-name"></a>
The name of the endpoint, such as `Endpoint 1`\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-groundstation-dataflowendpointgroup-socketaddress-port"></a>
The port of the endpoint, such as `55888`\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-groundstation-dataflowendpointgroup-socketaddress--examples"></a>

### Create a SocketAddress<a name="aws-properties-groundstation-dataflowendpointgroup-socketaddress--examples--Create_a_SocketAddress"></a>

The following example creates a Ground Station `SocketAddress`

#### JSON<a name="aws-properties-groundstation-dataflowendpointgroup-socketaddress--examples--Create_a_SocketAddress--json"></a>

```
{
  "Address": {
    "Name": "172.10.0.2",
    "Port": 44720
  }
}
```

#### YAML<a name="aws-properties-groundstation-dataflowendpointgroup-socketaddress--examples--Create_a_SocketAddress--yaml"></a>

```
Address:
  Name: 172.10.0.2
  Port: 44720
```