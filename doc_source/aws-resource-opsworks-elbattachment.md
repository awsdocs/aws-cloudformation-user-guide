# AWS::OpsWorks::ElasticLoadBalancerAttachment<a name="aws-resource-opsworks-elbattachment"></a>

Attaches an Elastic Load Balancing load balancer to an AWS OpsWorks layer that you specify\.

## Syntax<a name="aws-resource-opsworks-elbattachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-opsworks-elbattachment-syntax.json"></a>

```
{
  "Type" : "AWS::OpsWorks::ElasticLoadBalancerAttachment",
  "Properties" : {
      "[ElasticLoadBalancerName](#cfn-opsworks-elbattachment-elbname)" : String,
      "[LayerId](#cfn-opsworks-elbattachment-layerid)" : String
    }
}
```

### YAML<a name="aws-resource-opsworks-elbattachment-syntax.yaml"></a>

```
Type: AWS::OpsWorks::ElasticLoadBalancerAttachment
Properties: 
  [ElasticLoadBalancerName](#cfn-opsworks-elbattachment-elbname): String
  [LayerId](#cfn-opsworks-elbattachment-layerid): String
```

## Properties<a name="aws-resource-opsworks-elbattachment-properties"></a>

`ElasticLoadBalancerName`  <a name="cfn-opsworks-elbattachment-elbname"></a>
The Elastic Load Balancing instance's name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LayerId`  <a name="cfn-opsworks-elbattachment-layerid"></a>
The AWS OpsWorks layer ID that the Elastic Load Balancing load balancer will be attached to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-resource-opsworks-elbattachment--examples"></a>

### Template Snippet<a name="aws-resource-opsworks-elbattachment--examples--Template_Snippet"></a>

The following snippet specifies a load balancer attachment to an AWS OpsWorks layer, both of which would be described elsewhere in the same template:

#### JSON<a name="aws-resource-opsworks-elbattachment--examples--Template_Snippet--json"></a>

```
"ELBAttachment" : {
  "Type" : "AWS::OpsWorks::ElasticLoadBalancerAttachment",
    "Properties" : {
      "ElasticLoadBalancerName" : { "Ref" : "ELB" },
      "LayerId" : { "Ref" : "Layer" }
    }
}
```

#### YAML<a name="aws-resource-opsworks-elbattachment--examples--Template_Snippet--yaml"></a>

```
ELBAttachment: 
  Type: "AWS::OpsWorks::ElasticLoadBalancerAttachment"
  Properties: 
    ElasticLoadBalancerName: 
      Ref: "ELB"
    LayerId: 
      Ref: "Layer"
```

## See also<a name="aws-resource-opsworks-elbattachment--seealso"></a>
+  [AttachElasticLoadBalancer](https://docs.aws.amazon.com/opsworks/latest/APIReference/API_AttachElasticLoadBalancer.html) in the *AWS OpsWorks API Reference*\.
+  [Elastic Load Balancing Layer](https://docs.aws.amazon.com/opsworks/latest/userguide/layers-elb.html) in the *AWS OpsWorks User Guide*\.

