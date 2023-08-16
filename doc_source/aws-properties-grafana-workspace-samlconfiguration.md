# AWS::Grafana::Workspace SamlConfiguration<a name="aws-properties-grafana-workspace-samlconfiguration"></a>

A structure containing information about how this workspace works with SAML\. 

## Syntax<a name="aws-properties-grafana-workspace-samlconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-grafana-workspace-samlconfiguration-syntax.json"></a>

```
{
  "[AllowedOrganizations](#cfn-grafana-workspace-samlconfiguration-allowedorganizations)" : [ String, ... ],
  "[AssertionAttributes](#cfn-grafana-workspace-samlconfiguration-assertionattributes)" : AssertionAttributes,
  "[IdpMetadata](#cfn-grafana-workspace-samlconfiguration-idpmetadata)" : IdpMetadata,
  "[LoginValidityDuration](#cfn-grafana-workspace-samlconfiguration-loginvalidityduration)" : Double,
  "[RoleValues](#cfn-grafana-workspace-samlconfiguration-rolevalues)" : RoleValues
}
```

### YAML<a name="aws-properties-grafana-workspace-samlconfiguration-syntax.yaml"></a>

```
  [AllowedOrganizations](#cfn-grafana-workspace-samlconfiguration-allowedorganizations): 
    - String
  [AssertionAttributes](#cfn-grafana-workspace-samlconfiguration-assertionattributes): 
    AssertionAttributes
  [IdpMetadata](#cfn-grafana-workspace-samlconfiguration-idpmetadata): 
    IdpMetadata
  [LoginValidityDuration](#cfn-grafana-workspace-samlconfiguration-loginvalidityduration): Double
  [RoleValues](#cfn-grafana-workspace-samlconfiguration-rolevalues): 
    RoleValues
```

## Properties<a name="aws-properties-grafana-workspace-samlconfiguration-properties"></a>

`AllowedOrganizations`  <a name="cfn-grafana-workspace-samlconfiguration-allowedorganizations"></a>
Lists which organizations defined in the SAML assertion are allowed to use the Amazon Managed Grafana workspace\. If this is empty, all organizations in the assertion attribute have access\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AssertionAttributes`  <a name="cfn-grafana-workspace-samlconfiguration-assertionattributes"></a>
A structure that defines which attributes in the SAML assertion are to be used to define information about the users authenticated by that IdP to use the workspace\.  
*Required*: No  
*Type*: [AssertionAttributes](aws-properties-grafana-workspace-assertionattributes.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdpMetadata`  <a name="cfn-grafana-workspace-samlconfiguration-idpmetadata"></a>
A structure containing the identity provider \(IdP\) metadata used to integrate the identity provider with this workspace\.  
*Required*: Yes  
*Type*: [IdpMetadata](aws-properties-grafana-workspace-idpmetadata.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoginValidityDuration`  <a name="cfn-grafana-workspace-samlconfiguration-loginvalidityduration"></a>
How long a sign\-on session by a SAML user is valid, before the user has to sign on again\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleValues`  <a name="cfn-grafana-workspace-samlconfiguration-rolevalues"></a>
A structure containing arrays that map group names in the SAML assertion to the Grafana `Admin` and `Editor` roles in the workspace\.  
*Required*: No  
*Type*: [RoleValues](aws-properties-grafana-workspace-rolevalues.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)