---
section: Contributing
title: Packages
sort_info: 150
---

There are two options for you to contribute packages to Rock:

 - make your package a part of Rock 'proper', i.e., of the Rock package set
 - create [your own package set](../autoproj/advanced/creating_pkg_set.html)

This page will describe the process for both options.

Add your package to Rock
------------------------

As a side note, it is important that you realize that your library can be
integrated into Rock _without any changes_ to your library. The Rock build system is designed for
that, as long as it follows widely-accepted standards (see for instance
the "Build System Behaviour" section of the [corresponding Rock
guidelines](http://rock.opendfki.de/wiki/WikiStart/Standards/RG4)). Even the
[manifest.xml file](../autoproj/advanced/manifest-xml.html), which is used to
describe the package, can be provided as part of the package set instead
of as part of the package itself.

The process to get a package into Rock is:

 - locally modify the Rock package set (in autoproj/remotes/rock) to define your
   package. The package should go in the libs.autobuild file if it is a library
   and in the orogen.autobuild file if it is an oroGen package.
 - commit these changes
 - [send these changes to the Rock developers](merge_changes_to_rock-core.html). Make sure that
   the purpose of the package(s) is clear.
 - at this point, there is the option of putting the source code within Rock's
   github projects. While it is not mandatory, it is the preferred option.
   The Rock developers will be in touch with you to discuss this (either through
   the [rock-users mailing list](http://www.dfki.de/mailman/cgi-bin/listinfo/rock-users) or through the merge request / ticket you created)

Publish your package set in Rock
--------------------------------

If you have integrated more than one package, and want to keep control over
these packages (i.e., you want them to appear to be a separate contribution from your
company / research institute), there is the possibility to submit a package set.
This package set will be added to Rock's default build configuration, and will
be integrated into the Rock package directory.

The process to submit a package set is:

 - send the link and description of the package set to the [rock-users mailing
   list](http://www.dfki.de/mailman/cgi-bin/listinfo/rock-users)
 - wait for a Rock developer to pick up on that

