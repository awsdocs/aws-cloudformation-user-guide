# AWS::IoTTwinMaker::ComponentType PropertyDefinition<a name="aws-properties-iottwinmaker-componenttype-propertydefinition"></a>

PropertyDefinition is an object that maps strings to the property definitions in the component type\.

## Syntax<a name="aws-properties-iottwinmaker-componenttype-propertydefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iottwinmaker-componenttype-propertydefinition-syntax.json"></a>

```
{
  "[Configurations](#cfn-iottwinmaker-componenttype-propertydefinition-configurations)" : {Key : Value, ...},
  "[DataType](#cfn-iottwinmaker-componenttype-propertydefinition-datatype)" : DataType,
  "[DefaultValue](#cfn-iottwinmaker-componenttype-propertydefinition-defaultvalue)" : DataValue,
  "[IsExternalId](#cfn-iottwinmaker-componenttype-propertydefinition-isexternalid)" : Boolean,
  "[IsRequiredInEntity](#cfn-iottwinmaker-componenttype-propertydefinition-isrequiredinentity)" : Boolean,
  "[IsStoredExternally](#cfn-iottwinmaker-componenttype-propertydefinition-isstoredexternally)" : Boolean,
  "[IsTimeSeries](#cfn-iottwinmaker-componenttype-propertydefinition-istimeseries)" : Boolean
}
```

### YAML<a name="aws-properties-iottwinmaker-componenttype-propertydefinition-syntax.yaml"></a>

```
  [Configurations](#cfn-iottwinmaker-componenttype-propertydefinition-configurations): 
    Key : Value
  [DataType](#cfn-iottwinmaker-componenttype-propertydefinition-datatype): 
    DataType
  [DefaultValue](#cfn-iottwinmaker-componenttype-propertydefinition-defaultvalue): 
    DataValue
  [IsExternalId](#cfn-iottwinmaker-componenttype-propertydefinition-isexternalid): Boolean
  [IsRequiredInEntity](#cfn-iottwinmaker-componenttype-propertydefinition-isrequiredinentity): Boolean
  [IsStoredExternally](#cfn-iottwinmaker-componenttype-propertydefinition-isstoredexternally): Boolean
  [IsTimeSeries](#cfn-iottwinmaker-componenttype-propertydefinition-istimeseries): Boolean
```

## Properties<a name="aws-properties-iottwinmaker-componenttype-propertydefinition-properties"></a>

`Configurations`  <a name="cfn-iottwinmaker-componenttype-propertydefinition-configurations"></a>
A mapping that specifies configuration information about the property\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataType`  <a name="cfn-iottwinmaker-componenttype-propertydefinition-datatype"></a>
  
*Required*: No  
*Type*: [DataType](aws-properties-iottwinmaker-componenttype-datatype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultValue`  <a name="cfn-iottwinmaker-componenttype-propertydefinition-defaultvalue"></a>
A boolean value that specifies whether the property ID comes from an external data store\.  
*Required*: No  
*Type*: [DataValue](aws-properties-iottwinmaker-componenttype-datavalue.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsExternalId`  <a name="cfn-iottwinmaker-componenttype-propertydefinition-isexternalid"></a>
A boolean value that specifies whether the property ID comes from an external data store\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsRequiredInEntity`  <a name="cfn-iottwinmaker-componenttype-propertydefinition-isrequiredinentity"></a>
A boolean value that specifies whether the property is required in an entity\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsStoredExternally`  <a name="cfn-iottwinmaker-componenttype-propertydefinition-isstoredexternally"></a>
A boolean value that specifies whether the property is stored externally\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsTimeSeries`  <a name="cfn-iottwinmaker-componenttype-propertydefinition-istimeseries"></a>
A boolean value that specifies whether the property consists of time series data\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)