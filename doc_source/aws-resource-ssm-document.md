# AWS::SSM::Document<a name="aws-resource-ssm-document"></a>

The `AWS::SSM::Document` resource creates an SSM document in AWS Systems Manager that describes an instance configuration, which you can use to set up and run commands on your instances\.

**Topics**
+ [Syntax](#aws-resource-ssm-document-syntax)
+ [Properties](#w3ab2c21c10e1151b9)
+ [Return Value](#w3ab2c21c10e1151c11)
+ [Examples](#w3ab2c21c10e1151c13)

## Syntax<a name="aws-resource-ssm-document-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssm-document-syntax.json"></a>

```
{
  "Type" : "AWS::SSM::Document",
  "Properties" : {
    "[Content](#cfn-ssm-document-content)" : JSON object,
    "[DocumentType](#cfn-ssm-document-documenttype)" : String,
    "[Tags](#cfn-ssm-document-tags)" : [ Resource Tag, ... ]
  }
}
```

### YAML<a name="aws-resource-ssm-document-syntax.yaml"></a>

```
Type: "AWS::SSM::Document"
Properties: 
  [Content](#cfn-ssm-document-content): JSON object
  [DocumentType](#cfn-ssm-document-documenttype): String
  [Tags](#cfn-ssm-document-tags):
    - Resource Tag
```

## Properties<a name="w3ab2c21c10e1151b9"></a>

`Content`  <a name="cfn-ssm-document-content"></a>
A JSON object that describes an instance configuration\. For more information, see [Creating Systems Manager Documents](http://docs.aws.amazon.com/AWSEC2/latest/DeveloperGuide/create-ssm-doc.html) in the *AWS Systems Manager User Guide*\.  
The `Content` property is a non\-stringified property\. For more information about automation actions, see [Systems Manager Automation Document Reference](http://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-ami-actions.html) in the *AWS Systems Manager User Guide*\.
*Required*: Yes  
*Type*: JSON object  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`DocumentType`  <a name="cfn-ssm-document-documenttype"></a>
The type of document to create that relates to the purpose of your document, such as running commands, bootstrapping software, or automating tasks\. For valid values, see the [CreateDocument](http://docs.aws.amazon.com/systems-manager/latest/APIReference/API_CreateDocument.html) action in the *AWS Systems Manager API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Tags`  <a name="cfn-ssm-document-tags"></a>
AWS CloudFormation resource tags to apply to the document, which can help you identify and categorize these resources\.   
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="w3ab2c21c10e1151c11"></a>

### Ref<a name="w3ab2c21c10e1151c11b3"></a>

When you pass the logical ID of an `AWS::SSM::Document` resource to the intrinsic `Ref` function, the function returns the Systems Manager document name, such as `ssm-myinstanceconfig-ABCNPH3XCAO6`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="w3ab2c21c10e1151c13"></a>

### <a name="w3ab2c21c10e1151c13b3"></a>

The following Systems Manager document joins instances to a directory in AWS Directory Service\. The three runtime configuration parameters specify which directory the instance joins\. You specify these parameter values when you associate the document with an instance\.

#### JSON<a name="aws-resource-ssm-document-example.json"></a>

```
"document" : {
  "Type" : "AWS::SSM::Document",
  "Properties" : {
    "Content" : {
      "schemaVersion":"1.2",
      "description":"Join instances to an AWS Directory Service domain.",
      "parameters":{
        "directoryId":{
          "type":"String",
          "description":"(Required) The ID of the AWS Directory Service directory."
        },
        "directoryName":{
          "type":"String",
          "description":"(Required) The name of the directory; for example, test.example.com"
        },
        "dnsIpAddresses":{
          "type":"StringList",
          "default":[
          ],
          "description":"(Optional) The IP addresses of the DNS servers in the directory. Required when DHCP is not configured. Learn more at http://docs.aws.amazon.com/directoryservice/latest/simple-ad/join_get_dns_addresses.html",
          "allowedPattern":"((25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\\.){3}(25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)"
        }
      },
      "runtimeConfig":{
        "aws:domainJoin":{
          "properties":{
            "directoryId":"{{ directoryId }}",
            "directoryName":"{{ directoryName }}",
            "dnsIpAddresses":"{{ dnsIpAddresses }}"
          }
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-ssm-document-example.yaml"></a>

```
document: 
  Type: "AWS::SSM::Document"
  Properties: 
    Content: 
      schemaVersion: "1.2"
      description: "Join instances to an AWS Directory Service domain."
      parameters: 
        directoryId: 
          type: "String"
          description: "(Required) The ID of the AWS Directory Service directory."
        directoryName: 
          type: "String"
          description: "(Required) The name of the directory; for example, test.example.com"
        dnsIpAddresses: 
          type: "StringList"
          default: []
          description: "(Optional) The IP addresses of the DNS servers in the directory. Required when DHCP is not configured. Learn more at http://docs.aws.amazon.com/directoryservice/latest/simple-ad/join_get_dns_addresses.html"
          allowedPattern: "((25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\\.){3}(25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)"
      runtimeConfig: 
        aws:domainJoin: 
          properties: 
            directoryId: "{{ directoryId }}"
            directoryName: "{{ directoryName }}"
            dnsIpAddresses: "{{ dnsIpAddresses }}"
```

### <a name="w3ab2c21c10e1151c13b5"></a>

The following example shows how to associate the SSM document with an instance\. The `DocumentName` property specifies the SSM document and the `AssociationParameters` property specifies values for the runtime configuration parameters\.

#### JSON<a name="aws-resource-ssm-document-example2.json"></a>

```
"myEC2" : {
  "Type" : "AWS::EC2::Instance",
  "Properties" : {
    "ImageId" : {"Ref" : "myImageId"},
    "InstanceType" : "t2.micro",
    "SsmAssociations" : [ {
      "DocumentName" : {"Ref" : "document"},
      "AssociationParameters" : [
        { "Key" : "directoryId", "Value" : [ { "Ref" : "myDirectory" } ] },
        { "Key" : "directoryName", "Value" : ["testDirectory.example.com"] },
        { "Key" : "dnsIpAddresses", "Value" : { "Fn::GetAtt" : ["myDirectory", "DnsIpAddresses"] } }
      ]
    } ],
    "IamInstanceProfile" : {"Ref" : "myInstanceProfile"},
    "NetworkInterfaces" : [ {
      "DeviceIndex" : "0",
      "AssociatePublicIpAddress" : "true",
      "SubnetId" : {"Ref" : "mySubnet"}
    } ],
    "KeyName" : {"Ref" : "myKeyName"}
  }
}
```

#### YAML<a name="aws-resource-ssm-document-example2.yaml"></a>

```
myEC2: 
  Type: "AWS::EC2::Instance"
  Properties: 
    ImageId: 
      Ref: "myImageId"
    InstanceType: "t2.micro"
    SsmAssociations: 
      - 
        DocumentName: 
          Ref: "document"
        AssociationParameters: 
          - 
            Key: "directoryId"
            Value: 
              - 
                Ref: "myDirectory"
          - 
            Key: "directoryName"
            Value: 
              - "testDirectory.example.com"
          - 
            Key: "dnsIpAddresses"
            Value: 
              Fn::GetAtt: 
                - "myDirectory"
                - "DnsIpAddresses"
    IamInstanceProfile: 
      Ref: "myInstanceProfile"
    NetworkInterfaces: 
      - 
        DeviceIndex: "0"
        AssociatePublicIpAddress: "true"
        SubnetId: 
          Ref: "mySubnet"
    KeyName: 
      Ref: "myKeyName"
```