# AWS::Glue::Partition SerdeInfo<a name="aws-properties-glue-partition-serdeinfo"></a>

Information about a serialization/deserialization program \(SerDe\) that serves as an extractor and loader\.

## Syntax<a name="aws-properties-glue-partition-serdeinfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-partition-serdeinfo-syntax.json"></a>

```
{
  "[Name](#cfn-glue-partition-serdeinfo-name)" : String,
  "[Parameters](#cfn-glue-partition-serdeinfo-parameters)" : Json,
  "[SerializationLibrary](#cfn-glue-partition-serdeinfo-serializationlibrary)" : String
}
```

### YAML<a name="aws-properties-glue-partition-serdeinfo-syntax.yaml"></a>

```
  [Name](#cfn-glue-partition-serdeinfo-name): String
  [Parameters](#cfn-glue-partition-serdeinfo-parameters): Json
  [SerializationLibrary](#cfn-glue-partition-serdeinfo-serializationlibrary): String
```

## Properties<a name="aws-properties-glue-partition-serdeinfo-properties"></a>

`Name`  <a name="cfn-glue-partition-serdeinfo-name"></a>
Name of the SerDe\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-glue-partition-serdeinfo-parameters"></a>
These key\-value pairs define initialization parameters for the SerDe\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SerializationLibrary`  <a name="cfn-glue-partition-serdeinfo-serializationlibrary"></a>
Usually the class that implements the SerDe\. An example is `org.apache.hadoop.hive.serde2.columnar.ColumnarSerDe`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)