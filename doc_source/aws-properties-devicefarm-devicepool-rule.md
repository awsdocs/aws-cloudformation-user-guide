# AWS::DeviceFarm::DevicePool Rule<a name="aws-properties-devicefarm-devicepool-rule"></a>

Represents a condition for a device pool\.

## Syntax<a name="aws-properties-devicefarm-devicepool-rule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-devicefarm-devicepool-rule-syntax.json"></a>

```
{
  "[Attribute](#cfn-devicefarm-devicepool-rule-attribute)" : String,
  "[Operator](#cfn-devicefarm-devicepool-rule-operator)" : String,
  "[Value](#cfn-devicefarm-devicepool-rule-value)" : String
}
```

### YAML<a name="aws-properties-devicefarm-devicepool-rule-syntax.yaml"></a>

```
  [Attribute](#cfn-devicefarm-devicepool-rule-attribute): String
  [Operator](#cfn-devicefarm-devicepool-rule-operator): String
  [Value](#cfn-devicefarm-devicepool-rule-value): String
```

## Properties<a name="aws-properties-devicefarm-devicepool-rule-properties"></a>

`Attribute`  <a name="cfn-devicefarm-devicepool-rule-attribute"></a>
The rule's stringified attribute\. For example, specify the value as `"\"abc\""`\.  
The supported operators for each attribute are provided in the following list\.    
APPIUM\_VERSION  
The Appium version for the test\.  
Supported operators: `CONTAINS`   
ARN  
The Amazon Resource Name \(ARN\) of the device \(for example, `arn:aws:devicefarm:us-west-2::device:12345Example`\.  
Supported operators: `EQUALS`, `IN`, `NOT_IN`   
AVAILABILITY  
The current availability of the device\. Valid values are AVAILABLE, HIGHLY\_AVAILABLE, BUSY, or TEMPORARY\_NOT\_AVAILABLE\.  
Supported operators: `EQUALS`   
FLEET\_TYPE  
The fleet type\. Valid values are PUBLIC or PRIVATE\.  
Supported operators: `EQUALS`   
FORM\_FACTOR  
The device form factor\. Valid values are PHONE or TABLET\.  
Supported operators: `EQUALS`, `IN`, `NOT_IN`   
INSTANCE\_ARN  
The Amazon Resource Name \(ARN\) of the device instance\.  
Supported operators: `IN`, `NOT_IN`   
INSTANCE\_LABELS  
The label of the device instance\.  
Supported operators: `CONTAINS`   
MANUFACTURER  
The device manufacturer \(for example, Apple\)\.  
Supported operators: `EQUALS`, `IN`, `NOT_IN`   
MODEL  
The device model, such as Apple iPad Air 2 or Google Pixel\.  
Supported operators: `CONTAINS`, `EQUALS`, `IN`, `NOT_IN`   
OS\_VERSION  
The operating system version \(for example, 10\.3\.2\)\.  
Supported operators: `EQUALS`, `GREATER_THAN`, `GREATER_THAN_OR_EQUALS`, `IN`, `LESS_THAN`, `LESS_THAN_OR_EQUALS`, `NOT_IN`   
PLATFORM  
The device platform\. Valid values are ANDROID or IOS\.  
Supported operators: `EQUALS`, `IN`, `NOT_IN`   
REMOTE\_ACCESS\_ENABLED  
Whether the device is enabled for remote access\. Valid values are TRUE or FALSE\.  
Supported operators: `EQUALS`   
REMOTE\_DEBUG\_ENABLED  
Whether the device is enabled for remote debugging\. Valid values are TRUE or FALSE\.  
Supported operators: `EQUALS`   
Because remote debugging is [no longer supported](https://docs.aws.amazon.com/devicefarm/latest/developerguide/history.html), this filter is ignored\.
*Required*: No  
*Type*: String  
*Allowed values*: `APPIUM_VERSION | ARN | AVAILABILITY | FLEET_TYPE | FORM_FACTOR | INSTANCE_ARN | INSTANCE_LABELS | MANUFACTURER | MODEL | OS_VERSION | PLATFORM | REMOTE_ACCESS_ENABLED | REMOTE_DEBUG_ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Operator`  <a name="cfn-devicefarm-devicepool-rule-operator"></a>
Specifies how Device Farm compares the rule's attribute to the value\. For the operators that are supported by each attribute, see the attribute descriptions\.  
*Required*: No  
*Type*: String  
*Allowed values*: `CONTAINS | EQUALS | GREATER_THAN | GREATER_THAN_OR_EQUALS | IN | LESS_THAN | LESS_THAN_OR_EQUALS | NOT_IN`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-devicefarm-devicepool-rule-value"></a>
The rule's value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)