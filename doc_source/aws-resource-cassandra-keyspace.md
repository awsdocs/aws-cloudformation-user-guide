# AWS::Cassandra::Keyspace<a name="aws-resource-cassandra-keyspace"></a>

The `AWS::Cassandra::Keyspace` resource allows you to create a new keyspace in Amazon Keyspaces \(for Apache Cassandra\)\. For more information, see [Create a keyspace and a table](https://docs.aws.amazon.com/keyspaces/latest/devguide/getting-started.ddl.html) in the *Amazon Keyspaces Developer Guide*\.

## Syntax<a name="aws-resource-cassandra-keyspace-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cassandra-keyspace-syntax.json"></a>

```
{
  "Type" : "AWS::Cassandra::Keyspace",
  "Properties" : {
      "[KeyspaceName](#cfn-cassandra-keyspace-keyspacename)" : String,
      "[Tags](#cfn-cassandra-keyspace-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-cassandra-keyspace-syntax.yaml"></a>

```
Type: AWS::Cassandra::Keyspace
Properties: 
  [KeyspaceName](#cfn-cassandra-keyspace-keyspacename): String
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

`Tags`  <a name="cfn-cassandra-keyspace-tags"></a>
A list of key\-value pair tags to be attached to the resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cassandra-keyspace-return-values"></a>

### Ref<a name="aws-resource-cassandra-keyspace-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the keyspace\. For example:

 `{ "Ref": "MyNewKeyspace" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-cassandra-keyspace--examples"></a>



### Create a New Keyspace<a name="aws-resource-cassandra-keyspace--examples--Create_a_New_Keyspace"></a>

The following example creates a new keyspace named `MyNewKeyspace` with the following tags `{'key1':'val1', 'key2':'val2'}`:

#### JSON<a name="aws-resource-cassandra-keyspace--examples--Create_a_New_Keyspace--json"></a>

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

#### YAML<a name="aws-resource-cassandra-keyspace--examples--Create_a_New_Keyspace--yaml"></a>

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