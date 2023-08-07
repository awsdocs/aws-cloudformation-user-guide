# AWS::WAFv2::WebACL RequestInspectionACFP<a name="aws-properties-wafv2-webacl-requestinspectionacfp"></a>

Not currently supported by AWS CloudFormation\.

## Syntax<a name="aws-properties-wafv2-webacl-requestinspectionacfp-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-requestinspectionacfp-syntax.json"></a>

```
{
  "[AddressFields](#cfn-wafv2-webacl-requestinspectionacfp-addressfields)" : [ FieldIdentifier, ... ],
  "[EmailField](#cfn-wafv2-webacl-requestinspectionacfp-emailfield)" : FieldIdentifier,
  "[PasswordField](#cfn-wafv2-webacl-requestinspectionacfp-passwordfield)" : FieldIdentifier,
  "[PayloadType](#cfn-wafv2-webacl-requestinspectionacfp-payloadtype)" : String,
  "[PhoneNumberFields](#cfn-wafv2-webacl-requestinspectionacfp-phonenumberfields)" : [ FieldIdentifier, ... ],
  "[UsernameField](#cfn-wafv2-webacl-requestinspectionacfp-usernamefield)" : FieldIdentifier
}
```

### YAML<a name="aws-properties-wafv2-webacl-requestinspectionacfp-syntax.yaml"></a>

```
  [AddressFields](#cfn-wafv2-webacl-requestinspectionacfp-addressfields): 
    - FieldIdentifier
  [EmailField](#cfn-wafv2-webacl-requestinspectionacfp-emailfield): 
    FieldIdentifier
  [PasswordField](#cfn-wafv2-webacl-requestinspectionacfp-passwordfield): 
    FieldIdentifier
  [PayloadType](#cfn-wafv2-webacl-requestinspectionacfp-payloadtype): String
  [PhoneNumberFields](#cfn-wafv2-webacl-requestinspectionacfp-phonenumberfields): 
    - FieldIdentifier
  [UsernameField](#cfn-wafv2-webacl-requestinspectionacfp-usernamefield): 
    FieldIdentifier
```

## Properties<a name="aws-properties-wafv2-webacl-requestinspectionacfp-properties"></a>

`AddressFields`  <a name="cfn-wafv2-webacl-requestinspectionacfp-addressfields"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [FieldIdentifier](aws-properties-wafv2-webacl-fieldidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EmailField`  <a name="cfn-wafv2-webacl-requestinspectionacfp-emailfield"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [FieldIdentifier](aws-properties-wafv2-webacl-fieldidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PasswordField`  <a name="cfn-wafv2-webacl-requestinspectionacfp-passwordfield"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [FieldIdentifier](aws-properties-wafv2-webacl-fieldidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PayloadType`  <a name="cfn-wafv2-webacl-requestinspectionacfp-payloadtype"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `FORM_ENCODED | JSON`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PhoneNumberFields`  <a name="cfn-wafv2-webacl-requestinspectionacfp-phonenumberfields"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [FieldIdentifier](aws-properties-wafv2-webacl-fieldidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UsernameField`  <a name="cfn-wafv2-webacl-requestinspectionacfp-usernamefield"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [FieldIdentifier](aws-properties-wafv2-webacl-fieldidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)