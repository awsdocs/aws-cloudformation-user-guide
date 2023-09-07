# AWS::PCAConnectorAD::Template KeyUsageProperty<a name="aws-properties-pcaconnectorad-template-keyusageproperty"></a>

The key usage property defines the purpose of the private key contained in the certificate\. You can specify specific purposes using property flags or all by using property type ALL\.

## Syntax<a name="aws-properties-pcaconnectorad-template-keyusageproperty-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pcaconnectorad-template-keyusageproperty-syntax.json"></a>

```
{
  "[PropertyFlags](#cfn-pcaconnectorad-template-keyusageproperty-propertyflags)" : KeyUsagePropertyFlags,
  "[PropertyType](#cfn-pcaconnectorad-template-keyusageproperty-propertytype)" : String
}
```

### YAML<a name="aws-properties-pcaconnectorad-template-keyusageproperty-syntax.yaml"></a>

```
  [PropertyFlags](#cfn-pcaconnectorad-template-keyusageproperty-propertyflags): 
    KeyUsagePropertyFlags
  [PropertyType](#cfn-pcaconnectorad-template-keyusageproperty-propertytype): String
```

## Properties<a name="aws-properties-pcaconnectorad-template-keyusageproperty-properties"></a>

`PropertyFlags`  <a name="cfn-pcaconnectorad-template-keyusageproperty-propertyflags"></a>
You can specify key usage for encryption, key agreement, and signature\. You can use property flags or property type but not both\.   
*Required*: No  
*Type*: [KeyUsagePropertyFlags](aws-properties-pcaconnectorad-template-keyusagepropertyflags.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PropertyType`  <a name="cfn-pcaconnectorad-template-keyusageproperty-propertytype"></a>
You can specify all key usages using property type ALL\. You can use property type or property flags but not both\.   
*Required*: No  
*Type*: String  
*Allowed values*: `ALL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)