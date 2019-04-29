# F-TICKS logger module

With this module your simpleSAMLphp IdP will be able to write statistical logs in F-TICKS format.

## Install

Go to modules directory, type the following command

`git clone https://github.com/sifulan-access-federation/ftickslogger.git`

`touch ftickslogger/enable`

## Usage

This is an Authentication Processing filter, so you are supposed to set it up in authproc.idp section, eg. in metadata/saml20-idp-hosted.php.

```php
	95 => array(
        'class' => 'ftickslogger:ftickslogger',
        'attributename' => 'uid',
        'secretsalt' => 'echo9ke8ttwjgekourb767hy2p8mygcqaqi1'
    ),
```

Where `attributename` is the principal of the user, and the `secretsalt` is a secret salt to hash the value of principal :)
