# AWS::NimbleStudio::StudioComponent ActiveDirectoryConfiguration<a name="aws-properties-nimblestudio-studiocomponent-activedirectoryconfiguration"></a>

The configuration for a AWS Directory Service for Microsoft Active Directory studio resource\.

## Syntax<a name="aws-properties-nimblestudio-studiocomponent-activedirectoryconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-nimblestudio-studiocomponent-activedirectoryconfiguration-syntax.json"></a>

```
{
  "[ComputerAttributes](#cfn-nimblestudio-studiocomponent-activedirectoryconfiguration-computerattributes)" : [ ActiveDirectoryComputerAttribute, ... ],
  "[DirectoryId](#cfn-nimblestudio-studiocomponent-activedirectoryconfiguration-directoryid)" : String,
  "[OrganizationalUnitDistinguishedName](#cfn-nimblestudio-studiocomponent-activedirectoryconfiguration-organizationalunitdistinguishedname)" : String
}
```

### YAML<a name="aws-properties-nimblestudio-studiocomponent-activedirectoryconfiguration-syntax.yaml"></a>

```
  [ComputerAttributes](#cfn-nimblestudio-studiocomponent-activedirectoryconfiguration-computerattributes): 
    - ActiveDirectoryComputerAttribute
  [DirectoryId](#cfn-nimblestudio-studiocomponent-activedirectoryconfiguration-directoryid): String
  [OrganizationalUnitDistinguishedName](#cfn-nimblestudio-studiocomponent-activedirectoryconfiguration-organizationalunitdistinguishedname): String
```

## Properties<a name="aws-properties-nimblestudio-studiocomponent-activedirectoryconfiguration-properties"></a>

`ComputerAttributes`  <a name="cfn-nimblestudio-studiocomponent-activedirectoryconfiguration-computerattributes"></a>
A collection of custom attributes for an Active Directory computer\.  
*Required*: No  
*Type*: List of [ActiveDirectoryComputerAttribute](aws-properties-nimblestudio-studiocomponent-activedirectorycomputerattribute.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DirectoryId`  <a name="cfn-nimblestudio-studiocomponent-activedirectoryconfiguration-directoryid"></a>
The directory ID of the AWS Directory Service for Microsoft Active Directory to access using this studio component\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OrganizationalUnitDistinguishedName`  <a name="cfn-nimblestudio-studiocomponent-activedirectoryconfiguration-organizationalunitdistinguishedname"></a>
The distinguished name \(DN\) and organizational unit \(OU\) of an Active Directory computer\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)