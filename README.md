﻿[MvcAccount](http://maxtoroq.github.io/MvcAccount/) — Authentication and Account Management plugin for ASP.NET MVC
==================================================================================================================
MvcAccount is a substitute for [MembershipProvider](http://msdn.microsoft.com/library/system.web.security.membershipprovider) designed for ASP.NET MVC, that provides more features and the ability to store username/password and other related data in your own database.

Functions
---------
- **Sign In/Out**: With account lock out after max. invalid attempts.
- **Reset Password**: Sends email with link to enter new password.
- **Change Password**: User must sign in first.
- **Change Email**: With optional verification (sends email with link).

Password encryption methods
---------------------------
- **None**: Passwords are stored in clear text.
- **PBKDF2** ([Recommended](http://brockallen.com/2012/10/19/password-management-made-easy-in-asp-net-with-the-crypto-api/)): Passwords are hashed with the RFC 2898 algorithm.
  Implemented by [Crypto](http://msdn.microsoft.com/library/system.web.helpers.crypto), also used by [SimpleMembershipProvider](http://msdn.microsoft.com/library/webmatrix.webdata.simplemembershipprovider).
- **SHA1**: Passwords are encrypted one-way using the SHA1 hashing algorithm (reuses *SqlMembershipProvider* implementation).
- **MachineKey**: Passwords are encrypted using the encryption settings determined by the machineKey element configuration (reuses *SqlMembershipProvider* implementation).
- **Custom**: Provide your own implementation.

Integration
-----------
- **MembershipProvider**: Although MvcAccount is a substitute for *MembershipProvider* there are many components out there that work against this API, so MvcAccount also provides an implementation. The only functions currently implemented are:
  - **ValidateUser** (useful if your application implements other functions that require username/password verification).
  - **GetUser** (all overloads, this allows you to get user information from your application without a direct dependency on MvcAccount).
- **Bootstrap**: Views use Bootstrap markup and classes (optional, you are not required to use Bootstrap).

Localization
------------
MvcAccount is fully localized in the following languages:

- English (en)
- Spanish (es)
- Finnish (fi)
- Portuguese (pt)

Not included
------------
MvcAccount doesn't provide the following functionality:

- Anything related with roles or claims.
- External login providers (OAuth, OpenID).

Resources
---------
- [Documentation](docs/README.md)
- [Ask for help](https://github.com/maxtoroq/MvcAccount/issues?q=is%3Aissue+label%3Aquestion)
- [Report an issue](https://github.com/maxtoroq/MvcAccount/issues)

[![Donate](https://www.paypalobjects.com/en_US/i/btn/btn_donate_SM.gif)](http://maxtoroq.github.io/p/donate.html)