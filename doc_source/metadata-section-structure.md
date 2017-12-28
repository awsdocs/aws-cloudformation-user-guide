# Metadata<a name="metadata-section-structure"></a>

You can use the optional `Metadata` section to include arbitrary JSON or YAML objects that provide details about the template\. For example, you can include template implementation details about specific resources, as shown in the following snippet:

**Important**  
During a stack update, you cannot update the `Metadata` section by itself\. You can update it only when you include changes that add, modify, or delete resources\.

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

## Metadata Keys<a name="w3ab2c17c15c15c11"></a>

Some AWS CloudFormation features retrieve settings or configuration information that you define from the `Metadata` section\. You define this information in the following AWS CloudFormation\-specific metadata keys:

`AWS::CloudFormation::Init`  
Defines configuration tasks for the cfn\-init helper script\. This script is useful for configuring and installing applications on EC2 instances\. For more information, see [AWS::CloudFormation::Init](aws-resource-init.md)\.

`AWS::CloudFormation::Interface`  
Defines the grouping and ordering of input parameters when they are displayed in the AWS CloudFormation console\. By default, the AWS CloudFormation console alphabetically sorts parameters by their logical ID\. For more information, see [AWS::CloudFormation::Interface](aws-resource-cloudformation-interface.md)\.

`AWS::CloudFormation::Designer`  
Describes how your resources are laid out in AWS CloudFormation Designer \(Designer\)\. Designer automatically adds this information when you use it create and update templates\. For more information, see [What Is AWS CloudFormation Designer?](working-with-templates-cfn-designer.md)\.