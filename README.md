# mailserver
OpenBSD mailserver

* * *

## Features

- Multiple domains support with only one admin
- Work on OpenBSD 6.3
- Maildir format
- MTA : OpenSMTPD
- DKIM support
- Antispam : spamd with spf walk
- MDA : Dovecot
- POP3 / IMAP Protocol
- Manage Sieve
- MUA : Roundcubemail
- Web Server : httpd
- Let's Encrypt certificate 
- Packet Filter
- CLI to manage domains|users|spam, monitoring (cpu, mem, free space, used space per user)
- Installer (a mix of shell scripts)
- Full comments on any scripts and configuration files
- Documentation (backup & restore your server)

## Installation

Just run:

    cd /var
    git clone https://github.com/openbsdjumpstart/mailserver
    cd mailserver && ./bin/deploy

## Contributing

First off, thank you for considering contributing to this project.

We love to receive contributions to the project. There are many ways to
contribute, from improving the documentation, submitting bug reports and
feature requests or writing code which can be incorporated into the
project itself.

If you want to contribute to this project please read our suggestions in
the file [CODING.md](CODING.md). Following these guidelines helps that your
contributed code will fit in the project nicely.

## License

The contents of this repository are covered under the [ISC License](LICENSE).

