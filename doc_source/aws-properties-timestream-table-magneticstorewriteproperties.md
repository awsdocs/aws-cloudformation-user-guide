# AWS::Timestream::Table MagneticStoreWriteProperties<a name="aws-properties-timestream-table-magneticstorewriteproperties"></a>

The set of properties on a table for configuring magnetic store writes\.

## Syntax<a name="aws-properties-timestream-table-magneticstorewriteproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-timestream-table-magneticstorewriteproperties-syntax.json"></a>

```
{
  "[EnableMagneticStoreWrites](#cfn-timestream-table-magneticstorewriteproperties-enablemagneticstorewrites)" : Boolean,
  "[MagneticStoreRejectedDataLocation](#cfn-timestream-table-magneticstorewriteproperties-magneticstorerejecteddatalocation)" : MagneticStoreRejectedDataLocation
}
```

### YAML<a name="aws-properties-timestream-table-magneticstorewriteproperties-syntax.yaml"></a>

```
  [EnableMagneticStoreWrites](#cfn-timestream-table-magneticstorewriteproperties-enablemagneticstorewrites): Boolean
  [MagneticStoreRejectedDataLocation](#cfn-timestream-table-magneticstorewriteproperties-magneticstorerejecteddatalocation): 
    MagneticStoreRejectedDataLocation
```

## Properties<a name="aws-properties-timestream-table-magneticstorewriteproperties-properties"></a>

`EnableMagneticStoreWrites`  <a name="cfn-timestream-table-magneticstorewriteproperties-enablemagneticstorewrites"></a>
A flag to enable magnetic store writes\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MagneticStoreRejectedDataLocation`  <a name="cfn-timestream-table-magneticstorewriteproperties-magneticstorerejecteddatalocation"></a>
The location to write error reports for records rejected asynchronously during magnetic store writes\.  
*Required*: No  
*Type*: [MagneticStoreRejectedDataLocation](aws-properties-timestream-table-magneticstorerejecteddatalocation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)