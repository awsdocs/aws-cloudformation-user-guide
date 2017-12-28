# AWS::OpsWorks::ElasticLoadBalancerAttachment<a name="aws-resource-opsworks-elbattachment"></a>

Attaches an Elastic Load Balancing load balancer to an AWS OpsWorks layer that you specify\.


+ [Syntax](#aws-resource-opsworks-elbattachment-syntax)
+ [Properties](#w3ab2c21c10d844b9)
+ [Template Snippet](#w3ab2c21c10d844c11)
+ [See Also](#w3ab2c21c10d844c13)

## Syntax<a name="aws-resource-opsworks-elbattachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-opsworks-elbattachment-syntax.json"></a>

```
{
  "Type": "AWS::OpsWorks::ElasticLoadBalancerAttachment",
  "Properties": {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-elbattachment-elbname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-elbattachment-layerid)" : String
  }
}
```

### YAML<a name="aws-resource-opsworks-elbattachment-syntax.yaml"></a>

```
Type: "AWS::OpsWorks::ElasticLoadBalancerAttachment"
Properties: 
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-elbattachment-elbname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-elbattachment-layerid): String
```

## Properties<a name="w3ab2c21c10d844b9"></a>

`ElasticLoadBalancerName`  
Elastic Load Balancing load balancer name\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`LayerId`  
The AWS OpsWorks layer ID that the Elastic Load Balancing load balancer will be attached to\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

## Template Snippet<a name="w3ab2c21c10d844c11"></a>

The following snippet specifies a load balancer attachment to an AWS OpsWorks layer, both of which would be described elsewhere in the same template:

### JSON<a name="aws-resource-opsworks-elbattachment-example.json"></a>

```
"ELBAttachment" : {
  "Type" : "AWS::OpsWorks::ElasticLoadBalancerAttachment",
    "Properties" : {
      "ElasticLoadBalancerName" : { "Ref" : "ELB" },
      "LayerId" : { "Ref" : "Layer" }
    }
}
```

### YAML<a name="aws-resource-opsworks-elbattachment-example.yaml"></a>

```
ELBAttachment: 
  Type: "AWS::OpsWorks::ElasticLoadBalancerAttachment"
  Properties: 
    ElasticLoadBalancerName: 
      Ref: "ELB"
    LayerId: 
      Ref: "Layer"
```

## See Also<a name="w3ab2c21c10d844c13"></a>

+ [AWS::OpsWorks::Layer](aws-resource-opsworks-layer.md)