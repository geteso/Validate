### Validate
Automatically validates new user accounts.

[![License](https://img.shields.io/github/license/geteso/Validate)]()
[![Version](https://img.shields.io/github/v/release/geteso/Validate?include_prereleases)]()
[![PHP Version Support](https://img.shields.io/badge/php-%5E5.6.4-blue)]()

### Validating unregistered accounts
If an account has already signed up (but you have not yet configured your mailserver), you may validate unregistered accounts manually with an `UPDATE` statement (use at your own risk).
```sql
mysql -u <mysqlUser> -p <mysqlPass>
USE <mysqlDB>
UPDATE <tablePrefix>members SET account='member' WHERE memberId=<memberId>
```

Know that this plugin does not exempt you from configuring your mailserver, as it is still necessary for users to receive mail notifications.