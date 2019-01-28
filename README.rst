RHOSP Git Hooks
===============

Some `git hooks`__ to work around common issues with our internal `dist-git`__
branches for `RHOSP`__. If you don't work on my team, these probably aren't of
interest to you.

__ https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks
__ https://www.rdoproject.org/documentation/intro-packaging/#distgit---where-the-spec-file-lives
__ https://www.redhat.com/en/technologies/linux-platforms/openstack-platform

Installation
------------

There are two hooks provided: ``pre-push`` and ``pre-receive``. The
``pre-receive`` one is server-side (and currently unused) so you want the
``pre-push`` hook. To install this, simply paste it into the ``.git/hooks``
directory for your local repository and make it executable. For example::

    $ cp pre-push ../openstack-nova/.git/hooks
    $ chmod +x ../openstack-nova/.git/hooks
