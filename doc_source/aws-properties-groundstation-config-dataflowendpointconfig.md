# AWS::GroundStation::Config DataflowEndpointConfig<a name="aws-properties-groundstation-config-dataflowendpointconfig"></a>

 Provides information to AWS Ground Station about which IP endpoints to use during a contact\. 

## Syntax<a name="aws-properties-groundstation-config-dataflowendpointconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-groundstation-config-dataflowendpointconfig-syntax.json"></a>

```
{
  "[DataflowEndpointName](#cfn-groundstation-config-dataflowendpointconfig-dataflowendpointname)" : String,
  "[DataflowEndpointRegion](#cfn-groundstation-config-dataflowendpointconfig-dataflowendpointregion)" : String
}
```

### YAML<a name="aws-properties-groundstation-config-dataflowendpointconfig-syntax.yaml"></a>

```
  [DataflowEndpointName](#cfn-groundstation-config-dataflowendpointconfig-dataflowendpointname): String
  [DataflowEndpointRegion](#cfn-groundstation-config-dataflowendpointconfig-dataflowendpointregion): String
```

## Properties<a name="aws-properties-groundstation-config-dataflowendpointconfig-properties"></a>

`DataflowEndpointName`  <a name="cfn-groundstation-config-dataflowendpointconfig-dataflowendpointname"></a>
 The name of the dataflow endpoint to use during contacts\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataflowEndpointRegion`  <a name="cfn-groundstation-config-dataflowendpointconfig-dataflowendpointregion"></a>
 The region of the dataflow endpoint to use during contacts\. When omitted, Ground Station will use the region of the contact\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-groundstation-config-dataflowendpointconfig--examples"></a>

### Create a DataflowEndpointConfig<a name="aws-properties-groundstation-config-dataflowendpointconfig--examples--Create_a_DataflowEndpointConfig"></a>

The following example creates a Ground Station `DataflowEndpointConfig`

#### JSON<a name="aws-properties-groundstation-config-dataflowendpointconfig--examples--Create_a_DataflowEndpointConfig--json"></a>

```
{
  "DataflowEndpointConfig": {
    "DataflowEndpointName": "Downlink Demod Decode",
    "DataflowEndpointRegion": "us-east-2"
  }
}
```

#### YAML<a name="aws-properties-groundstation-config-dataflowendpointconfig--examples--Create_a_DataflowEndpointConfig--yaml"></a>

```
DataflowEndpointConfig:
  DataflowEndpointName: "Downlink Demod Decode"
  DataflowEndpointRegion: "us-east-2"
```