# AWS Key Management Service Developer Guide

-----
*****Copyright &copy; Amazon Web Services, Inc. and/or its affiliates. All rights reserved.*****

-----
Amazon's trademarks and trade dress may not be used in 
     connection with any product or service that is not Amazon's, 
     in any manner that is likely to cause confusion among customers, 
     or in any manner that disparages or discredits Amazon. All other 
     trademarks not owned by Amazon are the property of their respective
     owners, who may or may not be affiliated with, connected to, or 
     sponsored by Amazon.

-----
## Contents
+ [AWS Key Management Service](overview.md)
   + [AWS KMS concepts](concepts.md)
+ [Managing keys](getting-started.md)
   + [Creating keys](create-keys.md)
   + [Using aliases](kms-alias.md)
      + [About aliases](alias-about.md)
      + [Managing aliases](alias-manage.md)
      + [Using aliases in your applications](alias-using.md)
      + [Controlling access to aliases](alias-access.md)
      + [Using aliases to control access to KMS keys](alias-authorization.md)
      + [Finding aliases in AWS CloudTrail logs](alias-ct.md)
   + [Viewing keys](viewing-keys.md)
      + [Viewing KMS keys in the console](viewing-keys-console.md)
      + [Viewing KMS keys with the API](viewing-keys-cli.md)
      + [Viewing the cryptographic configuration of KMS keys](symm-asymm-crypto-config.md)
      + [Finding the key ID and key ARN](find-cmk-id-arn.md)
      + [Finding the alias name and alias ARN](find-cmk-alias.md)
   + [Editing keys](editing-keys.md)
   + [Tagging keys](tagging-keys.md)
      + [About tags in AWS KMS](tags-about.md)
      + [Managing KMS key tags in the console](manage-tags-console.md)
      + [Managing KMS key tags with API operations](manage-tags-api.md)
      + [Controlling access to tags](tag-permissions.md)
      + [Using tags to control access to KMS keys](tag-authorization.md)
   + [Enabling and disabling keys](enabling-keys.md)
   + [Rotating AWS KMS keys](rotate-keys.md)
   + [Monitoring AWS KMS keys](monitoring-overview.md)
      + [Logging AWS KMS API calls with AWS CloudTrail](logging-using-cloudtrail.md)
         + [Examples of AWS KMS log entries](understanding-kms-entries.md)
            + [CancelKeyDeletion](ct-cancel-key-deletion.md)
            + [ConnectCustomKeyStore](ct-connect-keystore.md)
            + [CreateAlias](ct-createalias.md)
            + [CreateCustomKeyStore](ct-create-keystore.md)
            + [CreateGrant](ct-creategrant.md)
            + [CreateKey](ct-createkey.md)
            + [Decrypt](ct-decrypt.md)
            + [Decrypt (from an enclave)](ct-decrypt-enclave.md)
            + [DeleteAlias](ct-deletealias.md)
            + [DeleteCustomKeyStore](ct-delete-keystore.md)
            + [DeleteExpiredKeyMaterial](ct-deleteexpiredkeymaterial.md)
            + [DeleteKey](ct-delete-key.md)
            + [DescribeCustomKeyStores](ct-describe-keystores.md)
            + [DescribeKey](ct-describekey.md)
            + [DisableKey](ct-disablekey.md)
            + [DisconnectCustomKeyStore](ct-disconnect-keystore.md)
            + [EnableKey](ct-enablekey.md)
            + [EnableKeyRotation](ct-enablekeyrotation.md)
            + [Encrypt](ct-encrypt.md)
            + [GenerateDataKey](ct-generatedatakey.md)
            + [GenerateDataKey (from an enclave)](ct-generate-data-key-enclave.md)
            + [GenerateDataKeyPair](ct-generatedatakeypair.md)
            + [GenerateDataKeyPairWithoutPlaintext](ct-generatedatakeypairwithoutplaintext.md)
            + [GenerateDataKeyWithoutPlaintext](ct-generatedatakeyplaintext.md)
            + [GenerateMac](ct-generatemac.md)
            + [GenerateRandom](ct-generaterandom.md)
            + [GenerateRandom (from an enclave)](ct-generate-random-enclave.md)
            + [GetKeyPolicy](ct-getkeypolicy.md)
            + [GetParametersForImport](ct-getparametersforimport.md)
            + [ImportKeyMaterial](ct-importkeymaterial.md)
            + [ListAliases](ct-listaliases.md)
            + [ListGrants](ct-listgrants.md)
            + [ReEncrypt](ct-reencrypt.md)
            + [ReplicateKey](ct-replicate-key.md)
            + [RotateKey](ct-rotatekey.md)
            + [ScheduleKeyDeletion](ct-schedule-key-deletion.md)
            + [Sign](ct-sign.md)
            + [SynchronizeMultiRegionKey](ct-synchronize-multi-region-key.md)
            + [TagResource](ct-tagresource.md)
            + [UntagResource](ct-untagresource.md)
            + [UpdateAlias](ct-updatealias.md)
            + [UpdateCustomKeyStore](ct-update-keystore.md)
            + [UpdatePrimaryRegion](ct-update-primary-region.md)
            + [VerifyMac](ct-verifymac.md)
            + [Verify](ct-verify.md)
            + [Amazon EC2 example one](ct-ec2one.md)
            + [Amazon EC2 example two](ct-ec2two.md)
      + [Monitoring with Amazon CloudWatch](monitoring-cloudwatch.md)
   + [Creating AWS KMS resources with AWS CloudFormation](creating-resources-with-cloudformation.md)
   + [Deleting AWS KMS keys](deleting-keys.md)
      + [Creating an Amazon CloudWatch alarm to detect usage of an AWS KMS key pending deletion](deleting-keys-creating-cloudwatch-alarm.md)
      + [Determining past usage of a KMS key](deleting-keys-determining-usage.md)
   + [Key states of AWS KMS keys](key-state.md)
