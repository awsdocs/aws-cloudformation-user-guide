# AWS OpsWorks ChefConfiguration Type<a name="aws-properties-opsworks-stack-chefconfiguration"></a>

Describes the Chef configuration for the [AWS::OpsWorks::Stack](aws-resource-opsworks-stack.md) resource type\. For more information, see [ChefConfiguration](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_ChefConfiguration.html) in the *AWS OpsWorks Stacks API Reference*\.

## Syntax<a name="w3ab2c21c14e1351b5"></a>

### JSON<a name="aws-properties-opsworks-stack-chefconfiguration-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-chefconfiguration-berkshelfversion)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-chefconfiguration-manageberkshelf)" : Boolean
}
```

### YAML<a name="aws-properties-opsworks-stack-chefconfiguration-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-chefconfiguration-berkshelfversion): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-chefconfiguration-manageberkshelf): Boolean
```

## Properties<a name="w3ab2c21c14e1351b7"></a>

`BerkshelfVersion`  
The Berkshelf version\.  
*Required: *No  
*Type*: String

`ManageBerkshelf`  
Whether to enable Berkshelf\.  
*Required: *No  
*Type*: Boolean