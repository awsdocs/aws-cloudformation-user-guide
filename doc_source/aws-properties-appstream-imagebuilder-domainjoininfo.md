# Amazon AppStream 2\.0 ImageBuilder DomainJoinInfo<a name="aws-properties-appstream-imagebuilder-domainjoininfo"></a>

<a name="aws-properties-appstream-imagebuilder-domainjoininfo-description"></a>The `DomainJoinInfo` property type specifies the name of the directory and organizational unit \(OU\) to use to join an Amazon AppStream 2\.0 image builder to a Microsoft Active Directory domain\.

<a name="aws-properties-appstream-imagebuilder-domainjoininfo-inheritance"></a> `DomainJoinInfo` is a property of the [AWS::AppStream::ImageBuilder](aws-resource-appstream-imagebuilder.md) resource\.

## Syntax<a name="aws-properties-appstream-imagebuilder-domainjoininfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appstream-imagebuilder-domainjoininfo-syntax.json"></a>

```
{
  "[DirectoryName](#cfn-appstream-imagebuilder-domainjoininfo-directoryname)" : String,
  "[OrganizationalUnitDistinguishedName](#cfn-appstream-imagebuilder-domainjoininfo-organizationalunitdistinguishedname)" : String
}
```

### YAML<a name="aws-properties-appstream-imagebuilder-domainjoininfo-syntax.yaml"></a>

```
[DirectoryName](#cfn-appstream-imagebuilder-domainjoininfo-directoryname): String
[OrganizationalUnitDistinguishedName](#cfn-appstream-imagebuilder-domainjoininfo-organizationalunitdistinguishedname): String
```

## Properties<a name="aws-properties-appstream-imagebuilder-domainjoininfo-properties"></a>

`DirectoryName`  <a name="cfn-appstream-imagebuilder-domainjoininfo-directoryname"></a>
The fully qualified name of the directory \(for example, corp\.example\.com\)\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`OrganizationalUnitDistinguishedName`  <a name="cfn-appstream-imagebuilder-domainjoininfo-organizationalunitdistinguishedname"></a>
The distinguished name of the organizational unit for computer accounts\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 