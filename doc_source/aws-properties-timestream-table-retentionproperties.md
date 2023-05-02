# AWS::Timestream::Table RetentionProperties<a name="aws-properties-timestream-table-retentionproperties"></a>

Retention properties contain the duration for which your time\-series data must be stored in the magnetic store and the memory store\. 

## Syntax<a name="aws-properties-timestream-table-retentionproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-timestream-table-retentionproperties-syntax.json"></a>

```
{
  "[MagneticStoreRetentionPeriodInDays](#cfn-timestream-table-retentionproperties-magneticstoreretentionperiodindays)" : String,
  "[MemoryStoreRetentionPeriodInHours](#cfn-timestream-table-retentionproperties-memorystoreretentionperiodinhours)" : String
}
```

### YAML<a name="aws-properties-timestream-table-retentionproperties-syntax.yaml"></a>

```
  [MagneticStoreRetentionPeriodInDays](#cfn-timestream-table-retentionproperties-magneticstoreretentionperiodindays): String
  [MemoryStoreRetentionPeriodInHours](#cfn-timestream-table-retentionproperties-memorystoreretentionperiodinhours): String
```

## Properties<a name="aws-properties-timestream-table-retentionproperties-properties"></a>

`MagneticStoreRetentionPeriodInDays`  <a name="cfn-timestream-table-retentionproperties-magneticstoreretentionperiodindays"></a>
The duration for which data must be stored in the magnetic store\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MemoryStoreRetentionPeriodInHours`  <a name="cfn-timestream-table-retentionproperties-memorystoreretentionperiodinhours"></a>
The duration for which data must be stored in the memory store\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)