# AWS::DirectoryService::MicrosoftAD<a name="aws-resource-directoryservice-microsoftad"></a>

The `AWS::DirectoryService::MicrosoftAD` resource creates a Microsoft Active Directory in AWS so that your directory users and groups can access the AWS Management Console and AWS applications using their existing credentials\. For more information, see [What Is AWS Directory Service?](http://docs.aws.amazon.com/directoryservice/latest/admin-guide/what_is.html) in the *AWS Directory Service Administration Guide*\.


+ [Syntax](#aws-resource-directoryservice-microsoftad-syntax)
+ [Properties](#w3ab2c21c10d303b9)
+ [Return Values](#w3ab2c21c10d303c11)
+ [Example](#w3ab2c21c10d303c13)

## Syntax<a name="aws-resource-directoryservice-microsoftad-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-directoryservice-microsoftad-syntax.json"></a>

```
{
  "Type" : "AWS::DirectoryService::MicrosoftAD",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-microsoftad-createalias)" : Boolean,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-microsoftad-enablesso)" : Boolean,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-microsoftad-name)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-microsoftad-password)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-microsoftad-shortname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-microsoftad-vpcsettings)" : VpcSettings
  }
}
```

### YAML<a name="aws-resource-directoryservice-microsoftad-syntax.yaml"></a>

```
Type: "AWS::DirectoryService::MicrosoftAD"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-microsoftad-createalias): Boolean
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-microsoftad-enablesso): Boolean
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-microsoftad-name): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-microsoftad-password): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-microsoftad-shortname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-directoryservice-microsoftad-vpcsettings):
    VpcSettings
```

## Properties<a name="w3ab2c21c10d303b9"></a>

`CreateAlias`  
A unique alias to assign to the Microsoft Active Directory in AWS\. AWS Directory Service uses the alias to construct the access URL for the directory, such as `http://alias.awsapps.com`\. By default, AWS CloudFormation does not create an alias\.  
*Required: *No  
*Type*: Boolean  
*Update requires*: Replacement

`EnableSso`  
Whether to enable single sign\-on for a Microsoft Active Directory in AWS\. Single sign\-on allows users in your directory to access certain AWS services from a computer joined to the directory without having to enter their credentials separately\. If you don't specify a value, AWS CloudFormation disables single sign\-on by default\.  
*Required: *No  
*Type*: Boolean  
*Update requires*: No interruption

`Name`  
The fully qualified name for the Microsoft Active Directory in AWS, such as `corp.example.com`\. The name doesn't need to be publicly resolvable; it will resolve inside your VPC only\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`Password`  
The password for the default administrative user, `Admin`\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`ShortName`  
The NetBIOS name for your domain, such as `CORP`\. If you don't specify a value, AWS Directory Service uses the first part of your directory DNS server name\. For example, if your directory DNS server name is `corp.example.com`, AWS Directory Service specifies `CORP` for the NetBIOS name\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`VpcSettings`  
Specifies the VPC settings of the Microsoft Active Directory server in AWS\.  
*Required: *Yes  
*Type*: [AWS Directory Service MicrosoftAD VpcSettings](aws-properties-directoryservice-microsoftad-vpcsettings.md)  
*Update requires*: Replacement

## Return Values<a name="w3ab2c21c10d303c11"></a>

### Ref<a name="w3ab2c21c10d303c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource ID\.

In the following sample, the `Ref` function returns the ID of the `myDirectory` directory, such as `d-12345ab592`\.

```
{ "Ref": "myDirectory" }
```

For more information about using the `Ref` function, see Ref\.

### Fn::GetAtt<a name="w3ab2c21c10d303c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Alias`  
The alias for a directory\. For example: `d-12373a053a` or `alias4-mydirectory-12345abcgmzsk` \(if you have the `CreateAlias` property set to true\)\.

`DnsIpAddresses`  
The IP addresses of the DNS servers for the directory, such as `[ "192.0.2.1", "192.0.2.2" ]`\.

For more information about using `Fn::GetAtt`, see Fn::GetAtt\.

## Example<a name="w3ab2c21c10d303c13"></a>

The following example creates a Microsoft Active Directory in AWS, where the directory DNS name is `corp.example.com`:

### JSON<a name="aws-resource-directoryservice-microsoftad-example.json"></a>

```
"myDirectory" : {
  "Type" : "AWS::DirectoryService::MicrosoftAD",
  "Properties" : {
    "Name" : "corp.example.com",
    "Password" : { "Ref" : "MicrosoftADPW" },
    "ShortName" : { "Ref" : "MicrosoftADShortName" },
    "VpcSettings" : { 
      "SubnetIds" : [ { "Ref" : "subnetID1" }, { "Ref" : "subnetID2" } ],
      "VpcId" : { "Ref" : "vpcID" }
    }
  }
}
```

### YAML<a name="aws-resource-directoryservice-microsoftad-example.yaml"></a>

```
myDirectory: 
  Type: "AWS::DirectoryService::MicrosoftAD"
  Properties: 
    Name: "corp.example.com"
    Password: 
      Ref: MicrosoftADPW
    ShortName: 
      Ref: MicrosoftADShortName
    VpcSettings: 
      SubnetIds: 
        - Ref: subnetID1
        - Ref: subnetID2
      VpcId: 
        Ref: vpcID
```