# AWS::FSx::StorageVirtualMachine SelfManagedActiveDirectoryConfiguration<a name="aws-properties-fsx-storagevirtualmachine-activedirectoryconfiguration-selfmanagedactivedirectoryconfiguration"></a>

The configuration that Amazon FSx uses to join a FSx for Windows File Server file system or an ONTAP storage virtual machine \(SVM\) to a self\-managed \(including on\-premises\) Microsoft Active Directory \(AD\) directory\. For more information, see [ Using Amazon FSx with your self\-managed Microsoft Active Directory](https://docs.aws.amazon.com/fsx/latest/WindowsGuide/self-managed-AD.html) or [Managing SVMs](https://docs.aws.amazon.com/fsx/latest/ONTAPGuide/managing-svms.html)\.

## Syntax<a name="aws-properties-fsx-storagevirtualmachine-activedirectoryconfiguration-selfmanagedactivedirectoryconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fsx-storagevirtualmachine-activedirectoryconfiguration-selfmanagedactivedirectoryconfiguration-syntax.json"></a>

```
{
  "[DnsIps](#cfn-fsx-storagevirtualmachine-activedirectoryconfiguration-selfmanagedactivedirectoryconfiguration-dnsips)" : [ String, ... ],
  "[DomainName](#cfn-fsx-storagevirtualmachine-activedirectoryconfiguration-selfmanagedactivedirectoryconfiguration-domainname)" : String,
  "[FileSystemAdministratorsGroup](#cfn-fsx-storagevirtualmachine-activedirectoryconfiguration-selfmanagedactivedirectoryconfiguration-filesystemadministratorsgroup)" : String,
  "[OrganizationalUnitDistinguishedName](#cfn-fsx-storagevirtualmachine-activedirectoryconfiguration-selfmanagedactivedirectoryconfiguration-organizationalunitdistinguishedname)" : String,
  "[Password](#cfn-fsx-storagevirtualmachine-activedirectoryconfiguration-selfmanagedactivedirectoryconfiguration-password)" : String,
  "[UserName](#cfn-fsx-storagevirtualmachine-activedirectoryconfiguration-selfmanagedactivedirectoryconfiguration-username)" : String
}
```

### YAML<a name="aws-properties-fsx-storagevirtualmachine-activedirectoryconfiguration-selfmanagedactivedirectoryconfiguration-syntax.yaml"></a>

```
  [DnsIps](#cfn-fsx-storagevirtualmachine-activedirectoryconfiguration-selfmanagedactivedirectoryconfiguration-dnsips): 
    - String
  [DomainName](#cfn-fsx-storagevirtualmachine-activedirectoryconfiguration-selfmanagedactivedirectoryconfiguration-domainname): String
  [FileSystemAdministratorsGroup](#cfn-fsx-storagevirtualmachine-activedirectoryconfiguration-selfmanagedactivedirectoryconfiguration-filesystemadministratorsgroup): String
  [OrganizationalUnitDistinguishedName](#cfn-fsx-storagevirtualmachine-activedirectoryconfiguration-selfmanagedactivedirectoryconfiguration-organizationalunitdistinguishedname): String
  [Password](#cfn-fsx-storagevirtualmachine-activedirectoryconfiguration-selfmanagedactivedirectoryconfiguration-password): String
  [UserName](#cfn-fsx-storagevirtualmachine-activedirectoryconfiguration-selfmanagedactivedirectoryconfiguration-username): String
```

## Properties<a name="aws-properties-fsx-storagevirtualmachine-activedirectoryconfiguration-selfmanagedactivedirectoryconfiguration-properties"></a>

`DnsIps`  <a name="cfn-fsx-storagevirtualmachine-activedirectoryconfiguration-selfmanagedactivedirectoryconfiguration-dnsips"></a>
A list of up to three IP addresses of DNS servers or domain controllers in the self\-managed AD directory\.   
*Required*: No  
*Type*: List of String  
*Maximum*: `3`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DomainName`  <a name="cfn-fsx-storagevirtualmachine-activedirectoryconfiguration-selfmanagedactivedirectoryconfiguration-domainname"></a>
The fully qualified domain name of the self\-managed AD directory, such as `corp.example.com`\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `^[^\u0000\u0085\u2028\u2029\r\n]{1,255}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FileSystemAdministratorsGroup`  <a name="cfn-fsx-storagevirtualmachine-activedirectoryconfiguration-selfmanagedactivedirectoryconfiguration-filesystemadministratorsgroup"></a>
\(Optional\) The name of the domain group whose members are granted administrative privileges for the file system\. Administrative privileges include taking ownership of files and folders, setting audit controls \(audit ACLs\) on files and folders, and administering the file system remotely by using the FSx Remote PowerShell\. The group that you specify must already exist in your domain\. If you don't provide one, your AD domain's Domain Admins group is used\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^[^\u0000\u0085\u2028\u2029\r\n]{1,256}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OrganizationalUnitDistinguishedName`  <a name="cfn-fsx-storagevirtualmachine-activedirectoryconfiguration-selfmanagedactivedirectoryconfiguration-organizationalunitdistinguishedname"></a>
\(Optional\) The fully qualified distinguished name of the organizational unit within your self\-managed AD directory\. Amazon FSx only accepts OU as the direct parent of the file system\. An example is `OU=FSx,DC=yourdomain,DC=corp,DC=com`\. To learn more, see [RFC 2253](https://tools.ietf.org/html/rfc2253)\. If none is provided, the FSx file system is created in the default location of your self\-managed AD directory\.   
Only Organizational Unit \(OU\) objects can be the direct parent of the file system that you're creating\.
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2000`  
*Pattern*: `^[^\u0000\u0085\u2028\u2029\r\n]{1,2000}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Password`  <a name="cfn-fsx-storagevirtualmachine-activedirectoryconfiguration-selfmanagedactivedirectoryconfiguration-password"></a>
The password for the service account on your self\-managed AD domain that Amazon FSx will use to join to your AD domain\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^.{1,256}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserName`  <a name="cfn-fsx-storagevirtualmachine-activedirectoryconfiguration-selfmanagedactivedirectoryconfiguration-username"></a>
The user name for the service account on your self\-managed AD domain that Amazon FSx will use to join to your AD domain\. This account must have the permission to join computers to the domain in the organizational unit provided in `OrganizationalUnitDistinguishedName`, or in the default location of your AD domain\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^[^\u0000\u0085\u2028\u2029\r\n]{1,256}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)