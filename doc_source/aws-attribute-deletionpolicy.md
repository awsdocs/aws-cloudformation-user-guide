# DeletionPolicy attribute<a name="aws-attribute-deletionpolicy"></a>

With the DeletionPolicy attribute you can preserve or \(in some cases\) backup a resource when its stack is deleted\. You specify a DeletionPolicy attribute for each resource that you want to control\. If a resource has no DeletionPolicy attribute, AWS CloudFormation deletes the resource by default\.

Note that this capability also applies to stack update operations that lead to resources being deleted from stacks\. For example, if you remove the resource from the stack template, and then update the stack with the template\. This capability does not apply to resources whose physical instance is replaced during stack update operations\. For example, if you edit a resource's properties such that AWS CloudFormation replaces that resource during a stack update\.

**Note**  
**Exception**: The default policy is `Snapshot` for `AWS::RDS::DBCluster` resources and for `AWS::RDS::DBInstance` resources that don't specify the `DBClusterIdentifier` property\.

To keep a resource when its stack is deleted, specify `Retain` for that resource\. You can use retain for any resource\. For example, you can retain a nested stack, Amazon S3 bucket, or EC2 instance so that you can continue to use or modify those resources after you delete their stacks\.

**Note**  
If you want to modify resources outside of AWS CloudFormation, use a retain policy and then delete the stack\. Otherwise, your resources might get out of sync with your AWS CloudFormation template and cause stack errors\.

For resources that support snapshots, such as `AWS::EC2::Volume`, specify `Snapshot` to have AWS CloudFormation create a snapshot before deleting the resource\.

The following snippet contains an Amazon S3 bucket resource with a `Retain` deletion policy\. When this stack is deleted, AWS CloudFormation leaves the bucket without deleting it\.

## JSON<a name="aws-attribute-deletionpolicy-example.json"></a>

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",
  "Resources" : {
    "myS3Bucket" : {
      "Type" : "AWS::S3::Bucket",
      "DeletionPolicy" : "Retain"
    }
  }
}
```

## YAML<a name="aws-attribute-deletionpolicy-example.yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  myS3Bucket:
    Type: AWS::S3::Bucket
    DeletionPolicy: Retain
```

## DeletionPolicy options<a name="aws-attribute-deletionpolicy-options"></a>

Delete  
AWS CloudFormation deletes the resource and all its content if applicable during stack deletion\. You can add this deletion policy to any resource type\. By default, if you don't specify a DeletionPolicy, AWS CloudFormation deletes your resources\. However, be aware of the following considerations:  
+ For `AWS::RDS::DBCluster` resources, the default policy is `Snapshot`\.
+ For `AWS::RDS::DBInstance` resources that don't specify the `DBClusterIdentifier` property, the default policy is `Snapshot`\.
+ For Amazon S3 buckets, you must delete all objects in the bucket for deletion to succeed\.

Retain  
AWS CloudFormation keeps the resource without deleting the resource or its contents when its stack is deleted\. You can add this deletion policy to any resource type\. Note that when AWS CloudFormation completes the stack deletion, the stack will be in `Delete_Complete` state; however, resources that are retained continue to exist and continue to incur applicable charges until you delete those resources\.  
For update operations, the following considerations apply:  
+ If a resource is deleted, the DeletionPolicy retains the physical resource but ensures that it's deleted from AWS CloudFormation's scope\.
+ If a resource is updated such that a new physical resource is created to replace the old resource, then the old resource is completely deleted, including from AWS CloudFormation's scope\.

Snapshot  
For resources that support snapshots, AWS CloudFormation creates a snapshot for the resource before deleting it\. Note that when AWS CloudFormation completes the stack deletion, the stack will be in the `Delete_Complete` state; however, the snapshots that are created with this policy continue to exist and continue to incur applicable charges until you delete those snapshots\.  
Resources that support snapshots include:  
+ `[AWS::EC2::Volume](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-ebs-volume.html)`
+ `[AWS::ElastiCache::CacheCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticache-cache-cluster.html)`
+ `[AWS::ElastiCache::ReplicationGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticache-replicationgroup.html)`
+ `[AWS::Neptune::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-neptune-dbcluster.html)`
+ `[AWS::RDS::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbcluster.html)`
+ `[AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html)`
+ `[AWS::Redshift::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-redshift-cluster.html)`