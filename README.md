# Awsidentity-Center
# IAM Identity Center – Secure AWS Account Management

This project shows how to secure many AWS accounts with **IAM Identity Center** (the old name was AWS SSO).

## Why it is important

Using **IAM Identity Center** is a good practice because it keeps your AWS environment **safe and simple**:

* You give each person only the access they need (least privilege).
* One portal controls many AWS accounts, so you work faster.
* You can reuse your company login (Azure AD, Okta, etc.) and keep MFA in one place.
* All actions are written in CloudTrail, so audits are easy.

This limits human error, saves time, and follows AWS security rules.

## Diagram

<img width="1536" height="1024" alt="diagram-iam-identity-center png" src="https://github.com/user-attachments/assets/dc143de7-dace-4873-9b7d-3cb78ff2ac05" />

### What happens

1. **Julia** is a member of the **Billing** group.
2. She signs in once in the **SSO Portal**.
3. IAM Identity Center gives her a permission set that allows only billing pages.
4. The same session works in every AWS account: General, Production, Development.
5. An external identity source (for example Azure AD) can manage users and groups.

### Why it is good

| Good practice                  | Reason                        |
| ------------------------------ | ----------------------------- |
| Least privilege                | Users see only what they need |
| Groups, not single users       | Easier to add/remove people   |
| Central logs with CloudTrail   | Easy audit                    |
| MFA at IdP                     | Extra security                |
| Regular review (every 90 days) | Clean up old access           |

### How to start

```bash
# 1. Create groups and permission sets in IAM Identity Center
# 2. Attach accounts to the groups
# 3. Connect your IdP (Azure AD, Okta, etc.)
# 4. Test the SSO portal
```

