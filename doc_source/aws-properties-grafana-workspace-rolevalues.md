# AWS::Grafana::Workspace RoleValues<a name="aws-properties-grafana-workspace-rolevalues"></a>

This structure defines which groups defined in the SAML assertion attribute are to be mapped to the Grafana `Admin` and `Editor` roles in the workspace\. SAML authenticated users not part of `Admin` or `Editor` role groups have `Viewer` permission over the workspace\.

## Syntax<a name="aws-properties-grafana-workspace-rolevalues-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-grafana-workspace-rolevalues-syntax.json"></a>

```
{
  "[Admin](#cfn-grafana-workspace-rolevalues-admin)" : [ String, ... ],
  "[Editor](#cfn-grafana-workspace-rolevalues-editor)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-grafana-workspace-rolevalues-syntax.yaml"></a>

```
  [Admin](#cfn-grafana-workspace-rolevalues-admin): 
    - String
  [Editor](#cfn-grafana-workspace-rolevalues-editor): 
    - String
```

## Properties<a name="aws-properties-grafana-workspace-rolevalues-properties"></a>

`Admin`  <a name="cfn-grafana-workspace-rolevalues-admin"></a>
A list of groups from the SAML assertion attribute to grant the Grafana `Admin` role to\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Editor`  <a name="cfn-grafana-workspace-rolevalues-editor"></a>
A list of groups from the SAML assertion attribute to grant the Grafana `Editor` role to\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)