
1.create user group role 
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": [
                "iam:CreateGroup",
                "iam:CreateRole",
                "iam:CreateUser"
            ],
            "Resource": "arn:aws:iam::006570735867:user/*"
        }
    ]
}

2.change password 

{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": "iam:ChangePassword",
            "Resource": "arn:aws:iam::006570735867:user/*"
        }
    ]
}
 
3.Delete user role group

{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": [
                "iam:DeleteGroup",
                "iam:DeleteRole",
                "iam:DeleteUser"
            ],
            "Resource": "arn:aws:iam::006570735867:user/*"
        }
    ]
}

4.create delete policy 

{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": [
                "iam:CreatePolicy",
                "iam:DeletePolicy"
            ],
            "Resource": "arn:aws:iam::006570735867:policy/*"
        }
    ]
}

5.IAM list policy 

{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": [
                "iam:ListRoleTags",
                "iam:ListInstanceProfileTags",
                "iam:ListServiceSpecificCredentials",
                "iam:ListMFADevices",
                "iam:ListSigningCertificates",
                "iam:ListInstanceProfilesForRole",
                "iam:ListSSHPublicKeys",
                "iam:ListAttachedRolePolicies",
                "iam:ListOpenIDConnectProviderTags",
                "iam:ListAttachedUserPolicies",
                "iam:ListSAMLProviderTags",
                "iam:ListAttachedGroupPolicies",
                "iam:ListPolicyTags",
                "iam:ListRolePolicies",
                "iam:ListAccessKeys",
                "iam:ListGroupPolicies",
                "iam:ListEntitiesForPolicy",
                "iam:ListUserPolicies",
                "iam:ListInstanceProfiles",
                "iam:ListPolicyVersions",
                "iam:ListGroupsForUser",
                "iam:ListServerCertificateTags",
                "iam:ListMFADeviceTags",
                "iam:GetLoginProfile",
                "iam:ListUserTags"
            ],
            "Resource": "arn:aws:iam::006570735867:user/*"
        },
        {
            "Sid": "VisualEditor1",
            "Effect": "Allow",
            "Action": [
                "iam:ListPolicies",
                "iam:ListSAMLProviders",
                "iam:ListOpenIDConnectProviders",
                "iam:ListServerCertificates",
                "iam:ListPoliciesGrantingServiceAccess",
                "iam:ListAccountAliases",
                "iam:ListRoles",
                "iam:ListUsers",
                "iam:ListGroups",
                "iam:ListVirtualMFADevices",
                "iam:GetAccountSummary"
            ],
            "Resource": "*"
        }
    ]
}

6.IAM read policy

{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": [
                "iam:GetServerCertificate",
                "iam:GetRole",
                "iam:GetPolicyVersion",
                "iam:GetInstanceProfile",
                "iam:GetPolicy",
                "iam:GetAccessKeyLastUsed",
                "iam:GetSSHPublicKey",
                "iam:GetGroup",
                "iam:GetContextKeysForPrincipalPolicy",
                "iam:GetServiceLinkedRoleDeletionStatus",
                "iam:SimulatePrincipalPolicy",
                "iam:GetUserPolicy",
                "iam:GenerateOrganizationsAccessReport",
                "iam:GetGroupPolicy",
                "iam:GetUser",
                "iam:GetOpenIDConnectProvider",
                "iam:GetRolePolicy",
                "iam:GetSAMLProvider"
            ],
            "Resource": "arn:aws:iam::006570735867:user/*"
        },
        {
            "Sid": "VisualEditor1",
            "Effect": "Allow",
            "Action": [
                "iam:GetContextKeysForCustomPolicy",
                "iam:GenerateCredentialReport",
                "iam:GetAccountPasswordPolicy",
                "iam:SimulateCustomPolicy",
                "iam:GetServiceLastAccessedDetailsWithEntities",
                "iam:GenerateServiceLastAccessedDetails",
                "iam:GetCredentialReport",
                "iam:GetServiceLastAccessedDetails",
                "iam:GetAccountAuthorizationDetails",
                "iam:GetOrganizationsAccessReport"
            ],
            "Resource": "*"
        }
    ]
}

7.Create delete bucket

{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": [
                "s3:CreateBucket",
                "s3:DeleteBucket"
            ],
            "Resource": "arn:aws:s3:::bucketonne"
        }
    ]
}

8.S3 list policy 

{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": [
                "s3:ListBucketMultipartUploads",
                "s3:ListBucketVersions",
                "s3:ListBucket",
                "s3:ListMultipartUploadParts"
            ],
            "Resource": "arn:aws:s3:::bucketonne"
        },
        {
            "Sid": "VisualEditor1",
            "Effect": "Allow",
            "Action": [
                "s3:ListStorageLensConfigurations",
                "s3:ListAllMyBuckets",
                "s3:ListJobs"
            ],
            "Resource": "*"
        }
    ]
}

9.Attach detach ec2 volume 

{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": [
                "ec2:DetachVolume",
                "ec2:AttachVolume"
            ],
            "Resource": "*"
        }
    ]
}

10.IAM group full access 

