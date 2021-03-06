Changelog
=========

v0.2.1
------

*Released: 2016-06-28*

- Support singular and plural versions of the ``item.package`` parameter, as
  well as both string an YAML list variants. [drybjed]

- Update list of Ubuntu releases. [drybjed]

- Add support for ``item.state`` parameter and deprecate the alternatives.
  [drybjed]

v0.2.0
------

*Released: 2016-06-14*

- Changed variable namespace from ``apt_preferences_`` to ``apt_preferences__``.
  ``apt_preferences_[^_]`` variables are hereby deprecated but are currently
  still supported to allow a soft migration.

  You might need to update your inventory. This oneliner might come in handy to
  do this:

  .. code:: shell

     git ls-files -z | xargs --null -I '{}' find '{}' -type f -print0 | xargs --null sed --in-place --regexp-extended 's/\<(apt_preferences)_([^_])/\1__\2/g;'

  [ypid]


- Added :any:`apt_preferences__preset_list` for advanced users. [ypid]

- Use marker levels in vim markers to eliminate empty spaces. [drybjed]

v0.1.3
------

*Released: 2016-02-07*

- Fix deprecation warnings in Ansible 2.1.0. [drybjed]

v0.1.2
------

*Released: 2015-11-13*

- Support ``item.role`` as an alternative parameter. [drybjed]

- Add support for ``item.when`` parameter, which introduces a way to
  enable/disable a particular pin conditionally. [drybjed]

- Check ``item.delete`` explicitly as a boolean. [drybjed]

v0.1.1
------

*Released: 2015-10-15*

- Fixed documentation spelling. [ypid]

v0.1.0
------

*Released: 2015-10-15*

- Add Changelog. [drybjed]

- Clean up documentation. [drybjed]

