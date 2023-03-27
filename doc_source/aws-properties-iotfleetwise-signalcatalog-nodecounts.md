# AWS::IoTFleetWise::SignalCatalog NodeCounts<a name="aws-properties-iotfleetwise-signalcatalog-nodecounts"></a>

Information about the number of nodes and node types in a vehicle network\.

## Syntax<a name="aws-properties-iotfleetwise-signalcatalog-nodecounts-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotfleetwise-signalcatalog-nodecounts-syntax.json"></a>

```
{
  "[TotalActuators](#cfn-iotfleetwise-signalcatalog-nodecounts-totalactuators)" : Double,
  "[TotalAttributes](#cfn-iotfleetwise-signalcatalog-nodecounts-totalattributes)" : Double,
  "[TotalBranches](#cfn-iotfleetwise-signalcatalog-nodecounts-totalbranches)" : Double,
  "[TotalNodes](#cfn-iotfleetwise-signalcatalog-nodecounts-totalnodes)" : Double,
  "[TotalSensors](#cfn-iotfleetwise-signalcatalog-nodecounts-totalsensors)" : Double
}
```

### YAML<a name="aws-properties-iotfleetwise-signalcatalog-nodecounts-syntax.yaml"></a>

```
  [TotalActuators](#cfn-iotfleetwise-signalcatalog-nodecounts-totalactuators): Double
  [TotalAttributes](#cfn-iotfleetwise-signalcatalog-nodecounts-totalattributes): Double
  [TotalBranches](#cfn-iotfleetwise-signalcatalog-nodecounts-totalbranches): Double
  [TotalNodes](#cfn-iotfleetwise-signalcatalog-nodecounts-totalnodes): Double
  [TotalSensors](#cfn-iotfleetwise-signalcatalog-nodecounts-totalsensors): Double
```

## Properties<a name="aws-properties-iotfleetwise-signalcatalog-nodecounts-properties"></a>

`TotalActuators`  <a name="cfn-iotfleetwise-signalcatalog-nodecounts-totalactuators"></a>
The total number of nodes in a vehicle network that represent actuators\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TotalAttributes`  <a name="cfn-iotfleetwise-signalcatalog-nodecounts-totalattributes"></a>
The total number of nodes in a vehicle network that represent attributes\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TotalBranches`  <a name="cfn-iotfleetwise-signalcatalog-nodecounts-totalbranches"></a>
The total number of nodes in a vehicle network that represent branches\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TotalNodes`  <a name="cfn-iotfleetwise-signalcatalog-nodecounts-totalnodes"></a>
The total number of nodes in a vehicle network\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TotalSensors`  <a name="cfn-iotfleetwise-signalcatalog-nodecounts-totalsensors"></a>
The total number of nodes in a vehicle network that represent sensors\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)