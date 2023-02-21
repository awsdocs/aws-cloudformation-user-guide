# AWS::FSx::StorageVirtualMachine<a name="aws-resource-fsx-storagevirtualmachine"></a>

Creates a storage virtual machine \(SVM\) for an Amazon FSx for ONTAP file system\.

## Syntax<a name="aws-resource-fsx-storagevirtualmachine-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-fsx-storagevirtualmachine-syntax.json"></a>

```
{
  "Type" : "AWS::FSx::StorageVirtualMachine",
  "Properties" : {
      "[ActiveDirectoryConfiguration](#cfn-fsx-storagevirtualmachine-activedirectoryconfiguration)" : ActiveDirectoryConfiguration,
      "[FileSystemId](#cfn-fsx-storagevirtualmachine-filesystemid)" : String,
      "[Name](#cfn-fsx-storagevirtualmachine-name)" : String,
      "[RootVolumeSecurityStyle](#cfn-fsx-storagevirtualmachine-rootvolumesecuritystyle)" : String,
      "[SvmAdminPassword](#cfn-fsx-storagevirtualmachine-svmadminpassword)" : String,
      "[Tags](#cfn-fsx-storagevirtualmachine-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-fsx-storagevirtualmachine-syntax.yaml"></a>

```
Type: AWS::FSx::StorageVirtualMachine
Properties: 
  [ActiveDirectoryConfiguration](#cfn-fsx-storagevirtualmachine-activedirectoryconfiguration): 
    ActiveDirectoryConfiguration
  [FileSystemId](#cfn-fsx-storagevirtualmachine-filesystemid): String
  [Name](#cfn-fsx-storagevirtualmachine-name): String
  [RootVolumeSecurityStyle](#cfn-fsx-storagevirtualmachine-rootvolumesecuritystyle): String
  [SvmAdminPassword](#cfn-fsx-storagevirtualmachine-svmadminpassword): String
  [Tags](#cfn-fsx-storagevirtualmachine-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-fsx-storagevirtualmachine-properties"></a>

`ActiveDirectoryConfiguration`  <a name="cfn-fsx-storagevirtualmachine-activedirectoryconfiguration"></a>
Describes the Microsoft Active Directory configuration to which the SVM is joined, if applicable\.  
*Required*: No  
*Type*: [ActiveDirectoryConfiguration](aws-properties-fsx-storagevirtualmachine-activedirectoryconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FileSystemId`  <a name="cfn-fsx-storagevirtualmachine-filesystemid"></a>
Specifies the FSx for ONTAP file system on which to create the SVM\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-fsx-storagevirtualmachine-name"></a>
The name of the SVM\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `47`  
*Pattern*: `^[^\u0000\u0085\u2028\u2029\r\n]{1,47}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RootVolumeSecurityStyle`  <a name="cfn-fsx-storagevirtualmachine-rootvolumesecuritystyle"></a>
The security style of the root volume of the SVM\. Specify one of the following values:  
+  `UNIX` if the file system is managed by a UNIX administrator, the majority of users are NFS clients, and an application accessing the data uses a UNIX user as the service account\.
+  `NTFS` if the file system is managed by a Windows administrator, the majority of users are SMB clients, and an application accessing the data uses a Windows user as the service account\.
+  `MIXED` if the file system is managed by both UNIX and Windows administrators and users consist of both NFS and SMB clients\.
*Required*: No  
*Type*: String  
*Allowed values*: `MIXED | NTFS | UNIX`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SvmAdminPassword`  <a name="cfn-fsx-storagevirtualmachine-svmadminpassword"></a>
Specifies the password to use when logging on to the SVM using a secure shell \(SSH\) connection to the SVM's management endpoint\. Doing so enables you to manage the SVM using the NetApp ONTAP CLI or REST API\. If you do not specify a password, you can still use the file system's `fsxadmin` user to manage the SVM\. For more information, see [ Managing SVMs using the NetApp ONTAP CLI](https://docs.aws.amazon.com/fsx/latest/ONTAPGuide/managing-resources-ontap-apps.html#vsadmin-ontap-cli) in the *FSx for ONTAP User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-fsx-storagevirtualmachine-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-fsx-storagevirtualmachine-return-values"></a>

### Ref<a name="aws-resource-fsx-storagevirtualmachine-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource ID, such as `svm-01234567890123456`\. For example:

`{"Ref": "svm_logical_id"}` returns 

`svm-01234567890123456`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-fsx-storagevirtualmachine-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-fsx-storagevirtualmachine-return-values-fn--getatt-fn--getatt"></a>

`ResourceARN`  <a name="ResourceARN-fn::getatt"></a>
Returns the storage virtual machine's Amazon Resource Name \(ARN\)\.  
Example: `arn:aws:fsx:us-east-2:111111111111:storage-virtual-machine/fs-0123456789abcdef1/svm-01234567890123456`

`StorageVirtualMachineId`  <a name="StorageVirtualMachineId-fn::getatt"></a>
Returns the storgage virtual machine's system generated ID\.  
Example: `svm-0123456789abcedf1`

`UUID`  <a name="UUID-fn::getatt"></a>
Returns the storage virtual machine's system generated unique identifier \(UUID\)\.  
Example: `abcd0123-cd45-ef67-11aa-1111aaaa23bc`

## Examples<a name="aws-resource-fsx-storagevirtualmachine--examples"></a>



### Create an Amazon FSx for NetApp ONTAP Storage Virtual Machine<a name="aws-resource-fsx-storagevirtualmachine--examples--Create_an_Amazon_FSx_for_NetApp_ONTAP_Storage_Virtual_Machine"></a>

The following examples create an Amazon FSx for NetApp ONTAP storage virtual machine \(SVN\) that's joined to a self\-managed Active Directory domain\.

#### JSON<a name="aws-resource-fsx-storagevirtualmachine--examples--Create_an_Amazon_FSx_for_NetApp_ONTAP_Storage_Virtual_Machine--json"></a>

```
{
  "OntapStorageVirtualMachineWithAllConfigs": {
    "Type": "AWS::FSx::StorageVirtualMachine",
    "Properties": {
      "ActiveDirectoryConfiguration": {
        "NetBiosName": "svm1",
        "SelfManagedActiveDirectoryConfiguration": {
          "DnsIps": [
            "10.0.10.67"
          ],
          "DomainName": "CFN-CUSTOMER-AD.SIMBA.LOCAL",
          "FileSystemAdministratorsGroup": "Domain Admins",
          "OrganizationalUnitDistinguishedName": "OU=cfn-customer-ad,DC=cfn-customer-ad,DC=simba,DC=local",
          "Password": {
            "Fn::Join": [
              ":",
              [
                "{{resolve:secretsmanager",
                {
                  "Fn::ImportValue": "CustomerADCredentialName"
              },
              "SecretString}}"
            ]
          ]
        },
        "UserName": "Admin"
      }
    },
    "FileSystemId": {
      "Ref": "OntapMultiAzFileSystemWithAllConfigs"
    },
    "Name": "svm1",
    "RootVolumeSecurityStyle": "MIXED",
    "SvmAdminPassword": {
      "Password": {
        "Fn::Join": [
        ":",
        [
          "{{resolve:secretsmanager",
            {
              "Fn::ImportValue": "CustomerADCredentialName"
              },
              "SecretString}}"
            ]
          ]
        }
      },
      "Tags": [
        {
          "Key": "Name",
          "Value": "OntapSvm"
        }
      ]
    }
  }
}
```

#### YAML<a name="aws-resource-fsx-storagevirtualmachine--examples--Create_an_Amazon_FSx_for_NetApp_ONTAP_Storage_Virtual_Machine--yaml"></a>

```
OntapStorageVirtualMachineWithAllConfigs:
  Type: "AWS::FSx::StorageVirtualMachine"
  Properties:
    ActiveDirectoryConfiguration:
      NetBiosName: "svm1"
      SelfManagedActiveDirectoryConfiguration:
        DnsIps: ["10.0.10.67"]
        DomainName: "CFN-CUSTOMER-AD.SIMBA.LOCAL"
        FileSystemAdministratorsGroup: "Domain Admins"
        OrganizationalUnitDistinguishedName: "OU=cfn-customer-ad,DC=cfn-customer-ad,DC=simba,DC=local"
        Password:
          !Join
          - ':'
          - - '{{resolve:secretsmanager'
            - !ImportValue CustomerADCredentialName
            - 'SecretString}}'
        UserName: "Admin"
    FileSystemId: !Ref OntapMultiAzFileSystemWithAllConfigs
    Name: "svm1"
    RootVolumeSecurityStyle: "MIXED"
    SvmAdminPassword:
      Password:
        !Join
        - ':'
        - - '{{resolve:secretsmanager'
          - !ImportValue CustomerADCredentialName
          - 'SecretString}}'
    Tags:
      - Key: "Name"
        Value: "OntapSvm"
```