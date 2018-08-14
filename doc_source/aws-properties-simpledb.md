# AWS::SDB::Domain<a name="aws-properties-simpledb"></a>

Use the `AWS::SDB::Domain` resource to declare an Amazon SimpleDB domain\. When you specify `AWS::SDB::Domain` as an argument in a `Ref` function, AWS CloudFormation returns the value of the `DomainName`\.

**Important**  
The `AWS::SDB::Domain` resource does not allow any updates, including metadata updates\.

## Syntax<a name="aws-resource-sdb-domain-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sdb-domain-syntax.json"></a>

```
{
  "Type" : "AWS::SDB::Domain",
  "Properties" : {
    "[Description](#cfn-sdb-domain-description)" : String
  }
}
```

### YAML<a name="aws-resource-sdb-domain-syntax.yaml"></a>

```
Type: "AWS::SDB::Domain"
Properties: 
  [Description](#cfn-sdb-domain-description): String
```

## Properties<a name="w3ab2c21c10e1060b9"></a>

`Description`  <a name="cfn-sdb-domain-description"></a>
Information about the Amazon SimpleDB domain\.  
*Required*: No  
*Type*: String  
*Update requires*: Updates are not supported\.