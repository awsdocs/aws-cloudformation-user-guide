# AWS::EMR::SecurityConfiguration<a name="aws-resource-emr-securityconfiguration"></a>

Use a `SecurityConfiguration` resource to configure data encryption, Kerberos authentication \(available in Amazon EMR release version 5\.10\.0 and later\), and Amazon S3 authorization for EMRFS \(available in EMR 5\.10\.0 and later\)\. You can re\-use a security configuration for any number of clusters in your account\. For more information and example security configuration JSON objects, see [Create a Security Configuration](https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-create-security-configuration.html) in the *Amazon EMR Management Guide*\.

## Syntax<a name="aws-resource-emr-securityconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-emr-securityconfiguration-syntax.json"></a>

```
{
  "Type" : "AWS::EMR::SecurityConfiguration",
  "Properties" : {
      "[Name](#cfn-emr-securityconfiguration-name)" : String,
      "[SecurityConfiguration](#cfn-emr-securityconfiguration-securityconfiguration)" : Json
    }
}
```

### YAML<a name="aws-resource-emr-securityconfiguration-syntax.yaml"></a>

```
Type: AWS::EMR::SecurityConfiguration
Properties: 
  [Name](#cfn-emr-securityconfiguration-name): String
  [SecurityConfiguration](#cfn-emr-securityconfiguration-securityconfiguration): Json
```

## Properties<a name="aws-resource-emr-securityconfiguration-properties"></a>

`Name`  <a name="cfn-emr-securityconfiguration-name"></a>
The name of the security configuration\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `10280`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecurityConfiguration`  <a name="cfn-emr-securityconfiguration-securityconfiguration"></a>
The security configuration details in JSON format\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-emr-securityconfiguration-return-values"></a>

### Ref<a name="aws-resource-emr-securityconfiguration-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns returns the security configuration name, such as `mySecurityConfiguration`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.