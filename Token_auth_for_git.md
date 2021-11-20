
Token authentication requirements for Git operations | The GitHub Blog 
 
Matthew Langlois
In July 2020, we announced our intent to require the use of token-based authentication (for example, a personal access, OAuth, or GitHub App installation token) for all authenticated Git operations. Beginning August 13, 2021, we will no longer accept account passwords when authenticating Git operations on GitHub.com.
Workflows affected
Command line Git access
Desktop applications using Git (GitHub Desktop is unaffected)
Any apps/services that access Git repositories on GitHub.com directly using your password
The following customers remain unaffected by this change:
If you have two-factor authentication enabled for your account, you are already required to use token- or SSH-based authentication.
If you use GitHub Enterprise Server, we have not announced any changes to our on-premises offering.
If you maintain a GitHub App, GitHub Apps do not support password authentication.
Background
We described our motivation as we announced similar changes to authenticating with the API as follows:
In recent years, GitHub customers have benefited from a number of security enhancements to GitHub.com, such as two-factor authentication, sign-in alerts, verified devices, preventing the use of compromised passwords, and WebAuthn support. These features make it more difficult for an attacker to take a password that’s been reused across multiple websites and use it to try to gain access to your GitHub account. Despite these improvements, for historical reasons customers without two-factor authentication enabled have been able to continue to authenticate Git and API operations using only their GitHub username and password.
Beginning August 13, 2021, we will no longer accept account passwords when authenticating Git operations and will require the use of token-based authentication, such as a personal access token (for developers) or an OAuth or GitHub App installation token (for integrators) for all authenticated Git operations on GitHub.com. You may also continue using SSH keys where you prefer.
Tokens offer a number of security benefits over password-based authentication:
1. Unique – tokens are specific to GitHub and can be generated per use or per device
2. Revocable – tokens can can be individually revoked at any time without needing to update unaffected credentials
3. Limited – tokens can be narrowly scoped to allow only the access necessary for the use case
4. Random – tokens are not subject to the types of dictionary or brute force attempts that simpler passwords that you need to remember or enter regularly might be
What you need to do today
For developers, if you are using a password to authenticate Git operations with GitHub.com today, you must begin using a personal access token over HTTPS (recommended) or SSH key by August 13, 2021, to avoid disruption. If you receive a warning that you are using an outdated third-party integration, you should update your client to the latest version.
For integrators, you must authenticate integrations using the web or device authorization flows by August 13, 2021, to avoid disruption. For more information, see Authorizing OAuth Apps and the announcement on the developer blog.
Enabling two-factor authentication
If you would like to ensure that your account does not allow password-based authentication, you can enable two-factor authentication for your account today. This will require you to use a personal access token for all authenticated operations via Git and third-party integrations.
June 30 and July 28, 2021 – Token (or SSH key) authentication will be temporarily required for all Git operations to encourage affected customers to update their authentication method (see below).
August 13, 2021 – Token (or SSH key) authentication will be required for all authenticated Git operations.
If you have any questions, please see the related API password authentication blog post, learn more about keeping your account secure, or contact GitHub Support. Need a security key? Head over to the GitHub Shop.