+ [Authentication and access control for AWS KMS](control-access.md)
   + [Key policies in AWS KMS](key-policies.md)
      + [Creating a key policy](key-policy-overview.md)
      + [Default key policy](key-policy-default.md)
      + [Viewing a key policy](key-policy-viewing.md)
      + [Changing a key policy](key-policy-modifying.md)
      + [Permissions for AWS services in key policies](key-policy-services.md)
   + [Using IAM policies with AWS KMS](iam-policies.md)
      + [Overview of IAM policies](iam-policies-overview.md)
      + [Best practices for IAM policies](iam-policies-best-practices.md)
      + [Specifying KMS keys in IAM policy statements](cmks-in-iam-policies.md)
      + [Permissions required to use the AWS KMS console](console-permissions.md)
      + [AWS managed policy for power users](aws-managed-policies.md)
      + [IAM policy examples](customer-managed-policies.md)
   + [Grants in AWS KMS](grants.md)
      + [Creating grants](create-grant-overview.md)
      + [Managing grants](grant-manage.md)
   + [Connecting to AWS KMS through a VPC endpoint](kms-vpc-endpoint.md)
   + [Using policy conditions with AWS KMS](policy-conditions.md)
   + [ABAC for AWS KMS](abac.md)
   + [Allowing users in other accounts to use a KMS key](key-policy-modifying-external-accounts.md)
   + [Using service-linked roles for AWS KMS](using-service-linked-roles.md)
   + [Using hybrid post-quantum TLS with AWS KMS](pqtls.md)
   + [Determining access to AWS KMS keys](determining-access.md)
      + [Examining the key policy](determining-access-key-policy.md)
      + [Examining IAM policies](determining-access-iam-policies.md)
      + [Examining grants](determining-access-grants.md)
      + [Troubleshooting key access](policy-evaluation.md)
   + [AWS KMS permissions](kms-api-permissions-reference.md)
