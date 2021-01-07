# AWS::DirectoryService::MicrosoftAD<a name="aws-resource-directoryservice-microsoftad"></a>

The `AWS::DirectoryService::MicrosoftAD` resource specifies a Microsoft Active Directory in AWS so that your directory users and groups can access the AWS Management Console and AWS applications using their existing credentials\. For more information, see [AWS Managed Microsoft AD](https://docs.aws.amazon.com/directoryservice/latest/admin-guide/directory_microsoft_ad.html) in the *AWS Directory Service Admin Guide*\.

## Syntax<a name="aws-resource-directoryservice-microsoftad-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-directoryservice-microsoftad-syntax.json"></a>

```
{
  "Type" : "AWS::DirectoryService::MicrosoftAD",
  "Properties" : {
      "[CreateAlias](#cfn-directoryservice-microsoftad-createalias)" : Boolean,
      "[Edition](#cfn-directoryservice-microsoftad-edition)" : String,
      "[EnableSso](#cfn-directoryservice-microsoftad-enablesso)" : Boolean,
      "[Name](#cfn-directoryservice-microsoftad-name)" : String,
      "[Password](#cfn-directoryservice-microsoftad-password)" : String,
      "[ShortName](#cfn-directoryservice-microsoftad-shortname)" : String,
      "[VpcSettings](#cfn-directoryservice-microsoftad-vpcsettings)" : VpcSettings
    }
}
```

### YAML<a name="aws-resource-directoryservice-microsoftad-syntax.yaml"></a>

```
Type: AWS::DirectoryService::MicrosoftAD
Properties: 
  [CreateAlias](#cfn-directoryservice-microsoftad-createalias): Boolean
  [Edition](#cfn-directoryservice-microsoftad-edition): String
  [EnableSso](#cfn-directoryservice-microsoftad-enablesso): Boolean
  [Name](#cfn-directoryservice-microsoftad-name): String
  [Password](#cfn-directoryservice-microsoftad-password): String
  [ShortName](#cfn-directoryservice-microsoftad-shortname): String
  [VpcSettings](#cfn-directoryservice-microsoftad-vpcsettings): 
    VpcSettings
```

## Properties<a name="aws-resource-directoryservice-microsoftad-properties"></a>

`CreateAlias`  <a name="cfn-directoryservice-microsoftad-createalias"></a>
Specifies an alias for a directory and assigns the alias to the directory\. The alias is used to construct the access URL for the directory, such as `http://<alias>.awsapps.com`\. By default, AWS CloudFormation does not create an alias\.  
After an alias has been created, it cannot be deleted or reused, so this operation should only be used when absolutely necessary\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Edition`  <a name="cfn-directoryservice-microsoftad-edition"></a>
AWS Managed Microsoft AD is available in two editions: `Standard` and `Enterprise`\. `Enterprise` is the default\.  
*Required*: No  
*Type*: String  
*Allowed values*: `Enterprise | Standard`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EnableSso`  <a name="cfn-directoryservice-microsoftad-enablesso"></a>
Whether to enable single sign\-on for a Microsoft Active Directory in AWS\. Single sign\-on allows users in your directory to access certain AWS services from a computer joined to the directory without having to enter their credentials separately\. If you don't specify a value, AWS CloudFormation disables single sign\-on by default\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-directoryservice-microsoftad-name"></a>
The fully qualified domain name for the AWS Managed Microsoft AD directory, such as `corp.example.com`\. This name will resolve inside your VPC only\. It does not need to be publicly resolvable\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^([a-zA-Z0-9]+[\\.-])+([a-zA-Z0-9])+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Password`  <a name="cfn-directoryservice-microsoftad-password"></a>
The password for the default administrative user named `Admin`\.  
If you need to change the password for the administrator account, see the [ResetUserPassword](https://docs.aws.amazon.com/directoryservice/latest/devguide/API_ResetUserPassword.html) API call in the *AWS Directory Service API Reference*\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `(?=^.{8,64}$)((?=.*\d)(?=.*[A-Z])(?=.*[a-z])|(?=.*\d)(?=.*[^A-Za-z0-9\s])(?=.*[a-z])|(?=.*[^A-Za-z0-9\s])(?=.*[A-Z])(?=.*[a-z])|(?=.*\d)(?=.*[A-Z])(?=.*[^A-Za-z0-9\s]))^.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ShortName`  <a name="cfn-directoryservice-microsoftad-shortname"></a>
The NetBIOS name for your domain, such as `CORP`\. If you don't specify a NetBIOS name, it will default to the first part of your directory DNS\. For example, `CORP` for the directory DNS `corp.example.com`\.   
*Required*: No  
*Type*: String  
*Pattern*: `^[^\\/:*?"<>|.]+[^\\/:*?"<>|]*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpcSettings`  <a name="cfn-directoryservice-microsoftad-vpcsettings"></a>
Specifies the VPC settings of the Microsoft AD directory server in AWS\.  
*Required*: Yes  
*Type*: [VpcSettings](aws-properties-directoryservice-microsoftad-vpcsettings.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-directoryservice-microsoftad-return-values"></a>

### Ref<a name="aws-resource-directoryservice-microsoftad-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource ID\.

In the following sample, the `Ref` function returns the ID of the `myDirectory` directory, such as `d-12345ab592`\.

`{ "Ref": "myDirectory" }`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-directoryservice-microsoftad-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-directoryservice-microsoftad-return-values-fn--getatt-fn--getatt"></a>

`Alias`  <a name="Alias-fn::getatt"></a>
The alias for a directory\. For example: `d-12373a053a` or `alias4-mydirectory-12345abcgmzsk` \(if you have the `CreateAlias` property set to true\)\.

`DnsIpAddresses`  <a name="DnsIpAddresses-fn::getatt"></a>
The IP addresses of the DNS servers for the directory, such as `[ "192.0.2.1", "192.0.2.2" ]`\.

## Examples<a name="aws-resource-directoryservice-microsoftad--examples"></a>

The following example creates a Microsoft Active Directory in AWS, where the directory DNS name is `corp.example.com`:

### Create an AWS Managed Microsoft Directory<a name="aws-resource-directoryservice-microsoftad--examples--Create_an_AWS_Managed_Microsoft_Directory"></a>

#### JSON<a name="aws-resource-directoryservice-microsoftad--examples--Create_an_AWS_Managed_Microsoft_Directory--json"></a>

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

#### YAML<a name="aws-resource-directoryservice-microsoftad--examples--Create_an_AWS_Managed_Microsoft_Directory--yaml"></a>

```
myDirectory: 
  Type: AWS::DirectoryService::MicrosoftAD
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

## See also<a name="aws-resource-directoryservice-microsoftad--seealso"></a>
+ [Getting Started with AWS Managed Microsoft AD](https://docs.aws.amazon.com/directoryservice/latest/admin-guide/ms_ad_getting_started.html) in the *AWS Directory Service Admin Guide*\.\.
+ [CreateMicrosoftAD](https://docs.aws.amazon.com/directoryservice/latest/devguide/API_CreateMicrosoftAD.html) in the *AWS Directory Service API Reference*\.

