# AWS::IoT::CACertificate RegistrationConfig<a name="aws-properties-iot-cacertificate-registrationconfig"></a>

The registration configuration\.

## Syntax<a name="aws-properties-iot-cacertificate-registrationconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-cacertificate-registrationconfig-syntax.json"></a>

```
{
  "[RoleArn](#cfn-iot-cacertificate-registrationconfig-rolearn)" : String,
  "[TemplateBody](#cfn-iot-cacertificate-registrationconfig-templatebody)" : String,
  "[TemplateName](#cfn-iot-cacertificate-registrationconfig-templatename)" : String
}
```

### YAML<a name="aws-properties-iot-cacertificate-registrationconfig-syntax.yaml"></a>

```
  [RoleArn](#cfn-iot-cacertificate-registrationconfig-rolearn): String
  [TemplateBody](#cfn-iot-cacertificate-registrationconfig-templatebody): String
  [TemplateName](#cfn-iot-cacertificate-registrationconfig-templatename): String
```

## Properties<a name="aws-properties-iot-cacertificate-registrationconfig-properties"></a>

`RoleArn`  <a name="cfn-iot-cacertificate-registrationconfig-rolearn"></a>
The ARN of the role\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemplateBody`  <a name="cfn-iot-cacertificate-registrationconfig-templatebody"></a>
The template body\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemplateName`  <a name="cfn-iot-cacertificate-registrationconfig-templatename"></a>
The name of the provisioning template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)