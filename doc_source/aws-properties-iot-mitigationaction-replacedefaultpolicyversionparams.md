# AWS::IoT::MitigationAction ReplaceDefaultPolicyVersionParams<a name="aws-properties-iot-mitigationaction-replacedefaultpolicyversionparams"></a>

Parameters to define a mitigation action that adds a blank policy to restrict permissions\.

## Syntax<a name="aws-properties-iot-mitigationaction-replacedefaultpolicyversionparams-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-mitigationaction-replacedefaultpolicyversionparams-syntax.json"></a>

```
{
  "[TemplateName](#cfn-iot-mitigationaction-replacedefaultpolicyversionparams-templatename)" : String
}
```

### YAML<a name="aws-properties-iot-mitigationaction-replacedefaultpolicyversionparams-syntax.yaml"></a>

```
  [TemplateName](#cfn-iot-mitigationaction-replacedefaultpolicyversionparams-templatename): String
```

## Properties<a name="aws-properties-iot-mitigationaction-replacedefaultpolicyversionparams-properties"></a>

`TemplateName`  <a name="cfn-iot-mitigationaction-replacedefaultpolicyversionparams-templatename"></a>
The name of the template to be applied\. The only supported value is `BLANK_POLICY`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)