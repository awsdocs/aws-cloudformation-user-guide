# AWS::Events::Connection Parameter<a name="aws-properties-events-connection-parameter"></a>

Additional query string parameter for the connection\. You can include up to 100 additional query string parameters per request\. Each additional parameter counts towards the event payload size, which cannot exceed 64 KB\.

## Syntax<a name="aws-properties-events-connection-parameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-connection-parameter-syntax.json"></a>

```
{
  "[IsValueSecret](#cfn-events-connection-parameter-isvaluesecret)" : Boolean,
  "[Key](#cfn-events-connection-parameter-key)" : String,
  "[Value](#cfn-events-connection-parameter-value)" : String
}
```

### YAML<a name="aws-properties-events-connection-parameter-syntax.yaml"></a>

```
  [IsValueSecret](#cfn-events-connection-parameter-isvaluesecret): Boolean
  [Key](#cfn-events-connection-parameter-key): String
  [Value](#cfn-events-connection-parameter-value): String
```

## Properties<a name="aws-properties-events-connection-parameter-properties"></a>

`IsValueSecret`  <a name="cfn-events-connection-parameter-isvaluesecret"></a>
Specifies whether the value is secret\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Key`  <a name="cfn-events-connection-parameter-key"></a>
The key for a query string parameter\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `[^\x00-\x1F\x7F]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-events-connection-parameter-value"></a>
The value associated with the key for the query string parameter\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `[^\x00-\x09\x0B\x0C\x0E-\x1F\x7F]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)