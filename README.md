# Disclaimer

## You should really probably be using SwiftMailer - [ [Github](https://github.com/swiftmailer/swiftmailer) | [Packagist](https://packagist.org/packages/swiftmailer/swiftmailer) ] instead of this.


![PHPMailer](https://raw.github.com/PHPMailer/PHPMailer/master/examples/images/phpmailer.png)

# PHPMailerNS - The namespaced "[PHPMailer](https://github.com/PHPMailer/)"

## [PHPMailerNS](https://github.com/Seanmcn/PHPMailerNS) Class Features

- Namespace Support
- Compatible with PHP 5.3 and later

## [PHPMailer](https://github.com/PHPMailer/) Class Features

- Probably the world's most popular code for sending email from PHP!
- Used by many open-source projects: Wordpress, Drupal, 1CRM, SugarCRM, Yii, Joomla! and many more
- Integrated SMTP support - send without a local mail server
- Send emails with multiple TOs, CCs, BCCs and REPLY-TOs
- Multipart/alternative emails for mail clients that do not read HTML email
- Support for UTF-8 content and 8bit, base64, binary, and quoted-printable encodings
- SMTP authentication with LOGIN, PLAIN, NTLM and CRAM-MD5 mechanisms over SSL and TLS transports
- Error messages in 47 languages!
- DKIM and S/MIME signing support
- Compatible with PHP 5.0 and later
- Much more!

## License

This software is distributed under the [LGPL 2.1](http://www.gnu.org/licenses/lgpl-2.1.html) license. Please read LICENSE for information on the
software availability and distribution.

## Installation & loading

PHPMailerNS is available via [Composer/Packagist](https://packagist.org/packages/phpmailerNS/phpmailerNS) (using semantic versioning), so just add this line to your `composer.json` file:

    "phpmailerns/phpmailerns": "~1.5"


PHPMailerNS only supports PHP 5.3 and up.


## A Simple Example

```php
<?php
use PHPMailerNS\Mailer;

$mail = new Mailer;

//$mail->SMTPDebug = 3;                               // Enable verbose debug output

$mail->isSMTP();                                      // Set mailer to use SMTP
$mail->Host = 'smtp1.example.com;smtp2.example.com';  // Specify main and backup SMTP servers
$mail->SMTPAuth = true;                               // Enable SMTP authentication
$mail->Username = 'user@example.com';                 // SMTP username
$mail->Password = 'secret';                           // SMTP password
$mail->SMTPSecure = 'tls';                            // Enable TLS encryption, `ssl` also accepted
$mail->Port = 587;                                    // TCP port to connect to

$mail->From = 'from@example.com';
$mail->FromName = 'Mailer';
$mail->addAddress('joe@example.net', 'Joe User');     // Add a recipient
$mail->addAddress('ellen@example.com');               // Name is optional
$mail->addReplyTo('info@example.com', 'Information');
$mail->addCC('cc@example.com');
$mail->addBCC('bcc@example.com');

$mail->addAttachment('/var/tmp/file.tar.gz');         // Add attachments
$mail->addAttachment('/tmp/image.jpg', 'new.jpg');    // Optional name
$mail->isHTML(true);                                  // Set email format to HTML

$mail->Subject = 'Here is the subject';
$mail->Body    = 'This is the HTML message body <b>in bold!</b>';
$mail->AltBody = 'This is the body in plain text for non-HTML mail clients';

if(!$mail->send()) {
    echo 'Message could not be sent.';
    echo 'Mailer Error: ' . $mail->ErrorInfo;
} else {
    echo 'Message has been sent';
}
```


That's it. You should now be ready to use PHPMailerNS!

## Localization
[PHPMailer](https://github.com/PHPMailer/) defaults to English, but in the [language](language/) folder you'll find numerous (46 at the time of writing!) translations for [PHPMailer](https://github.com/PHPMailer/) error messages that you may encounter. Their file names contain [ISO 639-1](http://en.wikipedia.org/wiki/ISO_639-1) language code for the translations, for example `fr` for French. To specify a language, you need to tell [PHPMailer](https://github.com/PHPMailer/) which one to use, like this:

```php
// To load the French version
$mail->setLanguage('fr', '/optional/path/to/language/directory/');
```


## Documentation

Examples of how to use [PHPMailer](https://github.com/PHPMailer/) for common scenarios can be found in the [examples](examples/) folder of the [PHPMailer](https://github.com/PHPMailer/) repository. If you're looking for a good starting point, we recommend you start with [the gmail example](examples/gmail.phps).

There are tips and a troubleshooting guide in the [GitHub wiki](https://github.com/PHPMailer/PHPMailer/wiki). If you're having trouble, this should be the first place you look as it's the most frequently updated.

Complete generated API documentation is [available online](http://phpmailer.github.io/PHPMailer/).

You'll find some basic user-level docs in the [docs](docs/) folder of the [PHPMailer](https://github.com/PHPMailer/) repo, and you can generate complete API-level documentation using the [generatedocs.sh](docs/generatedocs.sh) shell script in the docs folder, though you'll need to install [PHPDocumentor](http://www.phpdoc.org) first. You may find [the unit tests](test/phpmailerTest.php) a good source of how to do various operations such as encryption.

If the documentation doesn't cover what you need, search the [many questions on StackOverflow](http://stackoverflow.com/questions/tagged/phpmailer), and before you ask a question about "SMTP Error: Could not connect to SMTP host.", [read the troubleshooting guide](https://github.com/PHPMailer/PHPMailer/wiki/Troubleshooting).

## Contributing

Please submit bug reports, suggestions and pull requests for PHPMailer to the [GitHub issue tracker](https://github.com/PHPMailer/PHPMailer/issues).

## Changelog

See [changelog](changelog.md).
