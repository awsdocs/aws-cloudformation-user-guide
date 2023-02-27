# AWS::DynamoDB::GlobalTable TimeToLiveSpecification<a name="aws-properties-dynamodb-globaltable-timetolivespecification"></a>

Represents the settings used to enable or disable Time to Live \(TTL\) for the specified table\. All replicas will have the same time to live configuration\.

## Syntax<a name="aws-properties-dynamodb-globaltable-timetolivespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dynamodb-globaltable-timetolivespecification-syntax.json"></a>

```
{
  "[AttributeName](#cfn-dynamodb-globaltable-timetolivespecification-attributename)" : String,
  "[Enabled](#cfn-dynamodb-globaltable-timetolivespecification-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-dynamodb-globaltable-timetolivespecification-syntax.yaml"></a>

```
  [AttributeName](#cfn-dynamodb-globaltable-timetolivespecification-attributename): String
  [Enabled](#cfn-dynamodb-globaltable-timetolivespecification-enabled): Boolean
```

## Properties<a name="aws-properties-dynamodb-globaltable-timetolivespecification-properties"></a>

`AttributeName`  <a name="cfn-dynamodb-globaltable-timetolivespecification-attributename"></a>
The name of the attribute used to store the expiration time for items in the table\.  
Currently, you cannot directly change the attribute name used to evaluate time to live\. In order to do so, you must first disable time to live, and then re\-enable it with the new attribute name\. It can take up to one hour for changes to time to live to take effect\. If you attempt to modify time to live within that time window, your stack operation might be delayed\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-dynamodb-globaltable-timetolivespecification-enabled"></a>
Indicates whether TTL is to be enabled \(true\) or disabled \(false\) on the table\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)