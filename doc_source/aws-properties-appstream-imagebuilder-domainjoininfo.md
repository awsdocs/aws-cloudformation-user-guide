# AWS::AppStream::ImageBuilder DomainJoinInfo<a name="aws-properties-appstream-imagebuilder-domainjoininfo"></a>

The name of the directory and organizational unit \(OU\) to use to join the image builder to a Microsoft Active Directory domain\.

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
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OrganizationalUnitDistinguishedName`  <a name="cfn-appstream-imagebuilder-domainjoininfo-organizationalunitdistinguishedname"></a>
The distinguished name of the organizational unit for computer accounts\.  
*Required*: No  
*Type*: String  
*Maximum*: `2000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)