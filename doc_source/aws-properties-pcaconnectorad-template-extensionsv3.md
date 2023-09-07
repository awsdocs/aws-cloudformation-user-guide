# AWS::PCAConnectorAD::Template ExtensionsV3<a name="aws-properties-pcaconnectorad-template-extensionsv3"></a>

Certificate extensions for v3 template schema

## Syntax<a name="aws-properties-pcaconnectorad-template-extensionsv3-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pcaconnectorad-template-extensionsv3-syntax.json"></a>

```
{
  "[ApplicationPolicies](#cfn-pcaconnectorad-template-extensionsv3-applicationpolicies)" : ApplicationPolicies,
  "[KeyUsage](#cfn-pcaconnectorad-template-extensionsv3-keyusage)" : KeyUsage
}
```

### YAML<a name="aws-properties-pcaconnectorad-template-extensionsv3-syntax.yaml"></a>

```
  [ApplicationPolicies](#cfn-pcaconnectorad-template-extensionsv3-applicationpolicies): 
    ApplicationPolicies
  [KeyUsage](#cfn-pcaconnectorad-template-extensionsv3-keyusage): 
    KeyUsage
```

## Properties<a name="aws-properties-pcaconnectorad-template-extensionsv3-properties"></a>

`ApplicationPolicies`  <a name="cfn-pcaconnectorad-template-extensionsv3-applicationpolicies"></a>
Application policies specify what the certificate is used for and its purpose\.  
*Required*: No  
*Type*: [ApplicationPolicies](aws-properties-pcaconnectorad-template-applicationpolicies.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeyUsage`  <a name="cfn-pcaconnectorad-template-extensionsv3-keyusage"></a>
The key usage extension defines the purpose \(e\.g\., encipherment, signature, certificate signing\) of the key contained in the certificate\.  
*Required*: Yes  
*Type*: [KeyUsage](aws-properties-pcaconnectorad-template-keyusage.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)