# AWS::SecurityHub::Standard StandardsControl<a name="aws-properties-securityhub-standard-standardscontrol"></a>

Provides details about an individual security control\. For a list of Security Hub controls, see [Security Hub controls reference](https://docs.aws.amazon.com/securityhub/latest/userguide/securityhub-controls-reference.html) in the *AWS Security Hub User Guide*\.

## Syntax<a name="aws-properties-securityhub-standard-standardscontrol-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-securityhub-standard-standardscontrol-syntax.json"></a>

```
{
  "[Reason](#cfn-securityhub-standard-standardscontrol-reason)" : String,
  "[StandardsControlArn](#cfn-securityhub-standard-standardscontrol-standardscontrolarn)" : String
}
```

### YAML<a name="aws-properties-securityhub-standard-standardscontrol-syntax.yaml"></a>

```
  [Reason](#cfn-securityhub-standard-standardscontrol-reason): String
  [StandardsControlArn](#cfn-securityhub-standard-standardscontrol-standardscontrolarn): String
```

## Properties<a name="aws-properties-securityhub-standard-standardscontrol-properties"></a>

`Reason`  <a name="cfn-securityhub-standard-standardscontrol-reason"></a>
A user\-defined reason for changing a control's enablement status in a specified standard\.  
*Required*: No  
*Type*: String  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StandardsControlArn`  <a name="cfn-securityhub-standard-standardscontrol-standardscontrolarn"></a>
The Amazon Resource Name \(ARN\) of the control\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)