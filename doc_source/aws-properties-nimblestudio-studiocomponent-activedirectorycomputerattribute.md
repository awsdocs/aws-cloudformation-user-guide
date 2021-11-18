# AWS::NimbleStudio::StudioComponent ActiveDirectoryComputerAttribute<a name="aws-properties-nimblestudio-studiocomponent-activedirectorycomputerattribute"></a>

An LDAP attribute of an Active Directory computer account, in the form of a name:value pair\.

## Syntax<a name="aws-properties-nimblestudio-studiocomponent-activedirectorycomputerattribute-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-nimblestudio-studiocomponent-activedirectorycomputerattribute-syntax.json"></a>

```
{
  "[Name](#cfn-nimblestudio-studiocomponent-activedirectorycomputerattribute-name)" : String,
  "[Value](#cfn-nimblestudio-studiocomponent-activedirectorycomputerattribute-value)" : String
}
```

### YAML<a name="aws-properties-nimblestudio-studiocomponent-activedirectorycomputerattribute-syntax.yaml"></a>

```
  [Name](#cfn-nimblestudio-studiocomponent-activedirectorycomputerattribute-name): String
  [Value](#cfn-nimblestudio-studiocomponent-activedirectorycomputerattribute-value): String
```

## Properties<a name="aws-properties-nimblestudio-studiocomponent-activedirectorycomputerattribute-properties"></a>

`Name`  <a name="cfn-nimblestudio-studiocomponent-activedirectorycomputerattribute-name"></a>
The name for the LDAP attribute\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-nimblestudio-studiocomponent-activedirectorycomputerattribute-value"></a>
The value for the LDAP attribute\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)