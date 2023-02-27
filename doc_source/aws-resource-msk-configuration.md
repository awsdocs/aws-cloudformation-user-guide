# AWS::MSK::Configuration<a name="aws-resource-msk-configuration"></a>

Creates a new MSK configuration\.

## Syntax<a name="aws-resource-msk-configuration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-msk-configuration-syntax.json"></a>

```
{
  "Type" : "AWS::MSK::Configuration",
  "Properties" : {
      "[Description](#cfn-msk-configuration-description)" : String,
      "[KafkaVersionsList](#cfn-msk-configuration-kafkaversionslist)" : [ String, ... ],
      "[Name](#cfn-msk-configuration-name)" : String,
      "[ServerProperties](#cfn-msk-configuration-serverproperties)" : String
    }
}
```

### YAML<a name="aws-resource-msk-configuration-syntax.yaml"></a>

```
Type: AWS::MSK::Configuration
Properties: 
  [Description](#cfn-msk-configuration-description): String
  [KafkaVersionsList](#cfn-msk-configuration-kafkaversionslist): 
    - String
  [Name](#cfn-msk-configuration-name): String
  [ServerProperties](#cfn-msk-configuration-serverproperties): String
```

## Properties<a name="aws-resource-msk-configuration-properties"></a>

`Description`  <a name="cfn-msk-configuration-description"></a>
The description of the configuration\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KafkaVersionsList`  <a name="cfn-msk-configuration-kafkaversionslist"></a>
A list of the versions of Apache Kafka with which you can use this MSK configuration\. You can use this configuration for an MSK cluster only if the Apache Kafka version specified for the cluster appears in this list\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-msk-configuration-name"></a>
The name of the configuration\. Configuration names are strings that match the regex "^\[0\-9A\-Za\-z\]\[0\-9A\-Za\-z\-\]\{0,\}$"\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServerProperties`  <a name="cfn-msk-configuration-serverproperties"></a>
Contents of the `server.properties` file\. When using the API, you must ensure that the contents of the file are base64 encoded\. When using the console, the SDK, or the CLI, the contents of `server.properties` can be in plaintext\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-msk-configuration-return-values"></a>

### Ref<a name="aws-resource-msk-configuration-return-values-ref"></a>

The ARN of the configuration\.

### Fn::GetAtt<a name="aws-resource-msk-configuration-return-values-fn--getatt"></a>

The ARN of the configuration\.

#### <a name="aws-resource-msk-configuration-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the configuration\.