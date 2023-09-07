# AWS::PCAConnectorAD::Template KeyUsage<a name="aws-properties-pcaconnectorad-template-keyusage"></a>

The key usage extension defines the purpose \(e\.g\., encipherment, signature\) of the key contained in the certificate\.

## Syntax<a name="aws-properties-pcaconnectorad-template-keyusage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pcaconnectorad-template-keyusage-syntax.json"></a>

```
{
  "[Critical](#cfn-pcaconnectorad-template-keyusage-critical)" : Boolean,
  "[UsageFlags](#cfn-pcaconnectorad-template-keyusage-usageflags)" : KeyUsageFlags
}
```

### YAML<a name="aws-properties-pcaconnectorad-template-keyusage-syntax.yaml"></a>

```
  [Critical](#cfn-pcaconnectorad-template-keyusage-critical): Boolean
  [UsageFlags](#cfn-pcaconnectorad-template-keyusage-usageflags): 
    KeyUsageFlags
```

## Properties<a name="aws-properties-pcaconnectorad-template-keyusage-properties"></a>

`Critical`  <a name="cfn-pcaconnectorad-template-keyusage-critical"></a>
Sets the key usage extension to critical\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UsageFlags`  <a name="cfn-pcaconnectorad-template-keyusage-usageflags"></a>
The key usage flags represent the purpose \(e\.g\., encipherment, signature\) of the key contained in the certificate\.  
*Required*: Yes  
*Type*: [KeyUsageFlags](aws-properties-pcaconnectorad-template-keyusageflags.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)