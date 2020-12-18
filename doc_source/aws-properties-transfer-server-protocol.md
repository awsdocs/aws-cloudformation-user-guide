# AWS::Transfer::Server Protocol<a name="aws-properties-transfer-server-protocol"></a>

Specifies the file transfer protocol or protocols over which your file transfer protocol client can connect to your server's endpoint\. The available protocols are:
+ `SFTP` \(Secure Shell \(SSH\) File Transfer Protocol\): File transfer over SSH
+ `FTPS` \(File Transfer Protocol Secure\): File transfer with TLS encryption
+ `FTP` \(File Transfer Protocol\): Unencrypted file transfer

**Note**  
If you select `FTPS`, you must choose a certificate stored in AWS Certificate Manager \(ACM\) which will be used to identify your server when clients connect to it over FTPS\.  
If `Protocol` includes either `FTP` or `FTPS`, then the `EndpointType` must be `VPC` and the `IdentityProviderType` must be `API_GATEWAY`\.  
If `Protocol` includes `FTP`, then `AddressAllocationIds` cannot be associated\.  
If `Protocol` is set only to `SFTP`, the `EndpointType` can be set to `PUBLIC` and the `IdentityProviderType` can be set to `SERVICE_MANAGED`\.