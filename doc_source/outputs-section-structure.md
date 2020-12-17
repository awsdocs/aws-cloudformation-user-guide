# Outputs<a name="outputs-section-structure"></a>

The optional `Outputs` section declares output values that you can [import into other stacks](intrinsic-function-reference-importvalue.md) \(to [create cross\-stack references](walkthrough-crossstackref.md)\), return in response \(to describe stack calls\), or [view on the AWS CloudFormation console](cfn-console-view-stack-data-resources.md)\. For example, you can output the S3 bucket name for a stack to make the bucket easier to find\.

**Important**  
CloudFormation does not redact or obfuscate any information you include in the Outputs section\. We strongly recommend you do not use this section to output sensitive information, such as passwords or secrets\.

## Syntax<a name="outputs-section-syntax"></a>

The `Outputs` section consists of the key name `Outputs`, followed by a space and a single colon\. You can declare a maximum of 200 outputs in a template\.

The following example demonstrates the structure of the `Outputs` section\.

### JSON<a name="outputs-section-structure-syntax.json"></a>

Use braces to enclose all output declarations\. Delimit multiple outputs with commas\. 

```
"Outputs" : {
  "Logical ID" : {
    "Description" : "Information about the value",
    "Value" : "Value to return",
    "Export" : {
      "Name" : "Value to export"
    }
  }
}
```

### YAML<a name="outputs-section-structure-syntax.yaml"></a>

```
Outputs:
  Logical ID:
    Description: Information about the value
    Value: Value to return
    Export:
      Name: Value to export
```

### Output fields<a name="outputs-section-structure-output-fields"></a>

The `Outputs` section can include the following fields\.

**Logical ID**  
An identifier for the current output\. The logical ID must be alphanumeric \(`a-z`, `A-Z`, `0-9`\) and unique within the template\.

**Description \(optional\)**  
A `String` type that describes the output value\. The value for the description declaration must be a literal string that is between 0 and 1024 bytes in length\. You cannot use a parameter or function to specify the description\. The description can be a maximum of 4 K in length\.

**Value \(required\)**  
The value of the property returned by the `aws cloudformation describe-stacks` command\. The value of an output can include literals, parameter references, pseudo\-parameters, a mapping value, or intrinsic functions\.

**Export \(optional\)**  
The name of the resource output to be exported for a [cross\-stack reference](walkthrough-crossstackref.md)\.  
The following restrictions apply to cross\-stack references:  
+ For each AWS account, `Export` names must be unique within a region\.
+ You can't create cross\-stack references across regions\. You can use the intrinsic function `Fn::ImportValue` to import only values that have been exported within the same region\.
+ For outputs, the value of the `Name` property of an `Export` can't use `Ref` or `GetAtt` functions that depend on a resource\.

  Similarly, the `ImportValue` function can't include `Ref` or `GetAtt` functions that depend on a resource\.
+ You can't delete a stack if another stack references one of its outputs\.
+ You can't modify or remove an output value that is referenced by another stack\.
You can use intrinsic functions to customize the `Name` value of an export\. The following examples use the `Fn::Join` function\.  
JSON  

```
"Export" : {
  "Name" : {
    "Fn::Join" : [ ":", [ { "Ref" : "AWS::StackName" }, "AccountVPC" ] ]
  }
}
```
YAML  

```
Export:
  Name: !Join [ ":", [ !Ref "AWS::StackName", AccountVPC ] ]
```

To associate a condition with an output, define the condition in the `Conditions` section of the template\.

## Examples<a name="outputs-section-structure-examples"></a>

The following examples illustrate how stack output works\.

### Stack output<a name="outputs-section-structure-examples-stack-output"></a>

In the following example, the output named `BackupLoadBalancerDNSName` returns the DNS name for the resource with the logical ID `BackupLoadBalancer` only when the `CreateProdResources` condition is true\. \(The second output shows how to specify multiple outputs\.\)

#### JSON<a name="outputs-section-structure-example.json"></a>

```
"Outputs" : {
  "BackupLoadBalancerDNSName" : {
    "Description": "The DNSName of the backup load balancer",  
    "Value" : { "Fn::GetAtt" : [ "BackupLoadBalancer", "DNSName" ]},
    "Condition" : "CreateProdResources"
  },
  "InstanceID" : {
    "Description": "The Instance ID",  
    "Value" : { "Ref" : "EC2Instance" }
  }
}
```

#### YAML<a name="outputs-section-structure-example.yaml"></a>

```
Outputs:
  BackupLoadBalancerDNSName:
    Description: The DNSName of the backup load balancer
    Value: !GetAtt BackupLoadBalancer.DNSName
    Condition: CreateProdResources
  InstanceID:
    Description: The Instance ID
    Value: !Ref EC2Instance
```

### Cross\-stack output<a name="outputs-section-structure-examples-cross-stack"></a>

In the following examples, the output named `StackVPC` returns the ID of a VPC, and then exports the value for cross\-stack referencing with the name `VPCID` appended to the stack's name\.

#### JSON<a name="outputs-section-structure-cross-stack-example.json"></a>

```
"Outputs" : {
  "StackVPC" : {
    "Description" : "The ID of the VPC",
    "Value" : { "Ref" : "MyVPC" },
    "Export" : {
      "Name" : {"Fn::Sub": "${AWS::StackName}-VPCID" }
    }
  }
}
```

#### YAML<a name="outputs-section-structure-cross-stack-example.yaml"></a>

```
Outputs:
  StackVPC:
    Description: The ID of the VPC
    Value: !Ref MyVPC
    Export:
      Name: !Sub "${AWS::StackName}-VPCID"
```