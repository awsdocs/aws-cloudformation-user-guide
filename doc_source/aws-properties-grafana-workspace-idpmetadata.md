# AWS::Grafana::Workspace IdpMetadata<a name="aws-properties-grafana-workspace-idpmetadata"></a>

A structure containing the identity provider \(IdP\) metadata used to integrate the identity provider with this workspace\. You can specify the metadata either by providing a URL to its location in the `url` parameter, or by specifying the full metadata in XML format in the `xml` parameter\. Specifying both will cause an error\.

## Syntax<a name="aws-properties-grafana-workspace-idpmetadata-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-grafana-workspace-idpmetadata-syntax.json"></a>

```
{
  "[Url](#cfn-grafana-workspace-idpmetadata-url)" : String,
  "[Xml](#cfn-grafana-workspace-idpmetadata-xml)" : String
}
```

### YAML<a name="aws-properties-grafana-workspace-idpmetadata-syntax.yaml"></a>

```
  [Url](#cfn-grafana-workspace-idpmetadata-url): String
  [Xml](#cfn-grafana-workspace-idpmetadata-xml): String
```

## Properties<a name="aws-properties-grafana-workspace-idpmetadata-properties"></a>

`Url`  <a name="cfn-grafana-workspace-idpmetadata-url"></a>
The URL of the location containing the IdP metadata\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Xml`  <a name="cfn-grafana-workspace-idpmetadata-xml"></a>
The full IdP metadata, in XML format\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)