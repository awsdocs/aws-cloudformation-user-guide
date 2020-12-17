# AWS::DirectoryService::SimpleAD<a name="aws-resource-directoryservice-simplead"></a>

The `AWS::DirectoryService::SimpleAD` resource specifies an AWS Directory Service Simple Active Directory \(Simple AD\) in AWS so that your directory users and groups can access the AWS Management Console and AWS applications using their existing credentials\. Simple AD is a Microsoft Active Directory–compatible directory\. For more information, see [Simple Active Directory](https://docs.aws.amazon.com/directoryservice/latest/admin-guide/directory_simple_ad.html) in the *AWS Directory Service Admin Guide*\.

## Syntax<a name="aws-resource-directoryservice-simplead-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-directoryservice-simplead-syntax.json"></a>

```
{
  "Type" : "AWS::DirectoryService::SimpleAD",
  "Properties" : {
      "[CreateAlias](#cfn-directoryservice-simplead-createalias)" : Boolean,
      "[Description](#cfn-directoryservice-simplead-description)" : String,
      "[EnableSso](#cfn-directoryservice-simplead-enablesso)" : Boolean,
      "[Name](#cfn-directoryservice-simplead-name)" : String,
      "[Password](#cfn-directoryservice-simplead-password)" : String,
      "[ShortName](#cfn-directoryservice-simplead-shortname)" : String,
      "[Size](#cfn-directoryservice-simplead-size)" : String,
      "[VpcSettings](#cfn-directoryservice-simplead-vpcsettings)" : VpcSettings
    }
}
```

### YAML<a name="aws-resource-directoryservice-simplead-syntax.yaml"></a>

```
Type: AWS::DirectoryService::SimpleAD
Properties: 
  [CreateAlias](#cfn-directoryservice-simplead-createalias): Boolean
  [Description](#cfn-directoryservice-simplead-description): String
  [EnableSso](#cfn-directoryservice-simplead-enablesso): Boolean
  [Name](#cfn-directoryservice-simplead-name): String
  [Password](#cfn-directoryservice-simplead-password): String
  [ShortName](#cfn-directoryservice-simplead-shortname): String
  [Size](#cfn-directoryservice-simplead-size): String
  [VpcSettings](#cfn-directoryservice-simplead-vpcsettings): 
    VpcSettings
```

## Properties<a name="aws-resource-directoryservice-simplead-properties"></a>

`CreateAlias`  <a name="cfn-directoryservice-simplead-createalias"></a>
If set to `true`, specifies an alias for a directory and assigns the alias to the directory\. The alias is used to construct the access URL for the directory, such as `http://<alias>.awsapps.com`\. By default, this property is set to `false`\.  
After an alias has been created, it cannot be deleted or reused, so this operation should only be used when absolutely necessary\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-directoryservice-simplead-description"></a>
A description for the directory\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `128`  
*Pattern*: `^([a-zA-Z0-9_])[\\a-zA-Z0-9_@#%*+=:?./!\s-]*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EnableSso`  <a name="cfn-directoryservice-simplead-enablesso"></a>
Whether to enable single sign\-on for a directory\. If you don't specify a value, AWS CloudFormation disables single sign\-on by default\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-directoryservice-simplead-name"></a>
The fully qualified name for the directory, such as `corp.example.com`\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^([a-zA-Z0-9]+[\\.-])+([a-zA-Z0-9])+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Password`  <a name="cfn-directoryservice-simplead-password"></a>
The password for the directory administrator\. The directory creation process creates a directory administrator account with the user name `Administrator` and this password\.  
If you need to change the password for the administrator account, see the [ResetUserPassword](https://docs.aws.amazon.com/directoryservice/latest/devguide/API_ResetUserPassword.html) API call in the *AWS Directory Service API Reference*\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `(?=^.{8,64}$)((?=.*\d)(?=.*[A-Z])(?=.*[a-z])|(?=.*\d)(?=.*[^A-Za-z0-9\s])(?=.*[a-z])|(?=.*[^A-Za-z0-9\s])(?=.*[A-Z])(?=.*[a-z])|(?=.*\d)(?=.*[A-Z])(?=.*[^A-Za-z0-9\s]))^.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ShortName`  <a name="cfn-directoryservice-simplead-shortname"></a>
The NetBIOS name of the directory, such as `CORP`\.  
*Required*: No  
*Type*: String  
*Pattern*: `^[^\\/:*?"<>|.]+[^\\/:*?"<>|]*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Size`  <a name="cfn-directoryservice-simplead-size"></a>
The size of the directory\. For valid values, see [CreateDirectory](https://docs.aws.amazon.com/directoryservice/latest/devguide/API_CreateDirectory.html) in the *AWS Directory Service API Reference*\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Large | Small`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpcSettings`  <a name="cfn-directoryservice-simplead-vpcsettings"></a>
A [DirectoryVpcSettings](https://docs.aws.amazon.com/directoryservice/latest/devguide/API_DirectoryVpcSettings.html) object that contains additional information for the operation\.  
*Required*: Yes  
*Type*: [VpcSettings](aws-properties-directoryservice-simplead-vpcsettings.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-directoryservice-simplead-return-values"></a>

### Ref<a name="aws-resource-directoryservice-simplead-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource ID\.

In the following sample, the `Ref` function returns the ID of the `myDirectory` directory, such as `d-1a2b3c4d5e`\.

`{ "Ref": "myDirectory" }`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-directoryservice-simplead-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-directoryservice-simplead-return-values-fn--getatt-fn--getatt"></a>

`Alias`  <a name="Alias-fn::getatt"></a>
The alias for a directory\. For example: `d-12373a053a` or `alias4-mydirectory-12345abcgmzsk` \(if you have the `CreateAlias` property set to true\)\.

`DnsIpAddresses`  <a name="DnsIpAddresses-fn::getatt"></a>
The IP addresses of the DNS servers for the directory, such as `[ "172.31.3.154", "172.31.63.203" ]`\.

## Examples<a name="aws-resource-directoryservice-simplead--examples"></a>

The following example creates a Simple AD directory, where the directory DNS name is `corp.example.com`:

### Create a Simple AD Directory<a name="aws-resource-directoryservice-simplead--examples--Create_a_Simple_AD_Directory"></a>

#### JSON<a name="aws-resource-directoryservice-simplead--examples--Create_a_Simple_AD_Directory--json"></a>

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

#### YAML<a name="aws-resource-directoryservice-simplead--examples--Create_a_Simple_AD_Directory--yaml"></a>

```
myDirectory: 
  Type: AWS::DirectoryService::SimpleAD
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

## See also<a name="aws-resource-directoryservice-simplead--seealso"></a>
+ [Getting Started with Simple AD](https://docs.aws.amazon.com/directoryservice/latest/admin-guide/simple_ad_getting_started.html) in the *AWS Directory Service Admin Guide*\.\.
+ [CreateDirectory](https://docs.aws.amazon.com/directoryservice/latest/devguide/API_CreateDirectory.html) in the *AWS Directory Service API Reference*\.

