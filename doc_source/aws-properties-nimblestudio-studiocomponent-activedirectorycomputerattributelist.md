# AWS::NimbleStudio::StudioComponent ActiveDirectoryComputerAttributeList<a name="aws-properties-nimblestudio-studiocomponent-activedirectorycomputerattributelist"></a>

A collection of LDAP attributes to apply to Active Directory computer accounts that are created for streaming sessions\.

## Syntax<a name="aws-properties-nimblestudio-studiocomponent-activedirectorycomputerattributelist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-nimblestudio-studiocomponent-activedirectorycomputerattributelist-syntax.json"></a>

```
{
  "[ActiveDirectoryComputerAttributeList](#cfn-nimblestudio-studiocomponent-activedirectorycomputerattributelist-activedirectorycomputerattributelist)" : [ ActiveDirectoryComputerAttribute, ... ]
}
```

### YAML<a name="aws-properties-nimblestudio-studiocomponent-activedirectorycomputerattributelist-syntax.yaml"></a>

```
  [ActiveDirectoryComputerAttributeList](#cfn-nimblestudio-studiocomponent-activedirectorycomputerattributelist-activedirectorycomputerattributelist): 
    - ActiveDirectoryComputerAttribute
```

## Properties<a name="aws-properties-nimblestudio-studiocomponent-activedirectorycomputerattributelist-properties"></a>

`ActiveDirectoryComputerAttributeList`  <a name="cfn-nimblestudio-studiocomponent-activedirectorycomputerattributelist-activedirectorycomputerattributelist"></a>
A collection of LDAP attributes to apply to Active Directory computer accounts that are created for streaming sessions\.  
*Required*: No  
*Type*: [List](#aws-properties-nimblestudio-studiocomponent-activedirectorycomputerattributelist) of [ActiveDirectoryComputerAttribute](aws-properties-nimblestudio-studiocomponent-activedirectorycomputerattribute.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)