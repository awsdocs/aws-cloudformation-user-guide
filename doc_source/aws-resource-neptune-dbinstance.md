# AWS::Neptune::DBInstance<a name="aws-resource-neptune-dbinstance"></a>

The `AWS::Neptune::DBInstance` type creates an Neptune DB instance\. 

**Important**  
If a DB instance is deleted or replaced during an update, AWS CloudFormation deletes all automated snapshots\. However, it retains manual DB snapshots\. During an update that requires replacement, you can apply a stack policy to prevent DB instances from being replaced\. For more information, see [Prevent Updates to Stack Resources](protect-stack-resources.md)\.

**Topics**
+ [Syntax](#aws-resource-neptune-dbinstance-syntax)
+ [Properties](#aws-resource-neptune-dbinstance-prop)
+ [Updating and Deleting AWS::Neptune::DBInstance Resources](#updating-and-deleting-dbinstance-resources)
+ [Return Values](#aws-resource-neptune-dbinstance-returnvalues)

## Syntax<a name="aws-resource-neptune-dbinstance-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-neptune-dbinstance-syntax.json"></a>

```
{
  "Type" : "AWS::Neptune::DBInstance",
  "Properties" :
  {
    "[AllowMajorVersionUpgrade](#cfn-neptune-dbinstance-allowmajorversionupgrade)" : Boolean,
    "[AutoMinorVersionUpgrade](#cfn-neptune-dbinstance-autominorversionupgrade)" : Boolean,
    "[AvailabilityZone](#cfn-neptune-dbinstance-availabilityzone)" : String,
    "[DBClusterIdentifier](#cfn-neptune-dbinstance-dbclusteridentifier)" : String,
    "[DBInstanceClass](#cfn-neptune-dbinstance-dbinstanceclass)" : String,
    "[DBInstanceIdentifier](#cfn-neptune-dbinstance-dbinstanceidentifier)" : String,
    "[DBParameterGroupName](#cfn-neptune-dbinstance-dbparametergroupname)" : String,
    "[DBSnapshotIdentifier](#cfn-neptune-dbinstance-dbsnapshotidentifier)" : String,
    "[DBSubnetGroupName](#cfn-neptune-dbinstance-dbsubnetgroupname)" : String,
    "[PreferredMaintenanceWindow](#cfn-neptune-dbinstance-preferredmaintenancewindow)" : String,
    "[Tags](#cfn-neptune-dbinstance-tags)" : [ Resource Tag, ... ]
  }
}
```

### YAML<a name="aws-resource-neptune-dbinstance-syntax.yaml"></a>

```
Type: "AWS::Neptune::DBInstance"
Properties:
  [AllowMajorVersionUpgrade](#cfn-neptune-dbinstance-allowmajorversionupgrade): Boolean
  [AutoMinorVersionUpgrade](#cfn-neptune-dbinstance-autominorversionupgrade): Boolean
  [AvailabilityZone](#cfn-neptune-dbinstance-availabilityzone): String
  [DBClusterIdentifier](#cfn-neptune-dbinstance-dbclusteridentifier): String
  [DBInstanceClass](#cfn-neptune-dbinstance-dbinstanceclass): String
  [DBInstanceIdentifier](#cfn-neptune-dbinstance-dbinstanceidentifier): String
  [DBParameterGroupName](#cfn-neptune-dbinstance-dbparametergroupname): String
  [DBSnapshotIdentifier](#cfn-neptune-dbinstance-dbsnapshotidentifier): String
  [DBSubnetGroupName](#cfn-neptune-dbinstance-dbsubnetgroupname): String
  [PreferredMaintenanceWindow](#cfn-neptune-dbinstance-preferredmaintenancewindow) : String
  [Tags](#cfn-neptune-dbinstance-tags):
    Resource Tag
```

## Properties<a name="aws-resource-neptune-dbinstance-prop"></a>

`AllowMajorVersionUpgrade`  <a name="cfn-neptune-dbinstance-allowmajorversionupgrade"></a>
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`AutoMinorVersionUpgrade`  <a name="cfn-neptune-dbinstance-autominorversionupgrade"></a>
Indicates that minor engine upgrades are applied automatically to the DB instance during the maintenance window\. The default value is `true`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) or [some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)\. 

`AvailabilityZone`  <a name="cfn-neptune-dbinstance-availabilityzone"></a>
The name of the Availability Zone where the DB instance is located\. You can't set the `AvailabilityZone` parameter if the `MultiAZ` parameter is set to `true`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`DBClusterIdentifier`  <a name="cfn-neptune-dbinstance-dbclusteridentifier"></a>
The name of an existing DB cluster that this instance is associated with\.   
Neptune assigns the first DB instance in the cluster as the primary, and additional DB instances as replicas\.  
If you specify this property, the default deletion policy is `Delete`\. Otherwise, the default deletion policy is `Snapshot`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`DBInstanceClass`  <a name="cfn-neptune-dbinstance-dbinstanceclass"></a>
The name of the compute and memory capacity classes of the DB instance\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`DBInstanceIdentifier`  <a name="cfn-neptune-dbinstance-dbinstanceidentifier"></a>
A name for the DB instance\. If you specify a name, AWS CloudFormation converts it to lowercase\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the DB instance\. For more information, see [Name Type](aws-properties-name.md)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`DBParameterGroupName`  <a name="cfn-neptune-dbinstance-dbparametergroupname"></a>
The name of an existing DB parameter group or a reference to an [AWS::Neptune::DBParameterGroup](aws-resource-neptune-dbparametergroup.md) resource created in the template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) or [some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)\. If any of the data members of the referenced parameter group are changed during an update, the DB instance might need to be restarted, which causes some interruption\. If the parameter group contains static parameters, whether they were changed or not, an update triggers a reboot\.

`DBSnapshotIdentifier`  <a name="cfn-neptune-dbinstance-dbsnapshotidentifier"></a>
The name or Amazon Resource Name \(ARN\) of the DB snapshot that's used to restore the DB instance\. If you're restoring from a shared manual DB snapshot, you must specify the ARN of the snapshot\.  
By specifying this property, you can create a DB instance from the specified DB snapshot\. If the `DBSnapshotIdentifier` property is an empty string or the `AWS::Neptune::DBInstance` declaration has no `DBSnapshotIdentifier` property, AWS CloudFormation creates a new database\. If the property contains a value \(other than an empty string\), AWS CloudFormation creates a database from the specified snapshot\. If a snapshot with the specified name doesn't exist, AWS CloudFormation can't create the database and it rolls back the stack\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`DBSubnetGroupName`  <a name="cfn-neptune-dbinstance-dbsubnetgroupname"></a>
A DB subnet group to associate with the DB instance\. If you update this value, the new subnet group must be a subnet group in a new VPC\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`PreferredMaintenanceWindow`  <a name="cfn-neptune-dbinstance-preferredmaintenancewindow"></a>
The weekly time range \(in UTC\) during which system maintenance can occur\. For valid values, see the `PreferredMaintenanceWindow` parameter for the [CreateDBInstance](docs.aws.amazon.com/neptune/latest/userguide/API_CreateDBInstance.html) action in the **\.  
This property applies when AWS CloudFormation initially creates the DB instance\. If you use AWS CloudFormation to update the DB instance, those updates are applied immediately\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) or [some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)\. For more information, see [ModifyDBInstance](docs.aws.amazon.com/neptune/latest/userguide/API_ModifyDBInstance.html) in the **\.

`StorageEncrypted`  <a name="cfn-neptune-dbinstance-storageencrypted"></a>
Indicates whether the DB instance is encrypted\.  
If you specify the `DBClusterIdentifier`, `DBSnapshotIdentifier`, or `SourceDBInstanceIdentifier` property, don't specify this property\. The value is inherited from the cluster, snapshot, or source DB instance\.  
*Required*: Conditional\. If you specify the `KmsKeyId` property, you must enable encryption\.  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Tags`  <a name="cfn-neptune-dbinstance-tags"></a>
An arbitrary set of tags \(key–value pairs\) for this DB instance\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Updating and Deleting AWS::Neptune::DBInstance Resources<a name="updating-and-deleting-dbinstance-resources"></a>

### Updating DB Instances<a name="w3ab2c21c10d897c13b2"></a>

When properties labeled "*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)" are updated, AWS CloudFormation first creates a replacement DB instance, then changes references from other dependent resources to point to the replacement DB instance, and finally deletes the old DB instance\.

**Important**  
We highly recommend that you take a snapshot of the database before updating the stack\. If you don't, you lose the data when AWS CloudFormation replaces your DB instance\. To preserve your data, perform the following procedure:  
Deactivate any applications that are using the DB instance so that there's no activity on the DB instance\.
Create a snapshot of the DB instance\.
If you want to restore your instance using a DB snapshot, modify the updated template with your DB instance changes and add the `DBSnapshotIdentifier` property with the ID of the DB snapshot that you want to use\.
Update the stack\.

### Deleting DB Instances<a name="w3ab2c21c10d897c13b4"></a>

You can set a deletion policy for your DB instance to control how AWS CloudFormation handles the instance when the stack is deleted\. For Neptune DB instances, you can choose to *retain* the instance, to *delete* the instance, or to *create a snapshot* of the instance\. The default AWS CloudFormation behavior depends on the `DBClusterIdentifier` property:
+ For `AWS::Neptune::DBInstance` resources that don't specify the `DBClusterIdentifier` property, AWS CloudFormation saves a snapshot of the DB instance\.
+ For `AWS::Neptune::DBInstance` resources that do specify the `DBClusterIdentifier` property, AWS CloudFormation deletes the DB instance\.

For more information, see [DeletionPolicy Attribute](aws-attribute-deletionpolicy.md)\.

## Return Values<a name="aws-resource-neptune-dbinstance-returnvalues"></a>

### Ref<a name="aws-resource-neptune-dbinstance-ref"></a>

When you provide the Neptune DB instance's logical name to the `Ref` intrinsic function, `Ref` returns the `DBInstanceIdentifier`\. For example: `mystack-mydb-ea5ugmfvuaxg`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="aws-resource-neptune-dbinstance-getatt"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.
+ **Endpoint**

  The connection endpoint for the database\. For example: `mystack-mydb-1apw1j4phylrk.cg034hpkmmjt.``us-east-2``.rds.amazonaws.com`\.
+ **Endpoint**

  The port number on which the database accepts connections\. For example: `8182`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.