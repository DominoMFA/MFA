# MFA

the mfa.nsf is a solution that enable MFA (multi factor authentication) for Domino.

# Setup

## MFA.NSF

- copy mfa.nsf database to Domino data folder (it goes with predefined setup of documents, don't remove them, they are part of a solution).
- sign mfa.nsf with your server id
- create Config document
- you need to properly configure iMessageURL field (it's a service that sends SMS), see details https://github.com/Domino-iMessageSMS/iMessageSMS
- in the view Template press button 'Update Login Form' (that should generate Login form inside of MFA.nsf, which is mandatory by domcfg.nsf).
- replicate mfa.nsf to other Domino servers if needed (also configure connection/replication documents), so data are synchronized as fast as possible.

## DOMCFG

- create domcfg.nsf database and point it to use "Login" form in "mfa.nsf" 
