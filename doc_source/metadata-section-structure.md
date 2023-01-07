# Metadata<a name="metadata-section-structure"></a>

You can use the optional `Metadata` section to include arbitrary JSON or YAML objects that provide details about the template\. For example, you can include template implementation details about specific resources, as shown in the following snippet:

**Important**  
During a stack update, you cannot update the `Metadata` section by itself\. You can update it only when you include changes that add, modify, or delete resources\.

**Important**  
CloudFormation does not transform, modify, or redact any information you include in the `Metadata` section\. Because of this, we strongly recommend you do not use this section to store sensitive information, such as passwords or secrets\.

## JSON<a name="metadata-section-structure-example.json"></a>

```
"Metadata" : {
  "Instances" : {"Description" : "Information about the instances"},
  "Databases" : {"Description" : "Information about the databases"}
}
```

## YAML<a name="metadata-section-structure-example.yaml"></a>

```
Metadata:
  Instances:
    Description: "Information about the instances"
  Databases: 
    Description: "Information about the databases"
```

## Metadata keys<a name="metadata-section-structure-keys"></a>

Some AWS CloudFormation features retrieve settings or configuration information that you define in the `Metadata` section\. You define this information in the following AWS CloudFormation\-specific metadata keys:

`AWS::CloudFormation::Init`  
Defines configuration tasks for the cfn\-init helper script\. This script is useful for configuring and installing applications on EC2 instances\. For more information, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-init.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-init.html)\.

`AWS::CloudFormation::Interface`  
Defines the grouping and ordering of input parameters when they are displayed in the AWS CloudFormation console\. By default, the AWS CloudFormation console alphabetically sorts parameters by their logical ID\. For more information, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudformation-interface.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudformation-interface.html)\.

`AWS::CloudFormation::Designer`  
Describes how your resources are laid out in AWS CloudFormation Designer \(Designer\)\. Designer automatically adds this information when you use it to create and update templates\. For more information, see [What is AWS CloudFormation Designer?](working-with-templates-cfn-designer.md)\.