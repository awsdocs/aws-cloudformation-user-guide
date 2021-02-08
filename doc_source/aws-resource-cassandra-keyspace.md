# AWS::Cassandra::Keyspace<a name="aws-resource-cassandra-keyspace"></a>

The `AWS::Cassandra::Keyspace` resource allows you to create a new keyspace in Amazon Keyspaces \(for Apache Cassandra\)\. For more information, see [Create a Keyspace and a Table](https://docs.aws.amazon.com/keyspaces/latest/devguide/getting-started.ddl.html) in the *Amazon Keyspaces Developer Guide*\.

## Syntax<a name="aws-resource-cassandra-keyspace-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cassandra-keyspace-syntax.json"></a>

```
{
  "Type" : "AWS::Cassandra::Keyspace",
  "Properties" : {
      "[KeyspaceName](#cfn-cassandra-keyspace-keyspacename)" : String
    }
}
```

### YAML<a name="aws-resource-cassandra-keyspace-syntax.yaml"></a>

```
Type: AWS::Cassandra::Keyspace
Properties: 
  [KeyspaceName](#cfn-cassandra-keyspace-keyspacename): String
```

## Properties<a name="aws-resource-cassandra-keyspace-properties"></a>

`KeyspaceName`  <a name="cfn-cassandra-keyspace-keyspacename"></a>
The name of the keyspace to be created\. If you don't specify a name, AWS CloudFormation generates a unique ID and uses that ID for the keyspace name\. For more information, see [Name Type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html)\.  
*Length Constraints:* Minimum length of 3\. Maximum length of 255\.  
*Pattern:* `^[a-zA-Z0-9][a-zA-Z0-9_]{1,47}$`  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-cassandra-keyspace-return-values"></a>

### Ref<a name="aws-resource-cassandra-keyspace-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the keyspace\. For example:

 `{ "Ref": "MyNewKeyspace" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-cassandra-keyspace--examples"></a>



### Create a New Keyspace<a name="aws-resource-cassandra-keyspace--examples--Create_a_New_Keyspace"></a>

The following example creates a new keyspace named `MyNewKeyspace`:

#### JSON<a name="aws-resource-cassandra-keyspace--examples--Create_a_New_Keyspace--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Resources": {
    "MyNewKeyspace": {
      "Type": "AWS::Cassandra::Keyspace",
      "Properties": {
        "KeyspaceName": "MyNewKeyspace"
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
```