# AWS::LicenseManager::License Entitlement<a name="aws-properties-licensemanager-license-entitlement"></a>

Describes a resource entitled for use with a license\.

## Syntax<a name="aws-properties-licensemanager-license-entitlement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-licensemanager-license-entitlement-syntax.json"></a>

```
{
  "[AllowCheckIn](#cfn-licensemanager-license-entitlement-allowcheckin)" : Boolean,
  "[CheckoutRules](#cfn-licensemanager-license-entitlement-checkoutrules)" : RuleList,
  "[MaxCount](#cfn-licensemanager-license-entitlement-maxcount)" : Integer,
  "[Name](#cfn-licensemanager-license-entitlement-name)" : String,
  "[Overage](#cfn-licensemanager-license-entitlement-overage)" : Boolean,
  "[Unit](#cfn-licensemanager-license-entitlement-unit)" : String,
  "[Value](#cfn-licensemanager-license-entitlement-value)" : String
}
```

### YAML<a name="aws-properties-licensemanager-license-entitlement-syntax.yaml"></a>

```
  [AllowCheckIn](#cfn-licensemanager-license-entitlement-allowcheckin): Boolean
  [CheckoutRules](#cfn-licensemanager-license-entitlement-checkoutrules): 
    RuleList
  [MaxCount](#cfn-licensemanager-license-entitlement-maxcount): Integer
  [Name](#cfn-licensemanager-license-entitlement-name): String
  [Overage](#cfn-licensemanager-license-entitlement-overage): Boolean
  [Unit](#cfn-licensemanager-license-entitlement-unit): String
  [Value](#cfn-licensemanager-license-entitlement-value): String
```

## Properties<a name="aws-properties-licensemanager-license-entitlement-properties"></a>

`AllowCheckIn`  <a name="cfn-licensemanager-license-entitlement-allowcheckin"></a>
Indicates whether check\-ins are allowed\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CheckoutRules`  <a name="cfn-licensemanager-license-entitlement-checkoutrules"></a>
The license entitlement checkout rules\.   
*Required*: No  
*Type*: [RuleList](aws-properties-licensemanager-license-rulelist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxCount`  <a name="cfn-licensemanager-license-entitlement-maxcount"></a>
Maximum entitlement count\. Use if the unit is not None\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-licensemanager-license-entitlement-name"></a>
Entitlement name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Overage`  <a name="cfn-licensemanager-license-entitlement-overage"></a>
Indicates whether overages are allowed\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Unit`  <a name="cfn-licensemanager-license-entitlement-unit"></a>
Entitlement unit\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-licensemanager-license-entitlement-value"></a>
Entitlement resource\. Use only if the unit is None\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)