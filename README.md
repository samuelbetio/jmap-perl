Perl JMAP Proxy Server
======================

This is a simple implementation of a proxy server for the JMAP protocol as
specified at http://jmap.io/

At the backend, it talks to IMAP and SMTP servers to allow placing a JMAP
interface on top of a legacy mail system.

For efficiency reasons, this initial implementation requires that all servers
support the CONDSTORE extension, (RFC4551/RFC7162).

A separate backend for Gmail is provided, because Gmail has native server-side
thread support, meaning that threading does not need to be calculated locally.
