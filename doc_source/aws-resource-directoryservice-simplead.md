# AWS::DirectoryService::SimpleAD<a name="aws-resource-directoryservice-simplead"></a>

The `AWS::DirectoryService::SimpleAD` resource creates an AWS Directory Service Simple Active Directory \(Simple AD\) in AWS so that your directory users and groups can access the AWS Management Console and AWS applications using their existing credentials\. Simple AD is a Microsoft Active Directory–compatible directory\. For more information, see [What Is AWS Directory Service?](http://docs.aws.amazon.com/directoryservice/latest/admin-guide/what_is.html) in the *AWS Directory Service Administration Guide*\.


+ [Syntax](#aws-resource-directoryservice-simplead-syntax)
+ [Properties](#w3ab2c21c10d307b9)
+ [Return Values](#w3ab2c21c10d307c11)
+ [Example](#w3ab2c21c10d307c13)

## Syntax<a name="aws-resource-directoryservice-simplead-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-directoryservice-simplead-syntax.json"></a>

```
{
  "Type" : "AWS::DirectoryService::SimpleAD",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-simplead-createalias)" : Boolean,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-simplead-description)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-simplead-enablesso)" : Boolean,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-simplead-name)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-simplead-password)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-simplead-shortname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-simplead-size)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-simplead-vpcsettings)" : VpcSettings
  }
}
```

### YAML<a name="aws-resource-directoryservice-simplead-syntax.yaml"></a>

```
Type: "AWS::DirectoryService::SimpleAD"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-simplead-createalias): Boolean
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-simplead-description): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-simplead-enablesso): Boolean
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-simplead-name): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-simplead-password): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-simplead-shortname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-simplead-size): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-simplead-vpcsettings):
    VpcSettings
```

## Properties<a name="w3ab2c21c10d307b9"></a>

`CreateAlias`  
A unique alias to assign to the directory\. AWS Directory Service uses the alias to construct the access URL for the directory, such as `http://alias.awsapps.com`\. By default, AWS CloudFormation does not create an alias\.  
*Required: *No  
*Type*: Boolean  
*Update requires*: Replacement

`Description`  
A description of the directory\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`EnableSso`  
Whether to enable single sign\-on for a directory\. If you don't specify a value, AWS CloudFormation disables single sign\-on by default\.  
*Required: *No  
*Type*: Boolean  
*Update requires*: No interruption

`Name`  
The fully qualified name for the directory, such as `corp.example.com`\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`Password`  
The password for the directory administrator\. AWS Directory Service creates a directory administrator account with the user name `Administrator` and this password\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`ShortName`  
The NetBIOS name of the on\-premises directory, such as `CORP`\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`Size`  
The size of the directory\. For valid values, see [CreateDirectory](http://docs.aws.amazon.com/directoryservice/latest/devguide/API_CreateDirectory.html) in the *AWS Directory Service API Reference*\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`VpcSettings`  
Specifies the VPC settings of the directory server\.  
*Required: *Yes  
*Type*: [AWS Directory Service SimpleAD VpcSettings](aws-properties-directoryservice-simplead-vpcsettings.md)  
*Update requires*: Replacement

## Return Values<a name="w3ab2c21c10d307c11"></a>

### Ref<a name="w3ab2c21c10d307c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource ID\.

In the following sample, the `Ref` function returns the ID of the `myDirectory` directory, such as `d-1a2b3c4d5e`\.

```
{ "Ref": "myDirectory" }
```

For more information about using the `Ref` function, see Ref\.

### Fn::GetAtt<a name="w3ab2c21c10d307c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Alias`  
The alias for a directory\. For example: `d-12373a053a` or `alias4-mydirectory-12345abcgmzsk` \(if you have the `CreateAlias` property set to true\)\.

`DnsIpAddresses`  
The IP addresses of the DNS servers for the directory, such as `[ "172.31.3.154", "172.31.63.203" ]`\.

For more information about using `Fn::GetAtt`, see Fn::GetAtt\.

## Example<a name="w3ab2c21c10d307c13"></a>

The following example creates a Simple AD directory, where the directory DNS name is `corp.example.com`:

### JSON<a name="aws-resource-directoryservice-simplead-example.json"></a>

```
"myDirectory" : {
  "Type" : "AWS::DirectoryService::SimpleAD",
  "Properties" : {
    "Name" : "corp.example.com",
    "Password" : { "Ref" : "SimpleADPW" },
    "Size" : "Small",
    "VpcSettings" : { 
      "SubnetIds" : [ { "Ref" : "subnetID1" }, { "Ref" : "subnetID2" } ],
      "VpcId" : { "Ref" : "vpcID" }
    }
  }
}
```

### YAML<a name="aws-resource-directoryservice-simplead-example.yaml"></a>

```
myDirectory: 
  Type: "AWS::DirectoryService::SimpleAD"
  Properties: 
    Name: "corp.example.com"
    Password: 
      Ref: SimpleADPW
    Size: "Small"
    VpcSettings: 
      SubnetIds: 
        - Ref: subnetID1
        - Ref: subnetID2
      VpcId: 
        Ref: vpcID
```