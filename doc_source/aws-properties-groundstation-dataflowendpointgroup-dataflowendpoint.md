# AWS::GroundStation::DataflowEndpointGroup DataflowEndpoint<a name="aws-properties-groundstation-dataflowendpointgroup-dataflowendpoint"></a>

 Contains information such as socket address and name that defines an endpoint\. 

## Syntax<a name="aws-properties-groundstation-dataflowendpointgroup-dataflowendpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-groundstation-dataflowendpointgroup-dataflowendpoint-syntax.json"></a>

```
{
  "[Address](#cfn-groundstation-dataflowendpointgroup-dataflowendpoint-address)" : SocketAddress,
  "[Mtu](#cfn-groundstation-dataflowendpointgroup-dataflowendpoint-mtu)" : Integer,
  "[Name](#cfn-groundstation-dataflowendpointgroup-dataflowendpoint-name)" : String
}
```

### YAML<a name="aws-properties-groundstation-dataflowendpointgroup-dataflowendpoint-syntax.yaml"></a>

```
  [Address](#cfn-groundstation-dataflowendpointgroup-dataflowendpoint-address): 
    SocketAddress
  [Mtu](#cfn-groundstation-dataflowendpointgroup-dataflowendpoint-mtu): Integer
  [Name](#cfn-groundstation-dataflowendpointgroup-dataflowendpoint-name): String
```

## Properties<a name="aws-properties-groundstation-dataflowendpointgroup-dataflowendpoint-properties"></a>

`Address`  <a name="cfn-groundstation-dataflowendpointgroup-dataflowendpoint-address"></a>
 The address and port of an endpoint\.   
*Required*: No  
*Type*: [SocketAddress](aws-properties-groundstation-dataflowendpointgroup-socketaddress.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Mtu`  <a name="cfn-groundstation-dataflowendpointgroup-dataflowendpoint-mtu"></a>
Maximum transmission unit \(MTU\) size in bytes of a dataflow endpoint\. Valid values are between 1400 and 1500\. A default value of 1500 is used if not set\.   
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-groundstation-dataflowendpointgroup-dataflowendpoint-name"></a>
 The endpoint name\.   
 When listing available contacts for a satellite, Ground Station searches for a dataflow endpoint whose name matches the value specified by the dataflow endpoint config of the selected mission profile\. If no matching dataflow endpoints are found then Ground Station will not display any available contacts for the satellite\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-groundstation-dataflowendpointgroup-dataflowendpoint--examples"></a>

### Create a DataflowEndpoint<a name="aws-properties-groundstation-dataflowendpointgroup-dataflowendpoint--examples--Create_a_DataflowEndpoint"></a>

The following example creates a Ground Station `DataflowEndpoint`

#### JSON<a name="aws-properties-groundstation-dataflowendpointgroup-dataflowendpoint--examples--Create_a_DataflowEndpoint--json"></a>

```
{
  "Endpoint": {
    "Name": "myEndpoint",
    "Address": {
      "Name": "172.10.0.2",
      "Port": 44720
    },
    "Mtu": 1500
}
```

#### YAML<a name="aws-properties-groundstation-dataflowendpointgroup-dataflowendpoint--examples--Create_a_DataflowEndpoint--yaml"></a>

```
Endpoint:
  Name: myEndpoint
  Address:
    Name: 172.10.0.2
    Port: 44720
  Mtu: 1500
```