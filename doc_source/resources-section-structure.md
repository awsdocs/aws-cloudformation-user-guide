# Resources<a name="resources-section-structure"></a>

The required `Resources` section declares the AWS resources that you want to include in the stack, such as an Amazon EC2 instance or an Amazon S3 bucket\.

## Syntax<a name="resources-section-structure-syntax"></a>

The `Resources` section consists of the key name `Resources`\. The following pseudo template outlines the `Resources` section:

### JSON<a name="resources-section-structure-syntax.json"></a>

```
"Resources" : {
    "Logical ID" : {
        "Type" : "Resource type",
        "Properties" : {
            Set of properties
        }
    }
}
```

### YAML<a name="resources-section-structure-syntax.yaml"></a>

```
Resources:
  Logical ID:
    Type: Resource type
    Properties:
      Set of properties
```

### Resource fields<a name="resources-section-structure-resource-fields"></a>

**Logical ID**  <a name="resources-section-structure-logicalid"></a>
The logical ID must be alphanumeric \(A\-Za\-z0\-9\) and unique within the template\. Use the logical name to reference the resource in other parts of the template\. For example, if you want to map an Amazon Elastic Block Store volume to an Amazon EC2 instance, you reference the logical IDs to associate the block stores with the instance\.  
In addition to the logical ID, certain resources also have a physical ID, which is the actual assigned name for that resource, such as an EC2 instance ID or an S3 bucket name\. Use the physical IDs to identify resources outside of AWS CloudFormation templates, but only after the resources have been created\. For example, suppose you give an EC2 instance resource a logical ID of `MyEC2Instance`\. When AWS CloudFormation creates the instance, AWS CloudFormation automatically generates and assigns a physical ID \(such as `i-28f9ba55`\) to the instance\. You can use this physical ID to identify the instance and view its properties \(such as the DNS name\) by using the Amazon EC2 console\. For resources that support custom names, you can assign your own names \(physical IDs\) to help you quickly identify resources\. For example, you can name an S3 bucket that stores logs as `MyPerformanceLogs`\. For more information, see [Name type](aws-properties-name.md)\.

**Resource type**  
The resource type identifies the type of resource that you are declaring\. For example, `AWS::EC2::Instance` declares an EC2 instance\. For a list of all resource types, see [AWS resource and property types reference](aws-template-resource-type-ref.md)\.

**Resource properties**  
Resource properties are additional options that you can specify for a resource\. For example, for each EC2 instance, you must specify an Amazon Machine Image \(AMI\) ID for that instance\. You declare the AMI ID as a property of the instance, as shown in the following example:  

**Example JSON**  

```
"Resources" : {
  "MyEC2Instance" : {
    "Type" : "AWS::EC2::Instance",
    "Properties" : {
      "ImageId" : "ami-0ff8a91507f77f867"
    }
  }
}
```

**Example YAML**  

```
Resources:
  MyEC2Instance:
    Type: "AWS::EC2::Instance"
    Properties:
      ImageId: "ami-0ff8a91507f77f867"
```
If a resource doesn't require that properties be declared, omit the properties section of that resource\.  
Property values can be literal strings, lists of strings, Booleans, parameter references, pseudo references, or the value returned by a function\. The following example shows you how to declare different property value types:  

**Example JSON**  

```
"Properties" : {
    "String" : "one-string-value",
    "Number" : 123,
    "LiteralList" : [ "first-value", "second-value" ],
    "Boolean" : true,
    "ReferenceForOneValue" :  { "Ref" : "MyLogicalResourceName" } ,
    "FunctionResultWithFunctionParams" : {
        "Fn::Join" : [ "%", [ "Key=", { "Ref" : "MyParameter" } ] ] }
}
```

**Example YAML**  

```
Properties:
  String: OneStringValue
  String: A longer string value 
  Number: 123
  LiteralList:
    - "[first]-string-value with a special characters"
    - "[second]-string-value with a special characters"
  Boolean: true
  ReferenceForOneValue:
    Ref: MyLogicalResourceName
  ReferenceForOneValueShortCut: !Ref MyLogicalResourceName
  FunctionResultWithFunctionParams: !Sub |
    Key=%${MyParameter}
```

You can conditionally create a resource by associating a condition with it\. You must define the condition in the `Conditions` section of the template\.

## Examples<a name="resources-section-structure-examples"></a>

The following example shows a resource declaration\. It defines two resources\. The `MyInstance` resource includes the `MyQueue` resource as part of its `UserData` property:

### JSON<a name="resources-section-structure-example.json"></a>

```
  "Resources" : {
    "MyInstance" : {
        "Type" : "AWS::EC2::Instance",
        "Properties" : {
            "UserData" : {
                "Fn::Base64" : {
                    "Fn::Join" : [ "", [ "Queue=", { "Ref" : "MyQueue" } ] ]
                 } },
            "AvailabilityZone" : "us-east-1a",
            "ImageId" : "ami-0ff8a91507f77f867"
        }
    },

    "MyQueue" : {
        "Type" : "AWS::SQS::Queue",
        "Properties" : {
        }
    }
}
```

### YAML<a name="resources-section-structure-example.yaml"></a>

```
Resources: 
  MyInstance: 
    Type: "AWS::EC2::Instance"
    Properties: 
      UserData: 
        "Fn::Base64":
          !Sub |
            Queue=${MyQueue}
      AvailabilityZone: "us-east-1a"
      ImageId: "ami-0ff8a91507f77f867"
  MyQueue: 
    Type: "AWS::SQS::Queue"
    Properties: {}
```