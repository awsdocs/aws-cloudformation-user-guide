# AWS::IoT::DomainConfiguration Tags<a name="aws-properties-iot-domainconfiguration-tags"></a>

Metadata which can be used to manage the domain configuration\.

**Note**  
For URI Request parameters use format: \.\.\.key1=value1&key2=value2\.\.\.  
For the CLI command\-line parameter use format: &&tags "key1=value1&key2=value2\.\.\."  
For the cli\-input\-json file use format: "tags": "key1=value1&key2=value2\.\.\."

## Syntax<a name="aws-properties-iot-domainconfiguration-tags-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-domainconfiguration-tags-syntax.json"></a>

```
{
  "[Tags](#cfn-iot-domainconfiguration-tags-tags)" : [ Json, ... ]
}
```

### YAML<a name="aws-properties-iot-domainconfiguration-tags-syntax.yaml"></a>

```
  [Tags](#cfn-iot-domainconfiguration-tags-tags): 
    - Json
```

## Properties<a name="aws-properties-iot-domainconfiguration-tags-properties"></a>

`Tags`  <a name="cfn-iot-domainconfiguration-tags-tags"></a>
Metadata which can be used to manage the domain configuration\.  
For URI Request parameters use format: \.\.\.key1=value1&key2=value2\.\.\.  
For the CLI command\-line parameter use format: &&tags "key1=value1&key2=value2\.\.\."  
For the cli\-input\-json file use format: "tags": "key1=value1&key2=value2\.\.\."
*Required*: No  
*Type*: [List](#aws-properties-iot-domainconfiguration-tags) of [Json](#aws-properties-iot-domainconfiguration-tags)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)