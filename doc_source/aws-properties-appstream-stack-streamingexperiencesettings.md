# AWS::AppStream::Stack StreamingExperienceSettings<a name="aws-properties-appstream-stack-streamingexperiencesettings"></a>

The streaming protocol that you want your stack to prefer\. This can be UDP or TCP\. Currently, UDP is only supported in the Windows native client\.

## Syntax<a name="aws-properties-appstream-stack-streamingexperiencesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appstream-stack-streamingexperiencesettings-syntax.json"></a>

```
{
  "[PreferredProtocol](#cfn-appstream-stack-streamingexperiencesettings-preferredprotocol)" : String
}
```

### YAML<a name="aws-properties-appstream-stack-streamingexperiencesettings-syntax.yaml"></a>

```
  [PreferredProtocol](#cfn-appstream-stack-streamingexperiencesettings-preferredprotocol): String
```

## Properties<a name="aws-properties-appstream-stack-streamingexperiencesettings-properties"></a>

`PreferredProtocol`  <a name="cfn-appstream-stack-streamingexperiencesettings-preferredprotocol"></a>
The preferred protocol that you want to use while streaming your application\.  
*Required*: No  
*Type*: String  
*Allowed values*: `TCP | UDP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)