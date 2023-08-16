# AWS::ApiGateway::ClientCertificate<a name="aws-resource-apigateway-clientcertificate"></a>

The `AWS::ApiGateway::ClientCertificate` resource creates a client certificate that API Gateway uses to configure client\-side SSL authentication for sending requests to the integration endpoint\.

## Syntax<a name="aws-resource-apigateway-clientcertificate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-clientcertificate-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::ClientCertificate",
  "Properties" : {
      "[Description](#cfn-apigateway-clientcertificate-description)" : String,
      "[Tags](#cfn-apigateway-clientcertificate-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-apigateway-clientcertificate-syntax.yaml"></a>

```
Type: AWS::ApiGateway::ClientCertificate
Properties: 
  [Description](#cfn-apigateway-clientcertificate-description): String
  [Tags](#cfn-apigateway-clientcertificate-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-apigateway-clientcertificate-properties"></a>

`Description`  <a name="cfn-apigateway-clientcertificate-description"></a>
The description of the client certificate\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-apigateway-clientcertificate-tags"></a>
The collection of tags\. Each tag element is associated with a given resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-apigateway-clientcertificate-return-values"></a>

### Ref<a name="aws-resource-apigateway-clientcertificate-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the client certificate name, such as `abc123`\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-apigateway-clientcertificate-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-apigateway-clientcertificate-return-values-fn--getatt-fn--getatt"></a>

`ClientCertificateId`  <a name="ClientCertificateId-fn::getatt"></a>
The ID for the client certificate\. For example: `abc123`\.

## Examples<a name="aws-resource-apigateway-clientcertificate--examples"></a>



### Create client certificate<a name="aws-resource-apigateway-clientcertificate--examples--Create_client_certificate"></a>

The following example creates a client certificate that you can use with an API Gateway deployment and stage\.

#### JSON<a name="aws-resource-apigateway-clientcertificate--examples--Create_client_certificate--json"></a>

```
{
    "TestClientCertificate": {
        "Type": "AWS::ApiGateway::ClientCertificate",
        "Properties": {
            "Description": "A test client certificate"
        }
    }
}
```

#### YAML<a name="aws-resource-apigateway-clientcertificate--examples--Create_client_certificate--yaml"></a>

```
TestClientCertificate:
  Type: 'AWS::ApiGateway::ClientCertificate'
  Properties:
    Description: A test client certificate
```

## See also<a name="aws-resource-apigateway-clientcertificate--seealso"></a>
+ [clientcertificate:generate](https://docs.aws.amazon.com/apigateway/latest/api/API_GenerateClientCertificate.html) in the *Amazon API Gateway REST API Reference*

