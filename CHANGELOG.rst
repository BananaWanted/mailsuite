Changelog
=========

1.6.0
-----

- Remove copies of email headers from the root of the returned dictionary (still available under `headers`
- Store the HTML body in body in `body`, or the text body if an HTML body does not exist
- Store all body parts as a string in `raw_body`
- Only run `html2text` on HTML bodies
- Disable wrapping on markdown to make searching strings with Yara or other tools easier

1.5.4
-----

- Improve ``get_filename_safe_string()``

1.5.3
------

- Fix version numbering

1.5.2
-----

- Pin some dependency versions to avoid conflicts

  - ``six==1.13.0``
  - ``mail-parser==3.11.0``

1.5.1
-----

- Require ``mail-parser>=3.11.0`` ro avoid dependency problems

1.5.0
-----

- Add ``body_markdown`` to ``parse_email()`` results

1.4.0
-----

- Add ``headers_string`` to parsed output

1.3.1
-----

- Do not remove leading `/` from folder names

1.3.0
-----

- Set a configurable default IMAP timeout of 30 seconds
- Set a configurable maximum of 4 IMAP timeout retry attempts

1.2.1
-----

- Fix IMAP hierarchy separator parsing

1.2.0
-----

- Add support for sending emails with custom message headers
- Add ``parsedmarc.utils.create_email`` function

1.1.1
-----

- Fix error when sending email with no attachments
- Correct ``mailsuite.__version__``

1.1.0
-----

- Always use ``/`` as the folder hierarchy separator, and convert to the
  server's hierarchy separator in the background
- Always remove folder name characters that conflict with the server's
  hierarchy separators
- Prepend the namespace to the folder path when required

1.0.0
-----

- Initial release
