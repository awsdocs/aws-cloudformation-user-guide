# AWS::Elasticsearch::Domain AdvancedSecurityOptionsInput<a name="aws-properties-elasticsearch-domain-advancedsecurityoptionsinput"></a>

Specifies options for fine\-grained access control\.

## Syntax<a name="aws-properties-elasticsearch-domain-advancedsecurityoptionsinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticsearch-domain-advancedsecurityoptionsinput-syntax.json"></a>

```
{
  "[Enabled](#cfn-elasticsearch-domain-advancedsecurityoptionsinput-enabled)" : Boolean,
  "[InternalUserDatabaseEnabled](#cfn-elasticsearch-domain-advancedsecurityoptionsinput-internaluserdatabaseenabled)" : Boolean,
  "[MasterUserOptions](#cfn-elasticsearch-domain-advancedsecurityoptionsinput-masteruseroptions)" : MasterUserOptions
}
```

### YAML<a name="aws-properties-elasticsearch-domain-advancedsecurityoptionsinput-syntax.yaml"></a>

```
  [Enabled](#cfn-elasticsearch-domain-advancedsecurityoptionsinput-enabled): Boolean
  [InternalUserDatabaseEnabled](#cfn-elasticsearch-domain-advancedsecurityoptionsinput-internaluserdatabaseenabled): Boolean
  [MasterUserOptions](#cfn-elasticsearch-domain-advancedsecurityoptionsinput-masteruseroptions): 
    MasterUserOptions
```

## Properties<a name="aws-properties-elasticsearch-domain-advancedsecurityoptionsinput-properties"></a>

`Enabled`  <a name="cfn-elasticsearch-domain-advancedsecurityoptionsinput-enabled"></a>
True to enable fine\-grained access control\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InternalUserDatabaseEnabled`  <a name="cfn-elasticsearch-domain-advancedsecurityoptionsinput-internaluserdatabaseenabled"></a>
True to enable the internal user database\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MasterUserOptions`  <a name="cfn-elasticsearch-domain-advancedsecurityoptionsinput-masteruseroptions"></a>
Specifies information about the master user\.  
*Required*: No  
*Type*: [MasterUserOptions](aws-properties-elasticsearch-domain-masteruseroptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)