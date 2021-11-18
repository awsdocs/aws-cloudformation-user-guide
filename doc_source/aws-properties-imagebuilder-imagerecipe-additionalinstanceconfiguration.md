# AWS::ImageBuilder::ImageRecipe AdditionalInstanceConfiguration<a name="aws-properties-imagebuilder-imagerecipe-additionalinstanceconfiguration"></a>

In addition to your infrastruction configuration, these settings provide an extra layer of control over your build instances\. For instances where Image Builder installs the Systems Manager agent, you can choose whether to keep it for the AMI that you create\. You can also specify commands to run on launch for all of your build instances\.

## Syntax<a name="aws-properties-imagebuilder-imagerecipe-additionalinstanceconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-imagebuilder-imagerecipe-additionalinstanceconfiguration-syntax.json"></a>

```
{
  "[SystemsManagerAgent](#cfn-imagebuilder-imagerecipe-additionalinstanceconfiguration-systemsmanageragent)" : SystemsManagerAgent,
  "[UserDataOverride](#cfn-imagebuilder-imagerecipe-additionalinstanceconfiguration-userdataoverride)" : String
}
```

### YAML<a name="aws-properties-imagebuilder-imagerecipe-additionalinstanceconfiguration-syntax.yaml"></a>

```
  [SystemsManagerAgent](#cfn-imagebuilder-imagerecipe-additionalinstanceconfiguration-systemsmanageragent): 
    SystemsManagerAgent
  [UserDataOverride](#cfn-imagebuilder-imagerecipe-additionalinstanceconfiguration-userdataoverride): String
```

## Properties<a name="aws-properties-imagebuilder-imagerecipe-additionalinstanceconfiguration-properties"></a>

`SystemsManagerAgent`  <a name="cfn-imagebuilder-imagerecipe-additionalinstanceconfiguration-systemsmanageragent"></a>
Contains settings for the Systems Manager agent on your build instance\.  
*Required*: No  
*Type*: [SystemsManagerAgent](aws-properties-imagebuilder-imagerecipe-systemsmanageragent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserDataOverride`  <a name="cfn-imagebuilder-imagerecipe-additionalinstanceconfiguration-userdataoverride"></a>
Use this property to provide commands or a command script to run when you launch your build instance\.  
The userDataOverride property replaces any commands that Image Builder might have added to ensure that Systems Manager is installed on your Linux build instance\. If you override the user data, make sure that you add commands to install Systems Manager, if it is not pre\-installed on your base image\.
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `21847`  
*Pattern*: `^(?:[A-Za-z0-9+/]{4})*(?:[A-Za-z0-9+/]{2}==|[A-Za-z0-9+/]{3}=)?$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)