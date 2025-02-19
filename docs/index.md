---
title: FileSender Documentation
---

## FileSender project

FileSender is a web based application that allows authenticated users
to securely and easily send arbitrarily large files to other users.
Authentication of users is provided through [SimpleSAMLphp, supporting
SAML2, LDAP and RADIUS and
more](http://simplesamlphp.org/docs/stable/simplesamlphp-idp#section_2).
Users without an account can be sent an upload voucher by an
authenticated user. FileSender is developed to the requirements of the
higher education and research community.

The purpose of the software is to send a large file to someone, have
that file available for download for a certain number of downloads
and/or a certain amount of time, and after that automatically delete
the file. The software is not intended as a permanent file publishing
platform.

This is the home for Filesender documentation. For more information
about the project [please visit our homepage](http://filesender.org).

### Which version should you choose

There are 3 releases, of which 2 are maintained:

- Version 1 is an archived, older version of FileSender which is not maintained
- Version 2 is the current mainstream version with active feature developmet
- Version 3 is in development, with alpha releases. This version features a new UI

Version 3 and Version 2 should have the same functionality but version
3 uses Bootstrap to present a more modern UI. The uploaded files
storage handling is the same in version 2 and version 3. The database
schema is very similar between the two and should be identical at
specific release. For example, version 3.0alpha2 [explicitly
mentions](https://github.com/filesender/filesender/releases/tag/master3-filesender-3.0alpha2)
that it is feature compatible with 2.30. So you should be able to
direct 3.0alpha2 at the same uploaded files and database and have the
system function.

The version 2.x series is the recommended choice in late 2021. Perhaps
in 2022 version 3.x will become the recommended choice. The latest
version can be obtained from the [github releases
page](https://github.com/filesender/filesender/releases).

The release numbering for the 2.x series follows the
pattern 2.1, 2.2, 2.30 etc. Each of these releases builds on
version 2.0 adding bugfixes and features. Each new
release in the 2.x series will describe if database updates are needed
(most often by running a script) and if web page templates have been
updated in case you customize those on your site. If is intended that
you can migrate an active site to new releases with very minimal downtime.

The 1.6.x series is considered deprecated. It is still available
for those who have not upgraded to a 2.x installation: [1.6.1, released on December 30th 2015](https://downloads.filesender.org/filesender-1.6.1.tar.gz).

### Documentation

As of late 2021 the documentation for FileSender 3.x is the same as
that of the 2.x series. The same options are available in both
versions of FileSender and setup and configuration is the same. Both
FileSender 2.x and 3.x also share the same database schema and you
should be able to migrate a version from 2.x to 3.x retaining active
file uploads and all the information in the database.

Perhaps in 2022 FileSender 3.x will become the major release at which
point the documentation for 2.x will be cloned to a 3.x series.

Please see the [documentation for versions 2.x](http://docs.filesender.org/v2.0/).

### License

FileSender is released under the [BSD
license](http://opensource.org/licenses/BSD-3-Clause). It is open
source software and available for free.

### Availability and download

Visit the [Releases
page](https://github.com/filesender/filesender/releases) for details
about the general availability of the FileSender software.

### Feature Requests

Go to the [Issues](https://github.com/filesender/filesender/issues)
page if you have a feature you would like to see added to FileSender.

### Features

For a more detailed list of version 2.x features see the [v2.0 features page](v2.0/features/).
The functionality of the 3.x alpha release are the same as the 2.x features but a new Bootstrap
UI is used to present the site.

* light-weight server footprint, optimized for least possible dependencies
* share arbitrarily large files from standard desktop environments, no client-side deployment required
* WebCrypto backed End-to-End encryption of files using AES-CBC or AES-GCM modes.
* Native HTML5 and JavaScript UI with supported browsers. No plugins required.
* High-speed upload module with HTML5 uploads
* integrates with various authentication mechanisms using SimpleSAMLphp (SAML2, RADIUS, LDAP)
* upload guest vouchers to allow users without an account to upload a file. This can be restricted to only
  allow such uploads to be seen by the person who invited the guest.
* cancel / resume file uploads using the HTML5 File API in supported browsers
* resume an upload even after laptop sleep or from another machine with access to the same file.
* download files multiple times, from link with built-in password in auto-generated email, or directly from interface by authenticated user
* automatic deletion of shared files and issued vouchers after X amount of time, or manual deletion by authenticated user any time prior to expiry
* email notification each time a file is uploaded, downloaded or manually deleted, or a voucher is issued or manually deleted
* MyFiles provides overview lists of currently shared files * Overview list of unused issued guest vouchers
* resend download link emails to file recipients without re-uploading the file * add additional recipients to already uploaded files
* UTF8 support, supports all international character sets
* Multi-language support. Out-of-the-box FileSender supports Czech, Croatian, Dutch, English (Australian), Finnish, French, German, Hungarian, Italian, Norwegian (Bokmål), Serbian, Slovenian and Spanish. You can easily adapt relevant language labels to your local needs in an upgrade-friendly way, for example to localise the splash screen text. You can also easily modify which languages you make available to your users
* PDO-based multi-database support for PostgreSQL, MySQL and sqlite



### Requirements

Some storage, either MariaDB or PostgreSQL for database, either Apache
or nginx for web server, PHP and SimpleSamlPhp. Please see the
[installation](v2.0/install/) page for minimum version requirements
and advice.


