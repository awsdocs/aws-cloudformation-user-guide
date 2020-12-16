# UpdateReplacePolicy attribute<a name="aws-attribute-updatereplacepolicy"></a>

Use the UpdateReplacePolicy attribute to retain or \(in some cases\) backup the existing physical instance of a resource when it is replaced during a stack update operation\. 

When you initiate a stack update, AWS CloudFormation updates resources based on differences between what you submit and the stack's current template and parameters\. If you update a resource property that requires that the resource be [replaced](using-cfn-updating-stacks-update-behaviors.md#update-replacement), AWS CloudFormation recreates the resource during the update\. Recreating the resource generates a new physical ID\. AWS CloudFormation creates the replacement resource first, and then changes references from other dependent resources to point to the replacement resource\. By default, AWS CloudFormation then deletes the old resource\. Using the UpdateReplacePolicy, you can specify that AWS CloudFormation retain or \(in some cases\) create a snapshot of the old resource\.

For resources that support snapshots, such as `AWS::EC2::Volume`, specify `Snapshot` to have AWS CloudFormation create a snapshot before deleting the old resource instance\.

You can apply the UpdateReplacePolicy attribute to any resource\. UpdateReplacePolicy is only executed if you update a resource property whose update behavior is specified as [**Replacement**](using-cfn-updating-stacks-update-behaviors.md#update-replacement), thereby causing AWS CloudFormation to replace the old resource with a new one with a new physical ID\. For example, if you update the `Engine` property of an [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html) resource type, AWS CloudFormation creates a new resource and replaces the current DB instance resource with the new one\. The UpdateReplacePolicy attribute would then dictate whether AWS CloudFormation deleted, retained, or created a snapshot of the old DB instance\. The update behavior for each property of a resource is specified in the reference topic for that resource in the [AWS resource and property types reference](aws-template-resource-type-ref.md)\. For more information on resource update behavior, see [Update behaviors of stack resources](using-cfn-updating-stacks-update-behaviors.md)\.

The UpdateReplacePolicy attribute applies to [stack updates you perform directly](using-cfn-updating-stacks-direct.md), as well as stack updates performed using [change sets](using-cfn-updating-stacks-changesets.md)\.

**Note**  
Resources that are retained continue to exist and continue to incur applicable charges until you delete those resources\. Snapshots that are created with this policy continue to exist and continue to incur applicable charges until you delete those snapshots\. UpdateReplacePolicy retains the old physical resource or snapshot, but removes it from AWS CloudFormation's scope\. 

UpdateReplacePolicy differs from the [DeletionPolicy](aws-attribute-deletionpolicy.md) attribute in that it only applies to resources replaced during stack updates\. Use DeletionPolicy for resources deleted when a stack is deleted, or when the resource definition itself is deleted from the template as part of a stack update\. 

The following snippet contains an Amazon RDS database instance resource with a `Retain` policy for replacement\. When this resource is replaced with a new resource with a new physical ID, AWS CloudFormation leaves the old database instance without deleting it\.

## JSON<a name="aws-attribute-updatereplacepolicy-example.json"></a>

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",
  "Resources" : {
    "myDB" : {
      "Type" : "AWS::RDS::DBInstance",
      "DeletionPolicy" : "Retain",
      "UpdateReplacePolicy" : "Retain",
      "Properties" : {}
    }
  }
}
```

## YAML<a name="aws-attribute-updatereplacepolicy-example.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  myDB:
    Type: 'AWS::RDS::DBInstance'
    DeletionPolicy: Retain
    UpdateReplacePolicy: Retain
    Properties: {}
```

## UpdateReplacePolicy options<a name="aws-attribute-updatereplacepolicy-options"></a>

Delete  
AWS CloudFormation deletes the resource and all its content if applicable during resource replacement\. You can add this policy to any resource type\. By default, if you don't specify an UpdateReplacePolicy, AWS CloudFormation deletes your resources\. However, be aware of the following consideration:  
For Amazon S3 buckets, you must delete all objects in the bucket for deletion to succeed\.

Retain  
AWS CloudFormation keeps the resource without deleting the resource or its contents when the resource is replaced\. You can add this policy to any resource type\. Note that resources that are retained continue to exist and continue to incur applicable charges until you delete those resources\.  
If a resource is replaced, the UpdateReplacePolicy retains the old physical resource but removes it from AWS CloudFormation's scope\.

Snapshot  
For resources that support snapshots, AWS CloudFormation creates a snapshot for the resource before deleting it\. Note that snapshots that are created with this policy continue to exist and continue to incur applicable charges until you delete those snapshots\.  
If you specify the `Snapshot` option in the UpdateReplacePolicy for a resource that does not support snapshots, CloudFormation reverts to the default option, which is `Delete`\.
Resources that support snapshots include:  
+ `[AWS::EC2::Volume](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-ebs-volume.html)`
+ `[AWS::ElastiCache::CacheCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticache-cache-cluster.html)`
+ `[AWS::ElastiCache::ReplicationGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticache-replicationgroup.html)`
+ `[AWS::Neptune::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-neptune-dbcluster.html)`
+ `[AWS::RDS::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbcluster.html)`
+ `[AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html)`
+ `[AWS::Redshift::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-redshift-cluster.html)`