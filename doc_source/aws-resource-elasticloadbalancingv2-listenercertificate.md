# AWS::ElasticLoadBalancingV2::ListenerCertificate<a name="aws-resource-elasticloadbalancingv2-listenercertificate"></a>

The `AWS::ElasticLoadBalancingV2::ListenerCertificate` resource adds certificates to an HTTPS listener\. For more information, see [SSL Certificates](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/create-https-listener.html#https-listener-certificates) in the *User Guide for Application Load Balancers*\.

## Syntax<a name="aws-resource-elasticloadbalancingv2-listenercertificate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticloadbalancingv2-listenercertificate-syntax.json"></a>

```
{
  "Type" : "AWS::ElasticLoadBalancingV2::ListenerCertificate",
  "Properties" : {
    "[Certificates](#cfn-elasticloadbalancingv2-listenercertificate-certificates)" : [ [*Certificate*](aws-properties-elasticloadbalancingv2-listenercertificate-certificate.md), ... ]
    "[ListenerArn](#cfn-elasticloadbalancingv2-listenercertificate-listenerarn)" : String
  }
}
```

### YAML<a name="aws-resource-elasticloadbalancingv2-listenercertificate-syntax.yaml"></a>

```
Type: AWS::ElasticLoadBalancingV2::ListenerCertificate
Properties:
  [Certificates](#cfn-elasticloadbalancingv2-listenercertificate-certificates): 
    - [*Certificate*](aws-properties-elasticloadbalancingv2-listenercertificate-certificate.md)
  [ListenerArn](#cfn-elasticloadbalancingv2-listenercertificate-listenerarn): String
```

## Properties<a name="aws-resource-elasticloadbalancingv2-listenercertificate-properties"></a>

`Certificates`  <a name="cfn-elasticloadbalancingv2-listenercertificate-certificates"></a>
The certificates to add\. Duplicates not allowed\.  
 *Required*: Yes  
 *Type*: List of [Certificate](aws-properties-elasticloadbalancingv2-listenercertificate-certificate.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ListenerArn`  <a name="cfn-elasticloadbalancingv2-listenercertificate-listenerarn"></a>
The Amazon Resource Name \(ARN\) of the listener\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Example<a name="aws-resource-elasticloadbalancingv2-listenercertificate-examples"></a>

### <a name="aws-resource-elasticloadbalancingv2-listenercertificate-example1"></a>

The following example specifies a listener certificate, containing a single certificate, for a load balancer listener\.

#### JSON<a name="aws-resource-elasticloadbalancingv2-listenercertificate-example1.json"></a>

```
{
    "Parameters": {
        "CertificateArn1": {
            "Type": "String"
        },
        "CertificateArn2": {
            "Type": "String"
        },
        "LoadBalancerArn": {
            "Type": "String"
        },
        "TargetGroupArn": {
            "Type": "String"
        }
    },
    "Resources": {
        "ListenerCertificate": {
            "Type": "AWS::ElasticLoadBalancingV2::ListenerCertificate",
            "Properties": {
                "Certificates": [
                    {
                        "CertificateArn": {
                            "Ref": "CertificateArn1"
                        }
                    }
                ],
                "ListenerArn": {
                    "Ref": "Listener"
                }
            }
        },
        "Listener": {
            "Type": "AWS::ElasticLoadBalancingV2::Listener",
            "Properties": {
                "DefaultActions": [
                    {
                        "Type": "forward",
                        "TargetGroupArn": {
                            "Ref": "TargetGroupArn"
                        }
                    }
                ],
                "LoadBalancerArn": {
                    "Ref": "LoadBalancerArn"
                },
                "Port": "8000",
                "Protocol": "HTTPS",
                "Certificates": [
                    {
                        "CertificateArn": {
                            "Ref": "CertificateArn2"
                        }
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-elasticloadbalancingv2-listenercertificate-example1.yaml"></a>

```
Parameters:
  CertificateArn1:
    Type: String
  CertificateArn2:
    Type: String
  LoadBalancerArn:
    Type: String
  TargetGroupArn:
    Type: String
Resources:
  ListenerCertificate:
    Type: AWS::ElasticLoadBalancingV2::ListenerCertificate
    Properties:
      Certificates:
        - CertificateArn: !Ref CertificateArn1
      ListenerArn: !Ref Listener
  Listener:
    Type: AWS::ElasticLoadBalancingV2::Listener
    Properties:
      DefaultActions:
        - Type: forward
          TargetGroupArn: !Ref TargetGroupArn
      LoadBalancerArn: !Ref LoadBalancerArn
      Port: '8000'
      Protocol: HTTPS
      Certificates:
        - CertificateArn: !Ref CertificateArn2
```