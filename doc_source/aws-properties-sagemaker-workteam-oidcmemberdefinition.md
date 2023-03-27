# AWS::SageMaker::Workteam OidcMemberDefinition<a name="aws-properties-sagemaker-workteam-oidcmemberdefinition"></a>

A list of user groups that exist in your OIDC Identity Provider \(IdP\)\. One to ten groups can be used to create a single private work team\. When you add a user group to the list of `Groups`, you can add that user group to one or more private work teams\. If you add a user group to a private work team, all workers in that user group are added to the work team\.

## Syntax<a name="aws-properties-sagemaker-workteam-oidcmemberdefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-workteam-oidcmemberdefinition-syntax.json"></a>

```
{
  "[OidcGroups](#cfn-sagemaker-workteam-oidcmemberdefinition-oidcgroups)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-sagemaker-workteam-oidcmemberdefinition-syntax.yaml"></a>

```
  [OidcGroups](#cfn-sagemaker-workteam-oidcmemberdefinition-oidcgroups): 
    - String
```

## Properties<a name="aws-properties-sagemaker-workteam-oidcmemberdefinition-properties"></a>

`OidcGroups`  <a name="cfn-sagemaker-workteam-oidcmemberdefinition-oidcgroups"></a>
Property description not available\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)