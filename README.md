Authored Timezone
=================

Authored Timezone allows you to specify a custom timezone for the 'Authored on'
field. This is useful when content is written in different timezones. Each piece
of content can display its authored/submitted/created date in the timezone from
which it was written. You can also, optionally, display the author's country in
the 'Submitted' information.

Notes
-----

This module implements `hook_preprocess_node()` to display the 'created' date in
the selected timezone. As such, it can be easily overwritten by other
modules/themes that also implement `hook_preprocess_node()`. If your dates
aren't being displayed in the correct timezone, make sure other modules/themes
on your site aren't overwriting this.

When the 'Submitted By' module is enabled, it takes over control of the display
of the created date, author, etc. Therefore, you'll need to manually swap any
instances of `[node:created]` with `[node:authored-timezone-date]` to see your
dates displayed in the correct timezone.  
Additionally, the 'Display author country' option will be disabled, and you'll
need to manually add the `[node:authored-timezone-country]` token to your byline
fields instead.

Installation
------------

- Install this module using the official Backdrop CMS instructions at
  https://backdropcms.org/guide/modules.

- Enable the Timezone option on the content type(s) of your choice and,
  optionally, display the author's country.

- Add/edit content. The timezone will default to your current location, but can
  be changed as desired.

Issues
------

Bugs and Feature requests should be reported in the Issue Queue:
https://github.com/backdrop-contrib/authored_timezone/issues.

Current Maintainers
-------------------

- Peter Anderson (https://github.com/BWPanda).

License
-------

This project is GPL v2 software. See the LICENSE.txt file in this directory for
complete text.

