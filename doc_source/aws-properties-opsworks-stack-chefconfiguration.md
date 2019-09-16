# AWS::OpsWorks::Stack ChefConfiguration<a name="aws-properties-opsworks-stack-chefconfiguration"></a>

Describes the Chef configuration\.

## Syntax<a name="aws-properties-opsworks-stack-chefconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opsworks-stack-chefconfiguration-syntax.json"></a>

```
{
  "[BerkshelfVersion](#cfn-opsworks-chefconfiguration-berkshelfversion)" : String,
  "[ManageBerkshelf](#cfn-opsworks-chefconfiguration-berkshelfversion)" : Boolean
}
```

### YAML<a name="aws-properties-opsworks-stack-chefconfiguration-syntax.yaml"></a>

```
  [BerkshelfVersion](#cfn-opsworks-chefconfiguration-berkshelfversion): String
  [ManageBerkshelf](#cfn-opsworks-chefconfiguration-berkshelfversion): Boolean
```

## Properties<a name="aws-properties-opsworks-stack-chefconfiguration-properties"></a>

`BerkshelfVersion`  <a name="cfn-opsworks-chefconfiguration-berkshelfversion"></a>
The Berkshelf version\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManageBerkshelf`  <a name="cfn-opsworks-chefconfiguration-berkshelfversion"></a>
Whether to enable Berkshelf\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)