+ [Special-purpose keys](key-types.md)
   + [Asymmetric keys in AWS KMS](symmetric-asymmetric.md)
      + [Creating asymmetric KMS keys](asymm-create-key.md)
      + [Downloading public keys](download-public-key.md)
      + [Identifying asymmetric KMS keys](find-symm-asymm.md)
      + [Asymmetric key specs](asymmetric-key-specs.md)
   + [HMAC keys in AWS KMS](hmac.md)
      + [Creating HMAC KMS keys](hmac-create-key.md)
      + [Controlling access to HMAC KMS keys](hmac-authz.md)
      + [Viewing HMAC KMS keys](hmac-view.md)
   + [Multi-Region keys in AWS KMS](multi-region-keys-overview.md)
      + [Controlling access to multi-Region keys](multi-region-keys-auth.md)
      + [Creating multi-Region keys](multi-region-keys-create.md)
         + [Creating multi-Region primary keys](create-primary-keys.md)
         + [Creating multi-Region replica keys](multi-region-keys-replicate.md)
      + [Viewing multi-Region keys](multi-region-keys-view.md)
      + [Managing multi-Region keys](multi-region-keys-manage.md)
      + [Importing key material into multi-Region keys](multi-region-keys-import.md)
      + [Deleting multi-Region keys](multi-region-keys-delete.md)
   + [Importing key material in AWS KMS keys](importing-keys.md)
      + [Importing key material step 1: Create an AWS KMS key without key material](importing-keys-create-cmk.md)
      + [Importing key material step 2: Download the public key and import token](importing-keys-get-public-key-and-token.md)
      + [Importing key material step 3: Encrypt the key material](importing-keys-encrypt-key-material.md)
      + [Importing key material step 4: Import the key material](importing-keys-import-key-material.md)
      + [Deleting imported key material](importing-keys-delete-key-material.md)
   + [Custom key stores](custom-key-store-overview.md)
      + [What is a custom key store?](key-store-concepts.md)
      + [Controlling access to your custom key store](authorize-key-store.md)
      + [Creating a custom key store](create-keystore.md)
      + [Managing a custom key store](manage-keystore.md)
         + [Viewing a custom key store](view-keystore.md)
         + [Editing custom key store settings](update-keystore.md)
         + [Connecting and disconnecting a custom key store](disconnect-keystore.md)
         + [Deleting a custom key store](delete-keystore.md)
      + [Managing KMS keys in a custom key store](manage-cmk-keystore.md)
         + [Creating KMS keys in a custom key store](create-cmk-keystore.md)
         + [Viewing KMS keys in a custom key store](view-cmk-keystore.md)
         + [Using KMS keys in a custom key store](use-cmk-keystore.md)
         + [Finding KMS keys and key material](find-key-material.md)
         + [Scheduling deletion of KMS keys from a custom key store](delete-cmk-keystore.md)
      + [Troubleshooting a custom key store](fix-keystore.md)
   + [Key type reference](symm-asymm-compare.md)
+ [Security of AWS Key Management Service](kms-security.md)
   + [Data protection in AWS Key Management Service](data-protection.md)
   + [Identity and access management for AWS Key Management Service](security-iam.md)
   + [Logging and monitoring in AWS Key Management Service](security-logging-monitoring.md)
   + [Compliance validation for AWS Key Management Service](kms-compliance.md)
   + [Infrastructure security in AWS Key Management Service](infrastructure-security.md)
   + [Security best practices for AWS Key Management Service](best-practices.md)
+ [Quotas](limits.md)
   + [Resource quotas](resource-limits.md)
   + [Request quotas](requests-per-second.md)
   + [Throttling AWS KMS requests](throttling.md)
   + [Requesting an AWS KMS quota increase](increase-quota.md)
+ [How AWS services use AWS KMS](service-integration.md)
   + [How AWS CloudTrail uses AWS KMS](services-cloudtrail.md)
   + [How Amazon DynamoDB uses AWS KMS](services-dynamodb.md)
   + [How Amazon Elastic Block Store (Amazon EBS) uses AWS KMS](services-ebs.md)
   + [How Amazon Elastic Transcoder uses AWS KMS](services-et.md)
   + [How Amazon EMR uses AWS KMS](services-emr.md)
   + [How AWS Nitro Enclaves uses AWS KMS](services-nitro-enclaves.md)
   + [How Amazon Redshift uses AWS KMS](services-redshift.md)
   + [How Amazon Relational Database Service (Amazon RDS) uses AWS KMS](services-rds.md)
   + [How AWS Secrets Manager uses AWS KMS](services-secrets-manager.md)
   + [How Amazon Simple Email Service (Amazon SES) uses AWS KMS](services-ses.md)
   + [How Amazon Simple Storage Service (Amazon S3) uses AWS KMS](services-s3.md)
   + [How AWS Systems Manager Parameter Store uses AWS KMS](services-parameter-store.md)
   + [How Amazon WorkMail uses AWS KMS](services-wm.md)
   + [How WorkSpaces uses AWS KMS](services-workspaces.md)
+ [Programming the AWS KMS API](programming-top.md)
   + [Creating a client](programming-client.md)
   + [Working with keys](programming-keys.md)
   + [Working with aliases](programming-aliases.md)
   + [Encrypting and decrypting data keys](programming-encryption.md)
   + [Working with key policies](programming-key-policies.md)
   + [Working with grants](programming-grants.md)
+ [References](references.md)
+ [Document history](dochistory.md)