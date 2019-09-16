# AWS::DocDB::DBInstance<a name="aws-resource-docdb-dbinstance"></a>

The `AWS::DocDB::DBInstance` Amazon DocumentDB \(with MongoDB compatibility\) resource describes a DBInstance\. For more information, see [DBInstance](https://docs.aws.amazon.com/documentdb/latest/developerguide/API_DBInstance.html) in the *Amazon DocumentDB Developer Guide*\.

## Syntax<a name="aws-resource-docdb-dbinstance-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-docdb-dbinstance-syntax.json"></a>

```
{
  "Type" : "AWS::DocDB::DBInstance",
  "Properties" : {
      "[AutoMinorVersionUpgrade](#cfn-docdb-dbinstance-autominorversionupgrade)" : Boolean,
      "[AvailabilityZone](#cfn-docdb-dbinstance-availabilityzone)" : String,
      "[DBClusterIdentifier](#cfn-docdb-dbinstance-dbclusteridentifier)" : String,
      "[DBInstanceClass](#cfn-docdb-dbinstance-dbinstanceclass)" : String,
      "[DBInstanceIdentifier](#cfn-docdb-dbinstance-dbinstanceidentifier)" : String,
      "[PreferredMaintenanceWindow](#cfn-docdb-dbinstance-preferredmaintenancewindow)" : String,
      "[Tags](#cfn-docdb-dbinstance-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-docdb-dbinstance-syntax.yaml"></a>

```
Type: AWS::DocDB::DBInstance
Properties: 
  [AutoMinorVersionUpgrade](#cfn-docdb-dbinstance-autominorversionupgrade): Boolean
  [AvailabilityZone](#cfn-docdb-dbinstance-availabilityzone): String
  [DBClusterIdentifier](#cfn-docdb-dbinstance-dbclusteridentifier): String
  [DBInstanceClass](#cfn-docdb-dbinstance-dbinstanceclass): String
  [DBInstanceIdentifier](#cfn-docdb-dbinstance-dbinstanceidentifier): String
  [PreferredMaintenanceWindow](#cfn-docdb-dbinstance-preferredmaintenancewindow): String
  [Tags](#cfn-docdb-dbinstance-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-docdb-dbinstance-properties"></a>

`AutoMinorVersionUpgrade`  <a name="cfn-docdb-dbinstance-autominorversionupgrade"></a>
Indicates that minor engine upgrades are applied automatically to the DB instance during the maintenance window\.  
Default: `true`   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AvailabilityZone`  <a name="cfn-docdb-dbinstance-availabilityzone"></a>
 The Amazon EC2 Availability Zone that the DB instance is created in\.  
Default: A random, system\-chosen Availability Zone in the endpoint's AWS Region\.  
 Example: `us-east-1d`   
 Constraint: The `AvailabilityZone` parameter can't be specified if the `MultiAZ` parameter is set to `true`\. The specified Availability Zone must be in the same AWS Region as the current endpoint\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DBClusterIdentifier`  <a name="cfn-docdb-dbinstance-dbclusteridentifier"></a>
The identifier of the DB cluster that the instance will belong to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DBInstanceClass`  <a name="cfn-docdb-dbinstance-dbinstanceclass"></a>
The compute and memory capacity of the DB instance; for example, `db.m4.large`\. If you change the class of an instance there can be some interruption in the cluster's service\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DBInstanceIdentifier`  <a name="cfn-docdb-dbinstance-dbinstanceidentifier"></a>
The DB instance identifier\. This parameter is stored as a lowercase string\.  
Constraints:  
+ Must contain from 1 to 63 letters, numbers, or hyphens\.
+ The first character must be a letter\.
+ Cannot end with a hyphen or contain two consecutive hyphens\.
Example: `mydbinstance`   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PreferredMaintenanceWindow`  <a name="cfn-docdb-dbinstance-preferredmaintenancewindow"></a>
The time range each week during which system maintenance can occur, in Universal Coordinated Time \(UTC\)\.  
 Format: `ddd:hh24:mi-ddd:hh24:mi`   
The default is a 30\-minute window selected at random from an 8\-hour block of time for each AWS Region, occurring on a random day of the week\.   
Valid days: Mon, Tue, Wed, Thu, Fri, Sat, Sun  
Constraints: Minimum 30\-minute window\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-docdb-dbinstance-tags"></a>
The tags to be assigned to the DB instance\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-docdb-dbinstance-return-values"></a>

### Ref<a name="aws-resource-docdb-dbinstance-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the DBInstance's name, such as `sample-cluster-instance`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-docdb-dbinstance-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-docdb-dbinstance-return-values-fn--getatt-fn--getatt"></a>

`Endpoint`  <a name="Endpoint-fn::getatt"></a>
The connection endpoint for the DB instance\. For example: `sample-cluster.cluster-abcdefghijkl.us-east-1.docdb.amazonaws.com`\.

`Port`  <a name="Port-fn::getatt"></a>
The port number on which the database accepts connections, such as `27017`\.

## Examples<a name="aws-resource-docdb-dbinstance--examples"></a>

### <a name="aws-resource-docdb-dbinstance--examples--"></a>

#### JSON<a name="aws-resource-docdb-dbinstance--examples----json"></a>

```
{
   "Type" : "AWS::DocDB::DBInstance",
   "Properties" : {
      "AutoMinorVersionUpgrade" : Boolean,
      "AvailabilityZone" : String,
      "DBClusterIdentifier" : String,
      "DBInstanceClass" : String,
      "DBInstanceIdentifier" : String,
      "PreferredMaintenanceWindow" : String,
      "Tags" : [ Tag, ... ]
   }
}
```

#### YAML<a name="aws-resource-docdb-dbinstance--examples----yaml"></a>

```
Type: "AWS::DocDB::DBInstance"
Properties:
   AutoMinorVersionUpgrade: Boolean
   AvailabilityZone: String
   DBClusterIdentifier: String
   DBInstanceClass: String
   DBInstanceIdentifier: String
   PreferredMaintenanceWindow: String
   Tags:
      - Tag
```

## See Also<a name="aws-resource-docdb-dbinstance--seealso"></a>
+  [DBInstance](https://docs.aws.amazon.com/documentdb/latest/developerguide/API_DBInstance.html) 
+  [CreateDBInstance](https://docs.aws.amazon.com/documentdb/latest/developerguide/API_CreateDBInstance.html) 
+  [DeleteDBInstance](https://docs.aws.amazon.com/documentdb/latest/developerguide/API_DeleteDBInstance.html) 
+  [DescribeDBInstances](https://docs.aws.amazon.com/documentdb/latest/developerguide/API_DescribeDBInstances.html) 
+  [ModifyDBInstance](https://docs.aws.amazon.com/documentdb/latest/developerguide/API_ModifyDBInstance.html) 