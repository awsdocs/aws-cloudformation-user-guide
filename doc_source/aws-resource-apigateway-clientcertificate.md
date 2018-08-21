# AWS::ApiGateway::ClientCertificate<a name="aws-resource-apigateway-clientcertificate"></a>

The `AWS::ApiGateway::ClientCertificate` resource creates a client certificate that Amazon API Gateway \(API Gateway\) uses to configure client\-side SSL authentication for sending requests to the integration endpoint\.

**Topics**
+ [Syntax](#aws-resource-apigateway-clientcertificate-syntax)
+ [Properties](#w3ab2c21c10c31b9)
+ [Return Value](#w3ab2c21c10c31c11)
+ [Example](#w3ab2c21c10c31c13)

## Syntax<a name="aws-resource-apigateway-clientcertificate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-clientcertificate-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::ClientCertificate",
  "Properties" : {
    "[Description](#cfn-apigateway-clientcertificate-description)" : String
  }
}
```

### YAML<a name="aws-resource-apigateway-clientcertificate-syntax.yaml"></a>

```
Type: "AWS::ApiGateway::ClientCertificate"
Properties:
  [Description](#cfn-apigateway-clientcertificate-description): String
```

## Properties<a name="w3ab2c21c10c31b9"></a>

`Description`  <a name="cfn-apigateway-clientcertificate-description"></a>
A description of the client certificate\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="w3ab2c21c10c31c11"></a>

### Ref<a name="w3ab2c21c10c31c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the client certificate name, such as `abc123`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10c31c13"></a>

The following example creates a client certificate that you can use with an API Gateway deployment and stage\.

### JSON<a name="aws-resource-apigateway-clientcertificate-example.json"></a>

```
"TestClientCertificate": {
  "Type": "AWS::ApiGateway::ClientCertificate",
  "Properties": {
    "Description": "A test client certificate"
  }
}
```

### YAML<a name="aws-resource-apigateway-clientcertificate-example.yaml"></a>

```
TestClientCertificate: 
  Type: "AWS::ApiGateway::ClientCertificate"
  Properties: 
    Description: "A test client certificate"
```