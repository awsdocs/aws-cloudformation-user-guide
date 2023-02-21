# AWS::FSx::Volume OriginSnapshot<a name="aws-properties-fsx-volume-openzfsconfiguration-originsnapshot"></a>

The configuration object that specifies the snapshot to use as the origin of the data for the volume\.

## Syntax<a name="aws-properties-fsx-volume-openzfsconfiguration-originsnapshot-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fsx-volume-openzfsconfiguration-originsnapshot-syntax.json"></a>

```
{
  "[CopyStrategy](#cfn-fsx-volume-openzfsconfiguration-originsnapshot-copystrategy)" : String,
  "[SnapshotARN](#cfn-fsx-volume-openzfsconfiguration-originsnapshot-snapshotarn)" : String
}
```

### YAML<a name="aws-properties-fsx-volume-openzfsconfiguration-originsnapshot-syntax.yaml"></a>

```
  [CopyStrategy](#cfn-fsx-volume-openzfsconfiguration-originsnapshot-copystrategy): String
  [SnapshotARN](#cfn-fsx-volume-openzfsconfiguration-originsnapshot-snapshotarn): String
```

## Properties<a name="aws-properties-fsx-volume-openzfsconfiguration-originsnapshot-properties"></a>

`CopyStrategy`  <a name="cfn-fsx-volume-openzfsconfiguration-originsnapshot-copystrategy"></a>
The strategy used when copying data from the snapshot to the new volume\.   
+  `CLONE` \- The new volume references the data in the origin snapshot\. Cloning a snapshot is faster than copying data from the snapshot to a new volume and doesn't consume disk throughput\. However, the origin snapshot can't be deleted if there is a volume using its copied data\. 
+  `FULL_COPY` \- Copies all data from the snapshot to the new volume\. 
*Required*: Yes  
*Type*: String  
*Allowed values*: `CLONE | FULL_COPY`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SnapshotARN`  <a name="cfn-fsx-volume-openzfsconfiguration-originsnapshot-snapshotarn"></a>
Specifies the snapshot to use when creating an OpenZFS volume from a snapshot\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)