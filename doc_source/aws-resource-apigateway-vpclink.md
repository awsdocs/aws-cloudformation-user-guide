# AWS::ApiGateway::VpcLink<a name="aws-resource-apigateway-vpclink"></a>

The `AWS::ApiGateway::VpcLink` resource specifies an API Gateway VPC link for a `AWS::ApiGateway::RestApi` to access resources in an Amazon Virtual Private Cloud \(VPC\)\. For more information, see [vpclink:create](http://docs.aws.amazon.com/apigateway/api-reference/link-relation/vpclink-create/) in the *Amazon API Gateway REST API Reference*

**Topics**
+ [Syntax](#aws-resource-apigateway-vpclink-syntax)
+ [Properties](#w3ab2c21c10c93b9)
+ [Return Value](#w3ab2c21c10c93c11)
+ [Example](#aws-resource-apigateway-vpclink-examples)
+ [See Also](#aws-resource-apigateway-vpclink-seealso)

## Syntax<a name="aws-resource-apigateway-vpclink-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-vpclink-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::VpcLink",
  "Properties" : {
    "[Description](#cfn-apigateway-vpclink-description)" : String,
    "[Name](#cfn-apigateway-vpclink-name)" : String,
    "[TargetArns](#cfn-apigateway-vpclink-targetarns)" : [ String, ... ]
  }
}
```

### YAML<a name="aws-resource-apigateway-vpclink-syntax.yaml"></a>

```
Type: "AWS::ApiGateway::VpcLink"
Properties:
  [Description](#cfn-apigateway-vpclink-description): String
  [Name](#cfn-apigateway-vpclink-name): String
  [TargetArns](#cfn-apigateway-vpclink-targetarns):
    - String
```

## Properties<a name="w3ab2c21c10c93b9"></a>

`Description`  <a name="cfn-apigateway-vpclink-description"></a>
The description of the VPC link\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Name`  <a name="cfn-apigateway-vpclink-name"></a>
The name used to label and identify the VPC link\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`TargetArns`  <a name="cfn-apigateway-vpclink-targetarns"></a>
The ARNs of network load balancers of the VPC targeted by the VPC link\. The network load balancers must be owned by the same AWS account of the API owner\.  
*Required*: Yes  
List of *Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Value<a name="w3ab2c21c10c93c11"></a>

### Ref<a name="w3ab2c21c10c93c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the ID of the `VpcLink`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="aws-resource-apigateway-vpclink-examples"></a>

### <a name="aws-resource-apigateway-vpclink-example"></a>

#### JSON<a name="aws-resource-apigateway-vpclink-example.json"></a>

```
{
    "Parameters": {
        "description": {
            "Type": "String"
        },
        "name": {
            "Type": "String"
        }
    },
    "Resources": {
        "MyVpcLink": {
            "Type": "AWS::ApiGateway::VpcLink",
            "Properties": {
                "Description": {
                    "Ref": "description"
                },
                "Name": {
                    "Ref": "name"
                },
                "TargetArns": [
                    {
                        "Ref": "MyLoadBalancer"
                    }
                ]
            }
        },
        "MyLoadBalancer": {
            "Type": "AWS::ElasticLoadBalancingV2::LoadBalancer",
            "Properties": {
                "Type": "network",
                "Subnets": [
                    {
                        "Ref": "MySubnet"
                    }
                ]
            }
        },
        "MySubnet": {
            "Type": "AWS::EC2::Subnet",
            "Properties": {
                "VpcId": {
                    "Ref": "MyVPC"
                },
                "CidrBlock": "10.0.0.0/24"
            }
        },
        "MyVPC": {
            "Type": "AWS::EC2::VPC",
            "Properties": {
                "CidrBlock": "10.0.0.0/16"
            }
        },
        "MyInternetGateway": {
            "Type": "AWS::EC2::InternetGateway"
        },
        "MyInternetGatewayAttachment": {
            "Type": "AWS::EC2::VPCGatewayAttachment",
            "Properties": {
                "VpcId": {
                    "Ref": "MyVPC"
                },
                "InternetGatewayId": {
                    "Ref": "MyInternetGateway"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-apigateway-vpclink-example.yaml"></a>

```
Parameters:
    description:
        Type: String
    name:
        Type: String
Resources:
    MyVpcLink:
        Type: AWS::ApiGateway::VpcLink
        Properties:
            Description: !Ref description
            Name: !Ref name
            TargetArns:
               - !Ref MyLoadBalancer
    MyLoadBalancer:
            Type: AWS::ElasticLoadBalancingV2::LoadBalancer
            Properties:
                Type: network
                Subnets:
                   - !Ref MySubnet
    MySubnet:
        Type: AWS::EC2::Subnet
        Properties:
            VpcId: !Ref MyVPC
            CidrBlock: 10.0.0.0/24
    MyVPC:
        Type: AWS::EC2::VPC
        Properties:
            CidrBlock: 10.0.0.0/16
    MyInternetGateway:
        Type: AWS::EC2::InternetGateway
    MyInternetGatewayAttachment:
        Type: AWS::EC2::VPCGatewayAttachment
        Properties:
            VpcId: !Ref MyVPC
            InternetGatewayId: !Ref MyInternetGateway
```

## See Also<a name="aws-resource-apigateway-vpclink-seealso"></a>
+  [vpclink:create](http://docs.aws.amazon.com/apigateway/api-reference/link-relation/vpclink-create/) in the *Amazon API Gateway REST API Reference* 