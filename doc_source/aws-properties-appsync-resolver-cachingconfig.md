# AWS::AppSync::Resolver CachingConfig<a name="aws-properties-appsync-resolver-cachingconfig"></a>

The caching configuration for a resolver that has caching activated\.

## Syntax<a name="aws-properties-appsync-resolver-cachingconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-resolver-cachingconfig-syntax.json"></a>

```
{
  "[CachingKeys](#cfn-appsync-resolver-cachingconfig-cachingkeys)" : [ String, ... ],
  "[Ttl](#cfn-appsync-resolver-cachingconfig-ttl)" : Double
}
```

### YAML<a name="aws-properties-appsync-resolver-cachingconfig-syntax.yaml"></a>

```
  [CachingKeys](#cfn-appsync-resolver-cachingconfig-cachingkeys): 
    - String
  [Ttl](#cfn-appsync-resolver-cachingconfig-ttl): Double
```

## Properties<a name="aws-properties-appsync-resolver-cachingconfig-properties"></a>

`CachingKeys`  <a name="cfn-appsync-resolver-cachingconfig-cachingkeys"></a>
The caching keys for a resolver that has caching activated\.  
Valid values are entries from the `$context.arguments`, `$context.source`, and `$context.identity` maps\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ttl`  <a name="cfn-appsync-resolver-cachingconfig-ttl"></a>
The TTL in seconds for a resolver that has caching activated\.  
Valid values are 1–3,600 seconds\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)