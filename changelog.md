# ChangeLog - PHPMailerNamespaced

## Version 1.0 (May 6th 2015)
* Converted the PHPMailer to use namespaces.

# ChangeLog - PHPMailer

* Don't switch to quoted-printable for long lines if already using base64

## Version 5.2.10 (May 4th 2015)
* Add custom header getter
* Use `application/javascript` for .js attachments
* Improve RFC2821 compliance for timelimits, especially for end-of-data
* Add Azerbaijani translations (Thanks to @mirjalal)
* Minor code cleanup for robustness
* Add Indonesian translations (Thanks to @ceceprawiro)
* Avoid `error_log` Debugoutput naming clash
* Add ability to parse server capabilities in response to EHLO (useful for SendGrid etc)
* Amended default values for WordWrap to match RFC
* Remove html2text converter class (has incompatible license)
* Provide new mechanism for injecting html to text converters
* Improve pointers to docs and support in README
* Add example file upload script
* Refactor and major cleanup of EasyPeasyICS, now a lot more usable
* Make set() method simpler and more reliable
* Add Malay translation (Thanks to @nawawi)
* Add Bulgarian translation (Thanks to @mialy)
* Add Armenian translation (Thanks to Hrayr Grigoryan)
* Add Slovenian translation (Thanks to Klemen Tušar)
* More efficient word wrapping
* Add support for S/MIME signing with additional CA certificate (thanks to @IgitBuh)
* Fix incorrect MIME structure when using S/MIME signing and isMail() (#372)
* Improved checks and error messages for missing extensions
* Store and report SMTP errors more consistently
* Add MIME multipart preamble for better Outlook compatibility
* Enable TLS encryption automatically if the server offers it
* Provide detailed errors when individual recipients fail
* Report more errors when connecting
* Add extras classes to composer classmap
* Expose stream_context_create options via new SMTPOptions property
* Automatic encoding switch to quoted-printable if message lines are too long
* Add Korean translation (Thanks to @ChalkPE)
* Provide a pointer to troubleshooting docs on SMTP connection failure

