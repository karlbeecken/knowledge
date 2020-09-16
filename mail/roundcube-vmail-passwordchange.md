---
layout: default
title: Roundcube passwordchange with vmail
---

Tested
{: .label .label-green }

# Configuring Roundcube to allow changing passwords in vmail

1. enable the _password_ plugin in Roundcube
2. change dir to your roundcube installation directory, e.g. `/var/www/roundcube`
3. copy the default config for _password_: `cp plugins/password/config.inc.php.dist plugins/password/config.inc.php`
4. change the value of `$['password_algorithm']` to `'dovecot'`
5. uncomment the `$config['password_dovecotpw']` line for dovecot-2.x and comment the line for dovecot-1.x
6. change the value of `$config['password_dovecotpw']` to `'/usr/bin/doveadm pw'`
7. change the value of `$config['password_dovecotpw_method']` to `SHA512-CRYPT`
8. set `$config['password_dovecotpw_with_method']` to `true`
9. in `$config['password_db_dsn']` insert the DSN of your vmail db/user, e.g. `'mysql://vmail:password1234@localhost/vmail'` _Note: the given user has to have write access to the vmail database_
10. set `$config['password_query']` `'UPDATE accounts SET password=%P WHERE username=%l AND domain=%d LIMIT 1'`

That's it! You should change the name of the database if you used an other name than `vmail`.
