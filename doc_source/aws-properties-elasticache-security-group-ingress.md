# AWS::ElastiCache::SecurityGroupIngress<a name="aws-properties-elasticache-security-group-ingress"></a>

The AWS::ElastiCache::SecurityGroupIngress type authorizes ingress to a cache security group from hosts in specified Amazon EC2 security groups\. For more information about ElastiCache security group ingress, go to [AuthorizeCacheSecurityGroupIngress](https://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_AuthorizeCacheSecurityGroupIngress.html) in the *Amazon ElastiCache API Reference Guide*\. 

**Note**  
Updates are not supported\.

## Syntax<a name="aws-properties-elasticache-security-group-ingress-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticache-security-group-ingress-syntax.json"></a>

```
{
  "Type" : "AWS::ElastiCache::SecurityGroupIngress",
  "Properties" : {
      "[CacheSecurityGroupName](#cfn-elasticache-securitygroupingress-cachesecuritygroupname)" : String,
      "[EC2SecurityGroupName](#cfn-elasticache-securitygroupingress-ec2securitygroupname)" : String,
      "[EC2SecurityGroupOwnerId](#cfn-elasticache-securitygroupingress-ec2securitygroupownerid)" : String
    }
}
```

### YAML<a name="aws-properties-elasticache-security-group-ingress-syntax.yaml"></a>

```
Type: AWS::ElastiCache::SecurityGroupIngress
Properties: 
  [CacheSecurityGroupName](#cfn-elasticache-securitygroupingress-cachesecuritygroupname): String
  [EC2SecurityGroupName](#cfn-elasticache-securitygroupingress-ec2securitygroupname): String
  [EC2SecurityGroupOwnerId](#cfn-elasticache-securitygroupingress-ec2securitygroupownerid): String
```

## Properties<a name="aws-properties-elasticache-security-group-ingress-properties"></a>

`CacheSecurityGroupName`  <a name="cfn-elasticache-securitygroupingress-cachesecuritygroupname"></a>
The name of the Cache Security Group to authorize\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EC2SecurityGroupName`  <a name="cfn-elasticache-securitygroupingress-ec2securitygroupname"></a>
Name of the EC2 Security Group to include in the authorization\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EC2SecurityGroupOwnerId`  <a name="cfn-elasticache-securitygroupingress-ec2securitygroupownerid"></a>
Specifies the AWS Account ID of the owner of the EC2 security group specified in the EC2SecurityGroupName property\. The AWS access key ID is not an acceptable value\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-properties-elasticache-security-group-ingress-return-values"></a>

### Ref<a name="aws-properties-elasticache-security-group-ingress-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.