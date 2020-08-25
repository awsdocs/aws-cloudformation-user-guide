# AWS::FSx::FileSystem SelfManagedActiveDirectoryConfiguration<a name="aws-properties-fsx-filesystem-windowsconfiguration-selfmanagedactivedirectoryconfiguration"></a>

The configuration that Amazon FSx uses to join the Windows File Server instance to your self\-managed \(including on\-premises\) Microsoft Active Directory \(AD\) directory\.

## Syntax<a name="aws-properties-fsx-filesystem-windowsconfiguration-selfmanagedactivedirectoryconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fsx-filesystem-windowsconfiguration-selfmanagedactivedirectoryconfiguration-syntax.json"></a>

```
{
  "[DnsIps](#cfn-fsx-filesystem-windowsconfiguration-selfmanagedactivedirectoryconfiguration-dnsips)" : [ String, ... ],
  "[DomainName](#cfn-fsx-filesystem-windowsconfiguration-selfmanagedactivedirectoryconfiguration-domainname)" : String,
  "[FileSystemAdministratorsGroup](#cfn-fsx-filesystem-windowsconfiguration-selfmanagedactivedirectoryconfiguration-filesystemadministratorsgroup)" : String,
  "[OrganizationalUnitDistinguishedName](#cfn-fsx-filesystem-windowsconfiguration-selfmanagedactivedirectoryconfiguration-organizationalunitdistinguishedname)" : String,
  "[Password](#cfn-fsx-filesystem-windowsconfiguration-selfmanagedactivedirectoryconfiguration-password)" : String,
  "[UserName](#cfn-fsx-filesystem-windowsconfiguration-selfmanagedactivedirectoryconfiguration-username)" : String
}
```

### YAML<a name="aws-properties-fsx-filesystem-windowsconfiguration-selfmanagedactivedirectoryconfiguration-syntax.yaml"></a>

```
  [DnsIps](#cfn-fsx-filesystem-windowsconfiguration-selfmanagedactivedirectoryconfiguration-dnsips): 
    - String
  [DomainName](#cfn-fsx-filesystem-windowsconfiguration-selfmanagedactivedirectoryconfiguration-domainname): String
  [FileSystemAdministratorsGroup](#cfn-fsx-filesystem-windowsconfiguration-selfmanagedactivedirectoryconfiguration-filesystemadministratorsgroup): String
  [OrganizationalUnitDistinguishedName](#cfn-fsx-filesystem-windowsconfiguration-selfmanagedactivedirectoryconfiguration-organizationalunitdistinguishedname): String
  [Password](#cfn-fsx-filesystem-windowsconfiguration-selfmanagedactivedirectoryconfiguration-password): String
  [UserName](#cfn-fsx-filesystem-windowsconfiguration-selfmanagedactivedirectoryconfiguration-username): String
```

## Properties<a name="aws-properties-fsx-filesystem-windowsconfiguration-selfmanagedactivedirectoryconfiguration-properties"></a>

`DnsIps`  <a name="cfn-fsx-filesystem-windowsconfiguration-selfmanagedactivedirectoryconfiguration-dnsips"></a>
A list of up to two IP addresses of DNS servers or domain controllers in the self\-managed AD directory\. The IP addresses need to be either in the same VPC CIDR range as the one in which your Amazon FSx file system is being created, or in the private IP version 4 \(IPv4\) address ranges, as specified in [RFC 1918](http://www.faqs.org/rfcs/rfc1918.html):  
+ 10\.0\.0\.0 \- 10\.255\.255\.255 \(10/8 prefix\)
+ 172\.16\.0\.0 \- 172\.31\.255\.255 \(172\.16/12 prefix\)
+ 192\.168\.0\.0 \- 192\.168\.255\.255 \(192\.168/16 prefix\)
*Required*: No  
*Type*: List of String  
*Maximum*: `2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DomainName`  <a name="cfn-fsx-filesystem-windowsconfiguration-selfmanagedactivedirectoryconfiguration-domainname"></a>
The fully qualified domain name of the self\-managed AD directory, such as `corp.example.com`\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `^[^\u0000\u0085\u2028\u2029\r\n]{1,255}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FileSystemAdministratorsGroup`  <a name="cfn-fsx-filesystem-windowsconfiguration-selfmanagedactivedirectoryconfiguration-filesystemadministratorsgroup"></a>
\(Optional\) The name of the domain group whose members are granted administrative privileges for the file system\. Administrative privileges include taking ownership of files and folders, setting audit controls \(audit ACLs\) on files and folders, and administering the file system remotely by using the FSx Remote PowerShell\. The group that you specify must already exist in your domain\. If you don't provide one, your AD domain's Domain Admins group is used\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^[^\u0000\u0085\u2028\u2029\r\n]{1,256}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OrganizationalUnitDistinguishedName`  <a name="cfn-fsx-filesystem-windowsconfiguration-selfmanagedactivedirectoryconfiguration-organizationalunitdistinguishedname"></a>
\(Optional\) The fully qualified distinguished name of the organizational unit within your self\-managed AD directory that the Windows File Server instance will join\. Amazon FSx only accepts OU as the direct parent of the file system\. An example is `OU=FSx,DC=yourdomain,DC=corp,DC=com`\. To learn more, see [RFC 2253](https://tools.ietf.org/html/rfc2253)\. If none is provided, the FSx file system is created in the default location of your self\-managed AD directory\.   
Only Organizational Unit \(OU\) objects can be the direct parent of the file system that you're creating\.
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2000`  
*Pattern*: `^[^\u0000\u0085\u2028\u2029\r\n]{1,2000}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Password`  <a name="cfn-fsx-filesystem-windowsconfiguration-selfmanagedactivedirectoryconfiguration-password"></a>
The password for the service account on your self\-managed AD domain that Amazon FSx will use to join to your AD domain\. We strongly suggest that you follow best practices and *do not* embed passwords in your CFN templates\.   
The recommended approach is to use AWS Secrets Manager to store your passwords\. You can retrieve them for use in your templates using the `secretsmanager` dynamic reference\. There are additional costs associated with using AWS Secrets Manager\. To learn more, see [Secrets Manager secrets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/dynamic-references.html#dynamic-references-secretsmanager) in the *AWS CloudFormation User Guide*\.  
Alternatively, you can use the `NoEcho` property to obfuscate the password parameter value\. For more information, see [Do Not Embed Credentials in Your Templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/best-practices.html#creds) in the *AWS CloudFormation User Guide*\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^.{1,256}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserName`  <a name="cfn-fsx-filesystem-windowsconfiguration-selfmanagedactivedirectoryconfiguration-username"></a>
The user name for the service account on your self\-managed AD domain that Amazon FSx will use to join to your AD domain\. This account must have the permission to join computers to the domain in the organizational unit provided in `OrganizationalUnitDistinguishedName`, or in the default location of your AD domain\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^[^\u0000\u0085\u2028\u2029\r\n]{1,256}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)