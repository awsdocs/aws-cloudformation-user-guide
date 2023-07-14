# AWS::Cassandra::Keyspace<a name="aws-resource-cassandra-keyspace"></a>

You can use the `AWS::Cassandra::Keyspace` resource to create a new keyspace in Amazon Keyspaces \(for Apache Cassandra\)\. For more information, see [Create a keyspace and a table](https://docs.aws.amazon.com/keyspaces/latest/devguide/getting-started.ddl.html) in the *Amazon Keyspaces Developer Guide*\.

## Syntax<a name="aws-resource-cassandra-keyspace-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cassandra-keyspace-syntax.json"></a>

```
{
  "Type" : "AWS::Cassandra::Keyspace",
  "Properties" : {
      "[KeyspaceName](#cfn-cassandra-keyspace-keyspacename)" : String,
      "[ReplicationSpecification](#cfn-cassandra-keyspace-replicationspecification)" : ReplicationSpecification,
      "[Tags](#cfn-cassandra-keyspace-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-cassandra-keyspace-syntax.yaml"></a>

```
Type: AWS::Cassandra::Keyspace
Properties: 
  [KeyspaceName](#cfn-cassandra-keyspace-keyspacename): String
  [ReplicationSpecification](#cfn-cassandra-keyspace-replicationspecification): 
    ReplicationSpecification
  [Tags](#cfn-cassandra-keyspace-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-cassandra-keyspace-properties"></a>

`KeyspaceName`  <a name="cfn-cassandra-keyspace-keyspacename"></a>
The name of the keyspace to be created\. The keyspace name is case sensitive\. If you don't specify a name, AWS CloudFormation generates a unique ID and uses that ID for the keyspace name\. For more information, see [Name type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html)\.  
*Length constraints:* Minimum length of 3\. Maximum length of 255\.  
*Pattern:* `^[a-zA-Z0-9][a-zA-Z0-9_]{1,47}$`  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ReplicationSpecification`  <a name="cfn-cassandra-keyspace-replicationspecification"></a>
Specifies the `ReplicationStrategy` of a keyspace\. The options are:  
+ `SINGLE_REGION` for a single Region keyspace \(optional\) or
+ `MULTI_REGION` for a multi\-Region keyspace
 If no `ReplicationStrategy` is provided, the default is `SINGLE_REGION`\. If you choose `MULTI_REGION`, you must also provide a `RegionList` with the AWS Regions that the keyspace is replicated in\.   
*Required*: No  
*Type*: [ReplicationSpecification](aws-properties-cassandra-keyspace-replicationspecification.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-cassandra-keyspace-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cassandra-keyspace-return-values"></a>

### Ref<a name="aws-resource-cassandra-keyspace-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the name of the keyspace\. For example:

 `{ "Ref": "MyNewKeyspace" }` 

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-cassandra-keyspace--examples"></a>

This section includes code examples that demonstrate how to create a keyspace using the different options\.

### Create a new keyspace with tags<a name="aws-resource-cassandra-keyspace--examples--Create_a_new_keyspace_with_tags"></a>

The following example creates a new keyspace named `MyNewKeyspace` with the following tags: `{'key1':'val1', 'key2':'val2'}`\.

#### JSON<a name="aws-resource-cassandra-keyspace--examples--Create_a_new_keyspace_with_tags--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Resources": {
    "MyNewKeyspace": {
      "Type": "AWS::Cassandra::Keyspace",
      "Properties": {
        "KeyspaceName": "MyNewKeyspace",
        "Tags": [{"Key":"tag1","Value":"val1"}, {"Key":"tag2","Value":"val2"}]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-cassandra-keyspace--examples--Create_a_new_keyspace_with_tags--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  MyNewKeyspace:
    Type: AWS::Cassandra::Keyspace
    Properties:
      KeyspaceName: MyNewKeyspace
      Tags:
      - Key: tag1
      Value: val1
      - Key: tag2
      Value: val2
```

### Create a new multi\-Region keyspace<a name="aws-resource-cassandra-keyspace--examples--Create_a_new_multi-Region_keyspace"></a>

The following example creates a new multi\-Region keyspace named `MultiRegionKeyspace` that is replicated across three AWS Regions\.

#### JSON<a name="aws-resource-cassandra-keyspace--examples--Create_a_new_multi-Region_keyspace--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Resources": {
    "MultiRegionKeyspace": {
      "Type": "AWS::Cassandra::Keyspace",
      "Properties": {
        "KeyspaceName": "MultiRegionKeyspace",
        "ReplicationSpecification": {
          "ReplicationStrategy": "MULTI_REGION",
          "RegionList": ["us-east-1", "us-west-2", "eu-west-1"]
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-cassandra-keyspace--examples--Create_a_new_multi-Region_keyspace--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  MultiRegionKeyspace:
    Type: AWS::Cassandra::Keyspace
    Properties:
      KeyspaceName: MultiRegionKeyspace
      ReplicationSpecification:
        ReplicationStrategy: MULTI_REGION
        RegionList:
          - us-east-1
          - us-west-2
          - eu-west-1
```