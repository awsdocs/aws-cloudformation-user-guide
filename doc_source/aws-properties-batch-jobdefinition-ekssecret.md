# AWS::Batch::JobDefinition EksSecret<a name="aws-properties-batch-jobdefinition-ekssecret"></a>

Specifies the configuration of a Kubernetes `secret` volume\. For more information, see [secret](https://kubernetes.io/docs/concepts/storage/volumes/#secret) in the *Kubernetes documentation*\.

## Syntax<a name="aws-properties-batch-jobdefinition-ekssecret-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-ekssecret-syntax.json"></a>

```
{
  "[Optional](#cfn-batch-jobdefinition-ekssecret-optional)" : Boolean,
  "[SecretName](#cfn-batch-jobdefinition-ekssecret-secretname)" : String
}
```

### YAML<a name="aws-properties-batch-jobdefinition-ekssecret-syntax.yaml"></a>

```
  [Optional](#cfn-batch-jobdefinition-ekssecret-optional): Boolean
  [SecretName](#cfn-batch-jobdefinition-ekssecret-secretname): String
```

## Properties<a name="aws-properties-batch-jobdefinition-ekssecret-properties"></a>

`Optional`  <a name="cfn-batch-jobdefinition-ekssecret-optional"></a>
Specifies whether the secret or the secret's keys must be defined\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretName`  <a name="cfn-batch-jobdefinition-ekssecret-secretname"></a>
The name of the secret\. The name must be allowed as a DNS subdomain name\. For more information, see [DNS subdomain names](https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#dns-subdomain-names) in the *Kubernetes documentation*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)