{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": [
                "iam:GetPolicyVersion",
                "iam:DeactivateMFADevice",
                "iam:CreateServiceSpecificCredential",
                "iam:DeleteAccessKey",
                "iam:ListRoleTags",
                "iam:DeleteGroup",
                "iam:UpdateOpenIDConnectProviderThumbprint",
                "iam:RemoveRoleFromInstanceProfile",
                "iam:UpdateGroup",
                "iam:CreateRole",
                "iam:ListServiceSpecificCredentials",
                "iam:ListSigningCertificates",
                "iam:AddRoleToInstanceProfile",
                "iam:CreateLoginProfile",
                "iam:ListSSHPublicKeys",
                "iam:SimulatePrincipalPolicy",
                "iam:ListAttachedRolePolicies",
                "iam:ListOpenIDConnectProviderTags",
                "iam:ListSAMLProviderTags",
                "iam:DeleteServerCertificate",
                "iam:UploadSSHPublicKey",
                "iam:ListRolePolicies",
                "iam:DeleteOpenIDConnectProvider",
                "iam:ChangePassword",
                "iam:UpdateLoginProfile",
                "iam:UpdateServiceSpecificCredential",
                "iam:GetServerCertificate",
                "iam:GetRole",
                "iam:CreateGroup",
                "iam:GetPolicy",
                "iam:RemoveClientIDFromOpenIDConnectProvider",
                "iam:UpdateUser",
                "iam:GetAccessKeyLastUsed",
                "iam:ListEntitiesForPolicy",
                "iam:DeleteRole",
                "iam:UpdateRoleDescription",
                "iam:UpdateAccessKey",
                "iam:UpdateSSHPublicKey",
                "iam:UpdateServerCertificate",
                "iam:DeleteSigningCertificate",
                "iam:GetUserPolicy",
                "iam:ListGroupsForUser",
                "iam:DeleteServiceLinkedRole",
                "iam:GetGroupPolicy",
                "iam:GetOpenIDConnectProvider",
                "iam:GetRolePolicy",
                "iam:CreateInstanceProfile",
                "iam:ResetServiceSpecificCredential",
                "iam:DeleteSSHPublicKey",
                "iam:ListInstanceProfileTags",
                "iam:CreateVirtualMFADevice",
                "iam:CreateSAMLProvider",
                "iam:ListMFADevices",
                "iam:CreateUser",
                "iam:GetGroup",
                "iam:CreateAccessKey",
                "iam:GetContextKeysForPrincipalPolicy",
                "iam:GetServiceLinkedRoleDeletionStatus",
                "iam:ListInstanceProfilesForRole",
                "iam:PassRole",
                "iam:AddUserToGroup",
                "iam:RemoveUserFromGroup",
                "iam:GenerateOrganizationsAccessReport",
                "iam:EnableMFADevice",
                "iam:ResyncMFADevice",
                "iam:ListAttachedUserPolicies",
                "iam:ListAttachedGroupPolicies",
                "iam:ListPolicyTags",
                "iam:UpdateSAMLProvider",
                "iam:GetSAMLProvider",
                "iam:DeleteLoginProfile",
                "iam:ListAccessKeys",
                "iam:DeleteInstanceProfile",
                "iam:UploadSigningCertificate",
                "iam:GetInstanceProfile",
                "iam:ListGroupPolicies",
                "iam:GetSSHPublicKey",
                "iam:DeleteUser",
                "iam:ListUserPolicies",
                "iam:ListInstanceProfiles",
                "iam:CreateOpenIDConnectProvider",
                "iam:UploadServerCertificate",
                "iam:CreateServiceLinkedRole",
                "iam:ListPolicyVersions",
                "iam:DeleteVirtualMFADevice",
                "iam:ListServerCertificateTags",
                "iam:UpdateRole",
                "iam:GetUser",
                "iam:UpdateSigningCertificate",
                "iam:AddClientIDToOpenIDConnectProvider",
                "iam:ListMFADeviceTags",
                "iam:DeleteServiceSpecificCredential",
                "iam:GetLoginProfile",
                "iam:ListUserTags",
                "iam:DeleteSAMLProvider"
            ],
            "Resource": "arn:aws:iam::006570735867:group/New"
        },
        {
            "Sid": "VisualEditor1",
            "Effect": "Allow",
            "Action": [
                "iam:GenerateCredentialReport",
                "iam:GetAccountPasswordPolicy",
                "iam:GetServiceLastAccessedDetailsWithEntities",
                "iam:ListServerCertificates",
                "iam:GenerateServiceLastAccessedDetails",
                "iam:ListPoliciesGrantingServiceAccess",
                "iam:GetServiceLastAccessedDetails",
                "iam:ListVirtualMFADevices",
                "iam:GetOrganizationsAccessReport",
                "iam:SetSecurityTokenServicePreferences",
                "iam:SimulateCustomPolicy",
                "iam:CreateAccountAlias",
                "iam:GetAccountAuthorizationDetails",
                "iam:DeleteAccountAlias",
                "iam:GetCredentialReport",
                "iam:ListPolicies",
                "iam:ListSAMLProviders",
                "iam:ListRoles",
                "iam:GetContextKeysForCustomPolicy",
                "iam:UpdateAccountPasswordPolicy",
                "iam:ListOpenIDConnectProviders",
                "iam:ListAccountAliases",
                "iam:ListUsers",
                "iam:ListGroups",
                "iam:GetAccountSummary"
            ],
            "Resource": "*"
        }
    ]
}

