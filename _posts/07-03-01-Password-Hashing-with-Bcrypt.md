---
isChild: true
---

## Password Hashing with Bcrypt {#password_hashing_with_bcrypt_title}

Eventually everyone builds a PHP application that relies on user login. Usernames and (hashed) passwords are stored in a database and later used to authenticate users upon login.

It is important that you properly _hash_ passwords that are stored in a database. If passwords are not hashed, and your database is hacked or accessed by an unauthorized third-party, all user accounts are now compromised.

**Hash passwords with Bcrypt**. It's super simple, and (for all intents and purposes) Bcrypt makes it impossible for someone to reverse-engineer the plain-text version of a password should the database be compromised.

There are several Bcrypt libraries for PHP that you may use.

* [Read "How to Safely Store a Password" by Coda Hale][3]
* [Use Bcrypt with PHPass][4]

[3]: http://codahale.com/how-to-safely-store-a-password/
[4]: http://www.openwall.com/phpass/
