# À vous de jouer !

- Installez successivement les paquets `tree`, `git` et `nmap` sur toutes les cibles.

tree

```sh
ansible all -m package -a "name=tree state=present"
```

```
debian | CHANGED => {
    "cache_update_time": 1761245363,
    "cache_updated": false,
    "changed": true,
    "stderr": "",
    "stderr_lines": [],
    "stdout": "Reading package lists...\nBuilding dependency tree...\nReading state information...\nThe following NEW packages will be installed:\n  tree\n0 upgraded, 1 newly installed, 0 to remove and 0 not upgraded.\nNeed to get 52.5 kB of archives.\nAfter this operation, 116 kB of additional disk space will be used.\nGet:1 http://httpredir.debian.org/debian bookworm/main amd64 tree amd64 2.1.0-1 [52.5 kB]\nFetched 52.5 kB in 3s (20.8 kB/s)\nSelecting previously unselected package tree.\r\n(Reading database ... \r(Reading database ... 5%\r(Reading database ... 10%\r(Reading database ... 15%\r(Reading database ... 20%\r(Reading database ... 25%\r(Reading database ... 30%\r(Reading database ... 35%\r(Reading database ... 40%\r(Reading database ... 45%\r(Reading database ... 50%\r(Reading database ... 55%\r(Reading database ... 60%\r(Reading database ... 65%\r(Reading database ... 70%\r(Reading database ... 75%\r(Reading database ... 80%\r(Reading database ... 85%\r(Reading database ... 90%\r(Reading database ... 95%\r(Reading database ... 100%\r(Reading database ... 34138 files and directories currently installed.)\r\nPreparing to unpack .../tree_2.1.0-1_amd64.deb ...\r\nUnpacking tree (2.1.0-1) ...\r\nSetting up tree (2.1.0-1) ...\r\nProcessing triggers for man-db (2.11.2-2) ...\r\n",
    "stdout_lines": [
        "Reading package lists...",
        "Building dependency tree...",
        "Reading state information...",
        "The following NEW packages will be installed:",
        "  tree",
        "0 upgraded, 1 newly installed, 0 to remove and 0 not upgraded.",
        "Need to get 52.5 kB of archives.",
        "After this operation, 116 kB of additional disk space will be used.",
        "Get:1 http://httpredir.debian.org/debian bookworm/main amd64 tree amd64 2.1.0-1 [52.5 kB]",
        "Fetched 52.5 kB in 3s (20.8 kB/s)",
        "Selecting previously unselected package tree.",
        "(Reading database ... ",
        "(Reading database ... 5%",
        "(Reading database ... 10%",
        "(Reading database ... 15%",
        "(Reading database ... 20%",
        "(Reading database ... 25%",
        "(Reading database ... 30%",
        "(Reading database ... 35%",
        "(Reading database ... 40%",
        "(Reading database ... 45%",
        "(Reading database ... 50%",
        "(Reading database ... 55%",
        "(Reading database ... 60%",
        "(Reading database ... 65%",
        "(Reading database ... 70%",
        "(Reading database ... 75%",
        "(Reading database ... 80%",
        "(Reading database ... 85%",
        "(Reading database ... 90%",
        "(Reading database ... 95%",
        "(Reading database ... 100%",
        "(Reading database ... 34138 files and directories currently installed.)",
        "Preparing to unpack .../tree_2.1.0-1_amd64.deb ...",
        "Unpacking tree (2.1.0-1) ...",
        "Setting up tree (2.1.0-1) ...",
        "Processing triggers for man-db (2.11.2-2) ..."
    ]
}
rocky | SUCCESS => {
    "changed": false,
    "msg": "Nothing to do",
    "rc": 0,
    "results": []
}
suse | CHANGED => {
    "changed": true,
    "cmd": [
        "/usr/bin/zypper",
        "--quiet",
        "--non-interactive",
        "--xmlout",
        "install",
        "--type",
        "package",
        "--auto-agree-with-licenses",
        "--no-recommends",
        "--",
        "+tree"
    ],
    "name": [
        "tree"
    ],
    "rc": 0,
    "state": "present",
    "stderr": "",
    "stderr_lines": [],
    "stdout": "<?xml version='1.0'?>\n<stream>\n<install-summary download-size=\"56772\" space-usage-diff=\"116508\" space-usage-installed=\"116508\" space-usage-removed=\"0\" packages-to-change=\"1\" need-restart=\"0\" need-reboot=\"0\">\n<to-install>\n<solvable type=\"package\" name=\"tree\" edition=\"1.7.0-150000.3.2.1\" arch=\"x86_64\" repository=\"repo-sle-update\" summary=\"File listing as a tree\">\n<description>Tree is a recursive directory listing command that produces a depth\nindented listing of files, which is colorized ala dircolors if the\nLS_COLORS environment variable is set and output is to tty.</description></solvable>\n</to-install>\n</install-summary>\n<prompt id=\"0\">\n<text>Backend:  classic_rpmtrans\nContinue?</text>\n<option default=\"1\" value=\"y\" desc=\"Yes, accept the summary and proceed with installation/removal of packages.\"/>\n<option value=\"n\" desc=\"No, cancel the operation.\"/>\n<option value=\"v\" desc=\"Toggle display of package versions.\"/>\n<option value=\"a\" desc=\"Toggle display of package architectures.\"/>\n<option value=\"r\" desc=\"Toggle display of repositories from which the packages will be installed.\"/>\n<option value=\"m\" desc=\"Toggle display of package vendor names.\"/>\n<option value=\"d\" desc=\"Toggle between showing all details and as few details as possible.\"/>\n<option value=\"g\" desc=\"View the summary in pager.\"/>\n</prompt>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/tree-1.7.0-150000.3.2.1.x86_64.rpm\" percent=\"-1\" rate=\"-1\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/tree-1.7.0-150000.3.2.1.x86_64.rpm\" percent=\"0\" rate=\"0\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/tree-1.7.0-150000.3.2.1.x86_64.rpm\" percent=\"96\" rate=\"54764\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/tree-1.7.0-150000.3.2.1.x86_64.rpm\" rate=\"54764\" done=\"1\"/>\n</stream>\n",
    "stdout_lines": [
        "<?xml version='1.0'?>",
        "<stream>",
        "<install-summary download-size=\"56772\" space-usage-diff=\"116508\" space-usage-installed=\"116508\" space-usage-removed=\"0\" packages-to-change=\"1\" need-restart=\"0\" need-reboot=\"0\">",
        "<to-install>",
        "<solvable type=\"package\" name=\"tree\" edition=\"1.7.0-150000.3.2.1\" arch=\"x86_64\" repository=\"repo-sle-update\" summary=\"File listing as a tree\">",
        "<description>Tree is a recursive directory listing command that produces a depth",
        "indented listing of files, which is colorized ala dircolors if the",
        "LS_COLORS environment variable is set and output is to tty.</description></solvable>",
        "</to-install>",
        "</install-summary>",
        "<prompt id=\"0\">",
        "<text>Backend:  classic_rpmtrans",
        "Continue?</text>",
        "<option default=\"1\" value=\"y\" desc=\"Yes, accept the summary and proceed with installation/removal of packages.\"/>",
        "<option value=\"n\" desc=\"No, cancel the operation.\"/>",
        "<option value=\"v\" desc=\"Toggle display of package versions.\"/>",
        "<option value=\"a\" desc=\"Toggle display of package architectures.\"/>",
        "<option value=\"r\" desc=\"Toggle display of repositories from which the packages will be installed.\"/>",
        "<option value=\"m\" desc=\"Toggle display of package vendor names.\"/>",
        "<option value=\"d\" desc=\"Toggle between showing all details and as few details as possible.\"/>",
        "<option value=\"g\" desc=\"View the summary in pager.\"/>",
        "</prompt>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/tree-1.7.0-150000.3.2.1.x86_64.rpm\" percent=\"-1\" rate=\"-1\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/tree-1.7.0-150000.3.2.1.x86_64.rpm\" percent=\"0\" rate=\"0\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/tree-1.7.0-150000.3.2.1.x86_64.rpm\" percent=\"96\" rate=\"54764\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/tree-1.7.0-150000.3.2.1.x86_64.rpm\" rate=\"54764\" done=\"1\"/>",
        "</stream>"
    ],
    "update_cache": false
}
```

```sh
ansible all -m package -a "name=tree state=present"
```

```
rocky | SUCCESS => {
    "changed": false,
    "msg": "Nothing to do",
    "rc": 0,
    "results": []
}
debian | SUCCESS => {
    "cache_update_time": 1761245363,
    "cache_updated": false,
    "changed": false
}
suse | SUCCESS => {
    "changed": false,
    "name": [
        "tree"
    ],
    "rc": 0,
    "state": "present",
    "update_cache": false
}
```

git

```sh
ansible all -m package -a "name=git state=present"
```

```
rocky | CHANGED => {
    "changed": true,
    "msg": "",
    "rc": 0,
    "results": [
        "Installed: perl-Error-1:0.17029-7.el9.noarch",
        "Installed: perl-TermReadKey-2.38-11.el9.x86_64",
        "Installed: perl-lib-0.65-481.1.el9_6.x86_64",
        "Installed: git-core-2.47.3-1.el9_6.x86_64",
        "Installed: perl-File-Find-1.37-481.1.el9_6.noarch",
        "Installed: perl-Git-2.47.3-1.el9_6.noarch",
        "Installed: git-core-doc-2.47.3-1.el9_6.noarch",
        "Installed: git-2.47.3-1.el9_6.x86_64",
        "Installed: perl-DynaLoader-1.47-481.1.el9_6.x86_64"
    ]
}
suse | CHANGED => {
    "changed": true,
    "cmd": [
        "/usr/bin/zypper",
        "--quiet",
        "--non-interactive",
        "--xmlout",
        "install",
        "--type",
        "package",
        "--auto-agree-with-licenses",
        "--no-recommends",
        "--",
        "+git"
    ],
    "name": [
        "git"
    ],
    "rc": 0,
    "state": "present",
    "stderr": "",
    "stderr_lines": [],
    "stdout": "<?xml version='1.0'?>\n<stream>\n<install-summary download-size=\"6678364\" space-usage-diff=\"35905368\" space-usage-installed=\"35905368\" space-usage-removed=\"0\" packages-to-change=\"5\" need-restart=\"0\" need-reboot=\"0\">\n<to-install>\n<solvable type=\"package\" name=\"git\" edition=\"2.51.0-150600.3.12.1\" arch=\"x86_64\" repository=\"repo-sle-update\" summary=\"Fast, scalable, distributed revision control system\">\n<description>Git is a fast, scalable, distributed revision control system with an\nunusually rich command set that provides both high-level operations and\nfull access to internals.\n\nThis package itself only provides the README of git but with the\npackages it requires, it brings you a complete Git environment\nincluding GTK and email interfaces and tools for importing source code\nrepositories from other revision control systems such as subversion,\nCVS, and GNU arch.</description></solvable>\n<solvable type=\"package\" name=\"git-core\" edition=\"2.51.0-150600.3.12.1\" arch=\"x86_64\" repository=\"repo-sle-update\" summary=\"Core git tools\">\n<description>Git is a fast, scalable, distributed revision control system with an\nunusually rich command set that provides both high-level operations and\nfull access to internals.\n\nThese are the core tools with minimal dependencies.</description></solvable>\n<solvable type=\"package\" name=\"libsha1detectcoll1\" edition=\"1.0.3-2.18\" arch=\"x86_64\" repository=\"openSUSE-Leap-15.6-1\" summary=\"Library that can detect SHA-1 collisions\">\n<description>This library was designed as near drop-in replacements for other sha1sum\nimplementations. It will compute the SHA-1 hash of any given file and additionally\nwill detect cryptanalytic collision attacks against SHA-1 present in each file.\nIt is very fast and takes less than twice the amount of time as regular SHA-1.</description></solvable>\n<solvable type=\"package\" name=\"perl-Error\" edition=\"0.17025-1.20\" arch=\"noarch\" repository=\"openSUSE-Leap-15.6-1\" summary=\"Error/exception handling in an OO-ish way\">\n<description>The &apos;Error&apos; package provides two interfaces. Firstly &apos;Error&apos; provides a\nprocedural interface to exception handling. Secondly &apos;Error&apos; is a base\nclass for errors/exceptions that can either be thrown, for subsequent\ncatch, or can simply be recorded.\n\nErrors in the class &apos;Error&apos; should not be thrown directly, but the user\nshould throw errors from a sub-class of &apos;Error&apos;.</description></solvable>\n<solvable type=\"package\" name=\"perl-Git\" edition=\"2.51.0-150600.3.12.1\" arch=\"x86_64\" repository=\"repo-sle-update\" summary=\"perl Bindings for Git\">\n<description>Git is a fast, scalable, distributed revision control system with an\nunusually rich command set that provides both high-level operations and\nfull access to internals.\n\nThis package provides the Perl interface to the Git version control system.</description></solvable>\n</to-install>\n</install-summary>\n<prompt id=\"0\">\n<text>Backend:  classic_rpmtrans\nContinue?</text>\n<option default=\"1\" value=\"y\" desc=\"Yes, accept the summary and proceed with installation/removal of packages.\"/>\n<option value=\"n\" desc=\"No, cancel the operation.\"/>\n<option value=\"v\" desc=\"Toggle display of package versions.\"/>\n<option value=\"a\" desc=\"Toggle display of package architectures.\"/>\n<option value=\"r\" desc=\"Toggle display of repositories from which the packages will be installed.\"/>\n<option value=\"m\" desc=\"Toggle display of package vendor names.\"/>\n<option value=\"d\" desc=\"Toggle between showing all details and as few details as possible.\"/>\n<option value=\"g\" desc=\"View the summary in pager.\"/>\n</prompt>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/oss/x86_64/libsha1detectcoll1-1.0.3-2.18.x86_64.rpm\" percent=\"-1\" rate=\"-1\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/oss/x86_64/libsha1detectcoll1-1.0.3-2.18.x86_64.rpm\" percent=\"0\" rate=\"0\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/oss/x86_64/libsha1detectcoll1-1.0.3-2.18.x86_64.rpm\" rate=\"0\" done=\"1\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/oss/noarch/perl-Error-0.17025-1.20.noarch.rpm\" percent=\"-1\" rate=\"-1\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/oss/noarch/perl-Error-0.17025-1.20.noarch.rpm\" percent=\"0\" rate=\"0\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/oss/noarch/perl-Error-0.17025-1.20.noarch.rpm\" rate=\"0\" done=\"1\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/git-core-2.51.0-150600.3.12.1.x86_64.rpm\" percent=\"-1\" rate=\"-1\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/git-core-2.51.0-150600.3.12.1.x86_64.rpm\" percent=\"0\" rate=\"0\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/git-core-2.51.0-150600.3.12.1.x86_64.rpm\" percent=\"0\" rate=\"54760\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/git-core-2.51.0-150600.3.12.1.x86_64.rpm\" percent=\"24\" rate=\"1562056\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/git-core-2.51.0-150600.3.12.1.x86_64.rpm\" percent=\"48\" rate=\"3085424\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/git-core-2.51.0-150600.3.12.1.x86_64.rpm\" percent=\"65\" rate=\"4099024\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/git-core-2.51.0-150600.3.12.1.x86_64.rpm\" percent=\"81\" rate=\"4099024\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/git-core-2.51.0-150600.3.12.1.x86_64.rpm\" percent=\"92\" rate=\"4099024\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/git-core-2.51.0-150600.3.12.1.x86_64.rpm\" percent=\"100\" rate=\"4099024\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/git-core-2.51.0-150600.3.12.1.x86_64.rpm\" rate=\"6301796\" done=\"1\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/perl-Git-2.51.0-150600.3.12.1.x86_64.rpm\" percent=\"-1\" rate=\"-1\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/perl-Git-2.51.0-150600.3.12.1.x86_64.rpm\" percent=\"0\" rate=\"0\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/perl-Git-2.51.0-150600.3.12.1.x86_64.rpm\" rate=\"0\" done=\"1\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/git-2.51.0-150600.3.12.1.x86_64.rpm\" percent=\"-1\" rate=\"-1\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/git-2.51.0-150600.3.12.1.x86_64.rpm\" percent=\"0\" rate=\"0\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/git-2.51.0-150600.3.12.1.x86_64.rpm\" rate=\"0\" done=\"1\"/>\n</stream>\n",
    "stdout_lines": [
        "<?xml version='1.0'?>",
        "<stream>",
        "<install-summary download-size=\"6678364\" space-usage-diff=\"35905368\" space-usage-installed=\"35905368\" space-usage-removed=\"0\" packages-to-change=\"5\" need-restart=\"0\" need-reboot=\"0\">",
        "<to-install>",
        "<solvable type=\"package\" name=\"git\" edition=\"2.51.0-150600.3.12.1\" arch=\"x86_64\" repository=\"repo-sle-update\" summary=\"Fast, scalable, distributed revision control system\">",
        "<description>Git is a fast, scalable, distributed revision control system with an",
        "unusually rich command set that provides both high-level operations and",
        "full access to internals.",
        "",
        "This package itself only provides the README of git but with the",
        "packages it requires, it brings you a complete Git environment",
        "including GTK and email interfaces and tools for importing source code",
        "repositories from other revision control systems such as subversion,",
        "CVS, and GNU arch.</description></solvable>",
        "<solvable type=\"package\" name=\"git-core\" edition=\"2.51.0-150600.3.12.1\" arch=\"x86_64\" repository=\"repo-sle-update\" summary=\"Core git tools\">",
        "<description>Git is a fast, scalable, distributed revision control system with an",
        "unusually rich command set that provides both high-level operations and",
        "full access to internals.",
        "",
        "These are the core tools with minimal dependencies.</description></solvable>",
        "<solvable type=\"package\" name=\"libsha1detectcoll1\" edition=\"1.0.3-2.18\" arch=\"x86_64\" repository=\"openSUSE-Leap-15.6-1\" summary=\"Library that can detect SHA-1 collisions\">",
        "<description>This library was designed as near drop-in replacements for other sha1sum",
        "implementations. It will compute the SHA-1 hash of any given file and additionally",
        "will detect cryptanalytic collision attacks against SHA-1 present in each file.",
        "It is very fast and takes less than twice the amount of time as regular SHA-1.</description></solvable>",
        "<solvable type=\"package\" name=\"perl-Error\" edition=\"0.17025-1.20\" arch=\"noarch\" repository=\"openSUSE-Leap-15.6-1\" summary=\"Error/exception handling in an OO-ish way\">",
        "<description>The &apos;Error&apos; package provides two interfaces. Firstly &apos;Error&apos; provides a",
        "procedural interface to exception handling. Secondly &apos;Error&apos; is a base",
        "class for errors/exceptions that can either be thrown, for subsequent",
        "catch, or can simply be recorded.",
        "",
        "Errors in the class &apos;Error&apos; should not be thrown directly, but the user",
        "should throw errors from a sub-class of &apos;Error&apos;.</description></solvable>",
        "<solvable type=\"package\" name=\"perl-Git\" edition=\"2.51.0-150600.3.12.1\" arch=\"x86_64\" repository=\"repo-sle-update\" summary=\"perl Bindings for Git\">",
        "<description>Git is a fast, scalable, distributed revision control system with an",
        "unusually rich command set that provides both high-level operations and",
        "full access to internals.",
        "",
        "This package provides the Perl interface to the Git version control system.</description></solvable>",
        "</to-install>",
        "</install-summary>",
        "<prompt id=\"0\">",
        "<text>Backend:  classic_rpmtrans",
        "Continue?</text>",
        "<option default=\"1\" value=\"y\" desc=\"Yes, accept the summary and proceed with installation/removal of packages.\"/>",
        "<option value=\"n\" desc=\"No, cancel the operation.\"/>",
        "<option value=\"v\" desc=\"Toggle display of package versions.\"/>",
        "<option value=\"a\" desc=\"Toggle display of package architectures.\"/>",
        "<option value=\"r\" desc=\"Toggle display of repositories from which the packages will be installed.\"/>",
        "<option value=\"m\" desc=\"Toggle display of package vendor names.\"/>",
        "<option value=\"d\" desc=\"Toggle between showing all details and as few details as possible.\"/>",
        "<option value=\"g\" desc=\"View the summary in pager.\"/>",
        "</prompt>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/oss/x86_64/libsha1detectcoll1-1.0.3-2.18.x86_64.rpm\" percent=\"-1\" rate=\"-1\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/oss/x86_64/libsha1detectcoll1-1.0.3-2.18.x86_64.rpm\" percent=\"0\" rate=\"0\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/oss/x86_64/libsha1detectcoll1-1.0.3-2.18.x86_64.rpm\" rate=\"0\" done=\"1\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/oss/noarch/perl-Error-0.17025-1.20.noarch.rpm\" percent=\"-1\" rate=\"-1\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/oss/noarch/perl-Error-0.17025-1.20.noarch.rpm\" percent=\"0\" rate=\"0\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/oss/noarch/perl-Error-0.17025-1.20.noarch.rpm\" rate=\"0\" done=\"1\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/git-core-2.51.0-150600.3.12.1.x86_64.rpm\" percent=\"-1\" rate=\"-1\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/git-core-2.51.0-150600.3.12.1.x86_64.rpm\" percent=\"0\" rate=\"0\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/git-core-2.51.0-150600.3.12.1.x86_64.rpm\" percent=\"0\" rate=\"54760\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/git-core-2.51.0-150600.3.12.1.x86_64.rpm\" percent=\"24\" rate=\"1562056\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/git-core-2.51.0-150600.3.12.1.x86_64.rpm\" percent=\"48\" rate=\"3085424\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/git-core-2.51.0-150600.3.12.1.x86_64.rpm\" percent=\"65\" rate=\"4099024\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/git-core-2.51.0-150600.3.12.1.x86_64.rpm\" percent=\"81\" rate=\"4099024\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/git-core-2.51.0-150600.3.12.1.x86_64.rpm\" percent=\"92\" rate=\"4099024\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/git-core-2.51.0-150600.3.12.1.x86_64.rpm\" percent=\"100\" rate=\"4099024\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/git-core-2.51.0-150600.3.12.1.x86_64.rpm\" rate=\"6301796\" done=\"1\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/perl-Git-2.51.0-150600.3.12.1.x86_64.rpm\" percent=\"-1\" rate=\"-1\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/perl-Git-2.51.0-150600.3.12.1.x86_64.rpm\" percent=\"0\" rate=\"0\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/perl-Git-2.51.0-150600.3.12.1.x86_64.rpm\" rate=\"0\" done=\"1\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/git-2.51.0-150600.3.12.1.x86_64.rpm\" percent=\"-1\" rate=\"-1\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/git-2.51.0-150600.3.12.1.x86_64.rpm\" percent=\"0\" rate=\"0\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/git-2.51.0-150600.3.12.1.x86_64.rpm\" rate=\"0\" done=\"1\"/>",
        "</stream>"
    ],
    "update_cache": false
}
debian | CHANGED => {
    "cache_update_time": 1761245363,
    "cache_updated": false,
    "changed": true,
    "stderr": "",
    "stderr_lines": [],
    "stdout": "Reading package lists...\nBuilding dependency tree...\nReading state information...\nThe following additional packages will be installed:\n  git-man liberror-perl patch\nSuggested packages:\n  git-daemon-run | git-daemon-sysvinit git-doc git-email git-gui gitk gitweb\n  git-cvs git-mediawiki git-svn ed diffutils-doc\nThe following NEW packages will be installed:\n  git git-man liberror-perl patch\n0 upgraded, 4 newly installed, 0 to remove and 0 not upgraded.\nNeed to get 9470 kB of archives.\nAfter this operation, 48.5 MB of additional disk space will be used.\nGet:1 http://httpredir.debian.org/debian bookworm/main amd64 liberror-perl all 0.17029-2 [29.0 kB]\nGet:2 http://httpredir.debian.org/debian bookworm/main amd64 git-man all 1:2.39.5-0+deb12u2 [2053 kB]\nGet:3 http://httpredir.debian.org/debian bookworm/main amd64 git amd64 1:2.39.5-0+deb12u2 [7260 kB]\nGet:4 http://httpredir.debian.org/debian bookworm/main amd64 patch amd64 2.7.6-7 [128 kB]\nFetched 9470 kB in 2min 8s (73.9 kB/s)\nSelecting previously unselected package liberror-perl.\r\n(Reading database ... \r(Reading database ... 5%\r(Reading database ... 10%\r(Reading database ... 15%\r(Reading database ... 20%\r(Reading database ... 25%\r(Reading database ... 30%\r(Reading database ... 35%\r(Reading database ... 40%\r(Reading database ... 45%\r(Reading database ... 50%\r(Reading database ... 55%\r(Reading database ... 60%\r(Reading database ... 65%\r(Reading database ... 70%\r(Reading database ... 75%\r(Reading database ... 80%\r(Reading database ... 85%\r(Reading database ... 90%\r(Reading database ... 95%\r(Reading database ... 100%\r(Reading database ... 34146 files and directories currently installed.)\r\nPreparing to unpack .../liberror-perl_0.17029-2_all.deb ...\r\nUnpacking liberror-perl (0.17029-2) ...\r\nSelecting previously unselected package git-man.\r\nPreparing to unpack .../git-man_1%3a2.39.5-0+deb12u2_all.deb ...\r\nUnpacking git-man (1:2.39.5-0+deb12u2) ...\r\nSelecting previously unselected package git.\r\nPreparing to unpack .../git_1%3a2.39.5-0+deb12u2_amd64.deb ...\r\nUnpacking git (1:2.39.5-0+deb12u2) ...\r\nSelecting previously unselected package patch.\r\nPreparing to unpack .../patch_2.7.6-7_amd64.deb ...\r\nUnpacking patch (2.7.6-7) ...\r\nSetting up liberror-perl (0.17029-2) ...\r\nSetting up patch (2.7.6-7) ...\r\nSetting up git-man (1:2.39.5-0+deb12u2) ...\r\nSetting up git (1:2.39.5-0+deb12u2) ...\r\nProcessing triggers for man-db (2.11.2-2) ...\r\n",
    "stdout_lines": [
        "Reading package lists...",
        "Building dependency tree...",
        "Reading state information...",
        "The following additional packages will be installed:",
        "  git-man liberror-perl patch",
        "Suggested packages:",
        "  git-daemon-run | git-daemon-sysvinit git-doc git-email git-gui gitk gitweb",
        "  git-cvs git-mediawiki git-svn ed diffutils-doc",
        "The following NEW packages will be installed:",
        "  git git-man liberror-perl patch",
        "0 upgraded, 4 newly installed, 0 to remove and 0 not upgraded.",
        "Need to get 9470 kB of archives.",
        "After this operation, 48.5 MB of additional disk space will be used.",
        "Get:1 http://httpredir.debian.org/debian bookworm/main amd64 liberror-perl all 0.17029-2 [29.0 kB]",
        "Get:2 http://httpredir.debian.org/debian bookworm/main amd64 git-man all 1:2.39.5-0+deb12u2 [2053 kB]",
        "Get:3 http://httpredir.debian.org/debian bookworm/main amd64 git amd64 1:2.39.5-0+deb12u2 [7260 kB]",
        "Get:4 http://httpredir.debian.org/debian bookworm/main amd64 patch amd64 2.7.6-7 [128 kB]",
        "Fetched 9470 kB in 2min 8s (73.9 kB/s)",
        "Selecting previously unselected package liberror-perl.",
        "(Reading database ... ",
        "(Reading database ... 5%",
        "(Reading database ... 10%",
        "(Reading database ... 15%",
        "(Reading database ... 20%",
        "(Reading database ... 25%",
        "(Reading database ... 30%",
        "(Reading database ... 35%",
        "(Reading database ... 40%",
        "(Reading database ... 45%",
        "(Reading database ... 50%",
        "(Reading database ... 55%",
        "(Reading database ... 60%",
        "(Reading database ... 65%",
        "(Reading database ... 70%",
        "(Reading database ... 75%",
        "(Reading database ... 80%",
        "(Reading database ... 85%",
        "(Reading database ... 90%",
        "(Reading database ... 95%",
        "(Reading database ... 100%",
        "(Reading database ... 34146 files and directories currently installed.)",
        "Preparing to unpack .../liberror-perl_0.17029-2_all.deb ...",
        "Unpacking liberror-perl (0.17029-2) ...",
        "Selecting previously unselected package git-man.",
        "Preparing to unpack .../git-man_1%3a2.39.5-0+deb12u2_all.deb ...",
        "Unpacking git-man (1:2.39.5-0+deb12u2) ...",
        "Selecting previously unselected package git.",
        "Preparing to unpack .../git_1%3a2.39.5-0+deb12u2_amd64.deb ...",
        "Unpacking git (1:2.39.5-0+deb12u2) ...",
        "Selecting previously unselected package patch.",
        "Preparing to unpack .../patch_2.7.6-7_amd64.deb ...",
        "Unpacking patch (2.7.6-7) ...",
        "Setting up liberror-perl (0.17029-2) ...",
        "Setting up patch (2.7.6-7) ...",
        "Setting up git-man (1:2.39.5-0+deb12u2) ...",
        "Setting up git (1:2.39.5-0+deb12u2) ...",
        "Processing triggers for man-db (2.11.2-2) ..."
    ]
}
```

```sh
ansible all -m package -a "name=git state=present"
```

```
debian | SUCCESS => {
    "cache_update_time": 1761245363,
    "cache_updated": false,
    "changed": false
}
suse | SUCCESS => {
    "changed": false,
    "name": [
        "git"
    ],
    "rc": 0,
    "state": "present",
    "update_cache": false
}
rocky | SUCCESS => {
    "changed": false,
    "msg": "Nothing to do",
    "rc": 0,
    "results": []
}
```

nmap

```sh
ansible all -m package -a "name=nmap state=present"
```

```
rocky | CHANGED => {
    "changed": true,
    "msg": "",
    "rc": 0,
    "results": [
        "Installed: nmap-3:7.92-3.el9.x86_64"
    ]
}
suse | CHANGED => {
    "changed": true,
    "cmd": [
        "/usr/bin/zypper",
        "--quiet",
        "--non-interactive",
        "--xmlout",
        "install",
        "--type",
        "package",
        "--auto-agree-with-licenses",
        "--no-recommends",
        "--",
        "+nmap"
    ],
    "name": [
        "nmap"
    ],
    "rc": 0,
    "state": "present",
    "stderr": "",
    "stderr_lines": [],
    "stdout": "<?xml version='1.0'?>\n<stream>\n<install-summary download-size=\"6121272\" space-usage-diff=\"26574383\" space-usage-installed=\"26574383\" space-usage-removed=\"0\" packages-to-change=\"3\" need-restart=\"0\" need-reboot=\"0\">\n<to-install>\n<solvable type=\"package\" name=\"libpcap1\" edition=\"1.10.4-150600.3.6.2\" arch=\"x86_64\" repository=\"repo-sle-update\" summary=\"A Library for Network Sniffers\">\n<description>libpcap is a library used by packet sniffer programs. It provides an\ninterface for them to capture and analyze packets from network devices.\nThis package is only needed if you plan to compile or write such a\nprogram yourself.</description></solvable>\n<solvable type=\"package\" name=\"libssh2-1\" edition=\"1.11.0-150600.18.1\" arch=\"x86_64\" repository=\"openSUSE-Leap-15.6-1\" summary=\"A library implementing the SSH2 protocol\">\n<description>libssh2 is a library implementing the SSH2 protocol as defined by\nInternet Drafts: SECSH-TRANS, SECSH-USERAUTH, SECSH-CONNECTION,\nSECSH-ARCH, SECSH-FILEXFER, SECSH-DHGEX, SECSH-NUMBERS, and\nSECSH-PUBLICKEY.</description></solvable>\n<solvable type=\"package\" name=\"nmap\" edition=\"7.94-lp156.1.2\" arch=\"x86_64\" repository=\"openSUSE-Leap-15.6-Non-Oss\" summary=\"Network exploration tool and security scanner\">\n<description>Nmap (&quot;Network Mapper&quot;) is a utility for network exploration or\nsecurity auditing. It may as well be used for tasks such as network\ninventory, managing service upgrade schedules, and monitoring host or\nservice uptime. Nmap uses raw IP packets to determine what hosts are\navailable on the network, what services (application name and\nversion) those hosts are offering, what operating systems (and OS\nversions) they are running, what type of packet filters/firewalls are\nin use, and dozens of other characteristics. It scans large networks,\nand works fine against single hosts.</description></solvable>\n</to-install>\n</install-summary>\n<prompt id=\"0\">\n<text>Backend:  classic_rpmtrans\nContinue?</text>\n<option default=\"1\" value=\"y\" desc=\"Yes, accept the summary and proceed with installation/removal of packages.\"/>\n<option value=\"n\" desc=\"No, cancel the operation.\"/>\n<option value=\"v\" desc=\"Toggle display of package versions.\"/>\n<option value=\"a\" desc=\"Toggle display of package architectures.\"/>\n<option value=\"r\" desc=\"Toggle display of repositories from which the packages will be installed.\"/>\n<option value=\"m\" desc=\"Toggle display of package vendor names.\"/>\n<option value=\"d\" desc=\"Toggle between showing all details and as few details as possible.\"/>\n<option value=\"g\" desc=\"View the summary in pager.\"/>\n</prompt>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/oss/x86_64/libssh2-1-1.11.0-150600.18.1.x86_64.rpm\" percent=\"-1\" rate=\"-1\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/oss/x86_64/libssh2-1-1.11.0-150600.18.1.x86_64.rpm\" percent=\"0\" rate=\"0\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/oss/x86_64/libssh2-1-1.11.0-150600.18.1.x86_64.rpm\" percent=\"0\" rate=\"1186\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/oss/x86_64/libssh2-1-1.11.0-150600.18.1.x86_64.rpm\" rate=\"1186\" done=\"1\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/libpcap1-1.10.4-150600.3.6.2.x86_64.rpm\" percent=\"-1\" rate=\"-1\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/libpcap1-1.10.4-150600.3.6.2.x86_64.rpm\" percent=\"0\" rate=\"0\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/libpcap1-1.10.4-150600.3.6.2.x86_64.rpm\" percent=\"1\" rate=\"2618\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/libpcap1-1.10.4-150600.3.6.2.x86_64.rpm\" rate=\"2618\" done=\"1\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"-1\" rate=\"-1\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"0\" rate=\"0\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"0\" rate=\"33032\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"9\" rate=\"525360\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"18\" rate=\"891704\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"24\" rate=\"891704\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"30\" rate=\"891704\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"38\" rate=\"891704\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"48\" rate=\"891704\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"59\" rate=\"891704\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"64\" rate=\"891704\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"74\" rate=\"3220352\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"89\" rate=\"3220352\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"98\" rate=\"3220352\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"100\" rate=\"3220352\"/>\n<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" rate=\"2908750\" done=\"1\"/>\n</stream>\n",
    "stdout_lines": [
        "<?xml version='1.0'?>",
        "<stream>",
        "<install-summary download-size=\"6121272\" space-usage-diff=\"26574383\" space-usage-installed=\"26574383\" space-usage-removed=\"0\" packages-to-change=\"3\" need-restart=\"0\" need-reboot=\"0\">",
        "<to-install>",
        "<solvable type=\"package\" name=\"libpcap1\" edition=\"1.10.4-150600.3.6.2\" arch=\"x86_64\" repository=\"repo-sle-update\" summary=\"A Library for Network Sniffers\">",
        "<description>libpcap is a library used by packet sniffer programs. It provides an",
        "interface for them to capture and analyze packets from network devices.",
        "This package is only needed if you plan to compile or write such a",
        "program yourself.</description></solvable>",
        "<solvable type=\"package\" name=\"libssh2-1\" edition=\"1.11.0-150600.18.1\" arch=\"x86_64\" repository=\"openSUSE-Leap-15.6-1\" summary=\"A library implementing the SSH2 protocol\">",
        "<description>libssh2 is a library implementing the SSH2 protocol as defined by",
        "Internet Drafts: SECSH-TRANS, SECSH-USERAUTH, SECSH-CONNECTION,",
        "SECSH-ARCH, SECSH-FILEXFER, SECSH-DHGEX, SECSH-NUMBERS, and",
        "SECSH-PUBLICKEY.</description></solvable>",
        "<solvable type=\"package\" name=\"nmap\" edition=\"7.94-lp156.1.2\" arch=\"x86_64\" repository=\"openSUSE-Leap-15.6-Non-Oss\" summary=\"Network exploration tool and security scanner\">",
        "<description>Nmap (&quot;Network Mapper&quot;) is a utility for network exploration or",
        "security auditing. It may as well be used for tasks such as network",
        "inventory, managing service upgrade schedules, and monitoring host or",
        "service uptime. Nmap uses raw IP packets to determine what hosts are",
        "available on the network, what services (application name and",
        "version) those hosts are offering, what operating systems (and OS",
        "versions) they are running, what type of packet filters/firewalls are",
        "in use, and dozens of other characteristics. It scans large networks,",
        "and works fine against single hosts.</description></solvable>",
        "</to-install>",
        "</install-summary>",
        "<prompt id=\"0\">",
        "<text>Backend:  classic_rpmtrans",
        "Continue?</text>",
        "<option default=\"1\" value=\"y\" desc=\"Yes, accept the summary and proceed with installation/removal of packages.\"/>",
        "<option value=\"n\" desc=\"No, cancel the operation.\"/>",
        "<option value=\"v\" desc=\"Toggle display of package versions.\"/>",
        "<option value=\"a\" desc=\"Toggle display of package architectures.\"/>",
        "<option value=\"r\" desc=\"Toggle display of repositories from which the packages will be installed.\"/>",
        "<option value=\"m\" desc=\"Toggle display of package vendor names.\"/>",
        "<option value=\"d\" desc=\"Toggle between showing all details and as few details as possible.\"/>",
        "<option value=\"g\" desc=\"View the summary in pager.\"/>",
        "</prompt>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/oss/x86_64/libssh2-1-1.11.0-150600.18.1.x86_64.rpm\" percent=\"-1\" rate=\"-1\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/oss/x86_64/libssh2-1-1.11.0-150600.18.1.x86_64.rpm\" percent=\"0\" rate=\"0\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/oss/x86_64/libssh2-1-1.11.0-150600.18.1.x86_64.rpm\" percent=\"0\" rate=\"1186\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/oss/x86_64/libssh2-1-1.11.0-150600.18.1.x86_64.rpm\" rate=\"1186\" done=\"1\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/libpcap1-1.10.4-150600.3.6.2.x86_64.rpm\" percent=\"-1\" rate=\"-1\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/libpcap1-1.10.4-150600.3.6.2.x86_64.rpm\" percent=\"0\" rate=\"0\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/libpcap1-1.10.4-150600.3.6.2.x86_64.rpm\" percent=\"1\" rate=\"2618\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/update/leap/15.6/sle/x86_64/libpcap1-1.10.4-150600.3.6.2.x86_64.rpm\" rate=\"2618\" done=\"1\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"-1\" rate=\"-1\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"0\" rate=\"0\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"0\" rate=\"33032\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"9\" rate=\"525360\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"18\" rate=\"891704\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"24\" rate=\"891704\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"30\" rate=\"891704\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"38\" rate=\"891704\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"48\" rate=\"891704\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"59\" rate=\"891704\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"64\" rate=\"891704\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"74\" rate=\"3220352\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"89\" rate=\"3220352\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"98\" rate=\"3220352\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" percent=\"100\" rate=\"3220352\"/>",
        "<download url=\"http://fr2.rpmfind.net/linux/opensuse/distribution/leap/15.6/repo/non-oss/x86_64/nmap-7.94-lp156.1.2.x86_64.rpm\" rate=\"2908750\" done=\"1\"/>",
        "</stream>"
    ],
    "update_cache": false
}
debian | CHANGED => {
    "cache_update_time": 1761245363,
    "cache_updated": false,
    "changed": true,
    "stderr": "",
    "stderr_lines": [],
    "stdout": "Reading package lists...\nBuilding dependency tree...\nReading state information...\nThe following additional packages will be installed:\n  libblas3 liblinear4 liblua5.3-0 libpcap0.8 libpcre3 lua-lpeg nmap-common\nSuggested packages:\n  liblinear-tools liblinear-dev ncat ndiff zenmap\nThe following NEW packages will be installed:\n  libblas3 liblinear4 liblua5.3-0 libpcap0.8 libpcre3 lua-lpeg nmap\n  nmap-common\n0 upgraded, 8 newly installed, 0 to remove and 0 not upgraded.\nNeed to get 6896 kB of archives.\nAfter this operation, 28.7 MB of additional disk space will be used.\nGet:1 http://httpredir.debian.org/debian bookworm/main amd64 libblas3 amd64 3.11.0-2 [149 kB]\nGet:2 http://httpredir.debian.org/debian bookworm/main amd64 liblinear4 amd64 2.3.0+dfsg-5 [43.6 kB]\nGet:3 http://httpredir.debian.org/debian bookworm/main amd64 liblua5.3-0 amd64 5.3.6-2 [123 kB]\nGet:4 http://httpredir.debian.org/debian bookworm/main amd64 libpcap0.8 amd64 1.10.3-1 [157 kB]\nGet:5 http://httpredir.debian.org/debian bookworm/main amd64 libpcre3 amd64 2:8.39-15 [341 kB]\nGet:6 http://httpredir.debian.org/debian bookworm/main amd64 lua-lpeg amd64 1.0.2-2 [37.7 kB]\nGet:7 http://httpredir.debian.org/debian bookworm/main amd64 nmap-common all 7.93+dfsg1-1 [4148 kB]\nGet:8 http://httpredir.debian.org/debian bookworm/main amd64 nmap amd64 7.93+dfsg1-1 [1897 kB]\nFetched 6896 kB in 1min 5s (105 kB/s)\nSelecting previously unselected package libblas3:amd64.\r\n(Reading database ... \r(Reading database ... 5%\r(Reading database ... 10%\r(Reading database ... 15%\r(Reading database ... 20%\r(Reading database ... 25%\r(Reading database ... 30%\r(Reading database ... 35%\r(Reading database ... 40%\r(Reading database ... 45%\r(Reading database ... 50%\r(Reading database ... 55%\r(Reading database ... 60%\r(Reading database ... 65%\r(Reading database ... 70%\r(Reading database ... 75%\r(Reading database ... 80%\r(Reading database ... 85%\r(Reading database ... 90%\r(Reading database ... 95%\r(Reading database ... 100%\r(Reading database ... 35265 files and directories currently installed.)\r\nPreparing to unpack .../0-libblas3_3.11.0-2_amd64.deb ...\r\nUnpacking libblas3:amd64 (3.11.0-2) ...\r\nSelecting previously unselected package liblinear4:amd64.\r\nPreparing to unpack .../1-liblinear4_2.3.0+dfsg-5_amd64.deb ...\r\nUnpacking liblinear4:amd64 (2.3.0+dfsg-5) ...\r\nSelecting previously unselected package liblua5.3-0:amd64.\r\nPreparing to unpack .../2-liblua5.3-0_5.3.6-2_amd64.deb ...\r\nUnpacking liblua5.3-0:amd64 (5.3.6-2) ...\r\nSelecting previously unselected package libpcap0.8:amd64.\r\nPreparing to unpack .../3-libpcap0.8_1.10.3-1_amd64.deb ...\r\nUnpacking libpcap0.8:amd64 (1.10.3-1) ...\r\nSelecting previously unselected package libpcre3:amd64.\r\nPreparing to unpack .../4-libpcre3_2%3a8.39-15_amd64.deb ...\r\nUnpacking libpcre3:amd64 (2:8.39-15) ...\r\nSelecting previously unselected package lua-lpeg:amd64.\r\nPreparing to unpack .../5-lua-lpeg_1.0.2-2_amd64.deb ...\r\nUnpacking lua-lpeg:amd64 (1.0.2-2) ...\r\nSelecting previously unselected package nmap-common.\r\nPreparing to unpack .../6-nmap-common_7.93+dfsg1-1_all.deb ...\r\nUnpacking nmap-common (7.93+dfsg1-1) ...\r\nSelecting previously unselected package nmap.\r\nPreparing to unpack .../7-nmap_7.93+dfsg1-1_amd64.deb ...\r\nUnpacking nmap (7.93+dfsg1-1) ...\r\nSetting up lua-lpeg:amd64 (1.0.2-2) ...\r\nSetting up libpcre3:amd64 (2:8.39-15) ...\r\nSetting up libblas3:amd64 (3.11.0-2) ...\r\nupdate-alternatives: using /usr/lib/x86_64-linux-gnu/blas/libblas.so.3 to provide /usr/lib/x86_64-linux-gnu/libblas.so.3 (libblas.so.3-x86_64-linux-gnu) in auto mode\r\nSetting up libpcap0.8:amd64 (1.10.3-1) ...\r\nSetting up nmap-common (7.93+dfsg1-1) ...\r\nSetting up liblua5.3-0:amd64 (5.3.6-2) ...\r\nSetting up liblinear4:amd64 (2.3.0+dfsg-5) ...\r\nSetting up nmap (7.93+dfsg1-1) ...\r\nProcessing triggers for man-db (2.11.2-2) ...\r\nProcessing triggers for libc-bin (2.36-9+deb12u13) ...\r\n",
    "stdout_lines": [
        "Reading package lists...",
        "Building dependency tree...",
        "Reading state information...",
        "The following additional packages will be installed:",
        "  libblas3 liblinear4 liblua5.3-0 libpcap0.8 libpcre3 lua-lpeg nmap-common",
        "Suggested packages:",
        "  liblinear-tools liblinear-dev ncat ndiff zenmap",
        "The following NEW packages will be installed:",
        "  libblas3 liblinear4 liblua5.3-0 libpcap0.8 libpcre3 lua-lpeg nmap",
        "  nmap-common",
        "0 upgraded, 8 newly installed, 0 to remove and 0 not upgraded.",
        "Need to get 6896 kB of archives.",
        "After this operation, 28.7 MB of additional disk space will be used.",
        "Get:1 http://httpredir.debian.org/debian bookworm/main amd64 libblas3 amd64 3.11.0-2 [149 kB]",
        "Get:2 http://httpredir.debian.org/debian bookworm/main amd64 liblinear4 amd64 2.3.0+dfsg-5 [43.6 kB]",
        "Get:3 http://httpredir.debian.org/debian bookworm/main amd64 liblua5.3-0 amd64 5.3.6-2 [123 kB]",
        "Get:4 http://httpredir.debian.org/debian bookworm/main amd64 libpcap0.8 amd64 1.10.3-1 [157 kB]",
        "Get:5 http://httpredir.debian.org/debian bookworm/main amd64 libpcre3 amd64 2:8.39-15 [341 kB]",
        "Get:6 http://httpredir.debian.org/debian bookworm/main amd64 lua-lpeg amd64 1.0.2-2 [37.7 kB]",
        "Get:7 http://httpredir.debian.org/debian bookworm/main amd64 nmap-common all 7.93+dfsg1-1 [4148 kB]",
        "Get:8 http://httpredir.debian.org/debian bookworm/main amd64 nmap amd64 7.93+dfsg1-1 [1897 kB]",
        "Fetched 6896 kB in 1min 5s (105 kB/s)",
        "Selecting previously unselected package libblas3:amd64.",
        "(Reading database ... ",
        "(Reading database ... 5%",
        "(Reading database ... 10%",
        "(Reading database ... 15%",
        "(Reading database ... 20%",
        "(Reading database ... 25%",
        "(Reading database ... 30%",
        "(Reading database ... 35%",
        "(Reading database ... 40%",
        "(Reading database ... 45%",
        "(Reading database ... 50%",
        "(Reading database ... 55%",
        "(Reading database ... 60%",
        "(Reading database ... 65%",
        "(Reading database ... 70%",
        "(Reading database ... 75%",
        "(Reading database ... 80%",
        "(Reading database ... 85%",
        "(Reading database ... 90%",
        "(Reading database ... 95%",
        "(Reading database ... 100%",
        "(Reading database ... 35265 files and directories currently installed.)",
        "Preparing to unpack .../0-libblas3_3.11.0-2_amd64.deb ...",
        "Unpacking libblas3:amd64 (3.11.0-2) ...",
        "Selecting previously unselected package liblinear4:amd64.",
        "Preparing to unpack .../1-liblinear4_2.3.0+dfsg-5_amd64.deb ...",
        "Unpacking liblinear4:amd64 (2.3.0+dfsg-5) ...",
        "Selecting previously unselected package liblua5.3-0:amd64.",
        "Preparing to unpack .../2-liblua5.3-0_5.3.6-2_amd64.deb ...",
        "Unpacking liblua5.3-0:amd64 (5.3.6-2) ...",
        "Selecting previously unselected package libpcap0.8:amd64.",
        "Preparing to unpack .../3-libpcap0.8_1.10.3-1_amd64.deb ...",
        "Unpacking libpcap0.8:amd64 (1.10.3-1) ...",
        "Selecting previously unselected package libpcre3:amd64.",
        "Preparing to unpack .../4-libpcre3_2%3a8.39-15_amd64.deb ...",
        "Unpacking libpcre3:amd64 (2:8.39-15) ...",
        "Selecting previously unselected package lua-lpeg:amd64.",
        "Preparing to unpack .../5-lua-lpeg_1.0.2-2_amd64.deb ...",
        "Unpacking lua-lpeg:amd64 (1.0.2-2) ...",
        "Selecting previously unselected package nmap-common.",
        "Preparing to unpack .../6-nmap-common_7.93+dfsg1-1_all.deb ...",
        "Unpacking nmap-common (7.93+dfsg1-1) ...",
        "Selecting previously unselected package nmap.",
        "Preparing to unpack .../7-nmap_7.93+dfsg1-1_amd64.deb ...",
        "Unpacking nmap (7.93+dfsg1-1) ...",
        "Setting up lua-lpeg:amd64 (1.0.2-2) ...",
        "Setting up libpcre3:amd64 (2:8.39-15) ...",
        "Setting up libblas3:amd64 (3.11.0-2) ...",
        "update-alternatives: using /usr/lib/x86_64-linux-gnu/blas/libblas.so.3 to provide /usr/lib/x86_64-linux-gnu/libblas.so.3 (libblas.so.3-x86_64-linux-gnu) in auto mode",
        "Setting up libpcap0.8:amd64 (1.10.3-1) ...",
        "Setting up nmap-common (7.93+dfsg1-1) ...",
        "Setting up liblua5.3-0:amd64 (5.3.6-2) ...",
        "Setting up liblinear4:amd64 (2.3.0+dfsg-5) ...",
        "Setting up nmap (7.93+dfsg1-1) ...",
        "Processing triggers for man-db (2.11.2-2) ...",
        "Processing triggers for libc-bin (2.36-9+deb12u13) ..."
    ]
}
```

```sh
ansible all -m package -a "name=nmap state=present"
```

```
rocky | SUCCESS => {
    "changed": false,
    "msg": "Nothing to do",
    "rc": 0,
    "results": []
}
debian | SUCCESS => {
    "cache_update_time": 1761245363,
    "cache_updated": false,
    "changed": false
}
suse | SUCCESS => {
    "changed": false,
    "name": [
        "nmap"
    ],
    "rc": 0,
    "state": "present",
    "update_cache": false
}
```

- Désinstallez successivement ces trois paquets en utilisant le paramètre supplémentaire `state=absent`.

tree

```sh
ansible all -m package -a "name=tree state=absent"
```

```
rocky | CHANGED => {
    "changed": true,
    "msg": "",
    "rc": 0,
    "results": [
        "Removed: tree-1.8.0-10.el9.x86_64"
    ]
}
suse | CHANGED => {
    "changed": true,
    "cmd": [
        "/usr/bin/zypper",
        "--quiet",
        "--non-interactive",
        "--xmlout",
        "remove",
        "--type",
        "package",
        "tree"
    ],
    "name": [
        "tree"
    ],
    "rc": 0,
    "state": "absent",
    "stderr": "",
    "stderr_lines": [],
    "stdout": "<?xml version='1.0'?>\n<stream>\n<install-summary download-size=\"0\" space-usage-diff=\"-116508\" space-usage-installed=\"0\" space-usage-removed=\"116508\" packages-to-change=\"1\" need-restart=\"0\" need-reboot=\"0\">\n<to-remove>\n<solvable type=\"package\" name=\"tree\" edition=\"1.7.0-150000.3.2.1\" arch=\"x86_64\" repository=\"@System\" summary=\"File listing as a tree\">\n<description>Tree is a recursive directory listing command that produces a depth\nindented listing of files, which is colorized ala dircolors if the\nLS_COLORS environment variable is set and output is to tty.</description></solvable>\n</to-remove>\n</install-summary>\n<prompt id=\"0\">\n<text>Backend:  classic_rpmtrans\nContinue?</text>\n<option default=\"1\" value=\"y\" desc=\"Yes, accept the summary and proceed with installation/removal of packages.\"/>\n<option value=\"n\" desc=\"No, cancel the operation.\"/>\n<option value=\"v\" desc=\"Toggle display of package versions.\"/>\n<option value=\"a\" desc=\"Toggle display of package architectures.\"/>\n<option value=\"r\" desc=\"Toggle display of repositories from which the packages will be installed.\"/>\n<option value=\"m\" desc=\"Toggle display of package vendor names.\"/>\n<option value=\"d\" desc=\"Toggle between showing all details and as few details as possible.\"/>\n<option value=\"g\" desc=\"View the summary in pager.\"/>\n</prompt>\n</stream>\n",
    "stdout_lines": [
        "<?xml version='1.0'?>",
        "<stream>",
        "<install-summary download-size=\"0\" space-usage-diff=\"-116508\" space-usage-installed=\"0\" space-usage-removed=\"116508\" packages-to-change=\"1\" need-restart=\"0\" need-reboot=\"0\">",
        "<to-remove>",
        "<solvable type=\"package\" name=\"tree\" edition=\"1.7.0-150000.3.2.1\" arch=\"x86_64\" repository=\"@System\" summary=\"File listing as a tree\">",
        "<description>Tree is a recursive directory listing command that produces a depth",
        "indented listing of files, which is colorized ala dircolors if the",
        "LS_COLORS environment variable is set and output is to tty.</description></solvable>",
        "</to-remove>",
        "</install-summary>",
        "<prompt id=\"0\">",
        "<text>Backend:  classic_rpmtrans",
        "Continue?</text>",
        "<option default=\"1\" value=\"y\" desc=\"Yes, accept the summary and proceed with installation/removal of packages.\"/>",
        "<option value=\"n\" desc=\"No, cancel the operation.\"/>",
        "<option value=\"v\" desc=\"Toggle display of package versions.\"/>",
        "<option value=\"a\" desc=\"Toggle display of package architectures.\"/>",
        "<option value=\"r\" desc=\"Toggle display of repositories from which the packages will be installed.\"/>",
        "<option value=\"m\" desc=\"Toggle display of package vendor names.\"/>",
        "<option value=\"d\" desc=\"Toggle between showing all details and as few details as possible.\"/>",
        "<option value=\"g\" desc=\"View the summary in pager.\"/>",
        "</prompt>",
        "</stream>"
    ],
    "update_cache": false
}
debian | CHANGED => {
    "changed": true,
    "stderr": "",
    "stderr_lines": [],
    "stdout": "Reading package lists...\nBuilding dependency tree...\nReading state information...\nThe following packages will be REMOVED:\n  tree\n0 upgraded, 0 newly installed, 1 to remove and 0 not upgraded.\nAfter this operation, 116 kB disk space will be freed.\n(Reading database ... \r(Reading database ... 5%\r(Reading database ... 10%\r(Reading database ... 15%\r(Reading database ... 20%\r(Reading database ... 25%\r(Reading database ... 30%\r(Reading database ... 35%\r(Reading database ... 40%\r(Reading database ... 45%\r(Reading database ... 50%\r(Reading database ... 55%\r(Reading database ... 60%\r(Reading database ... 65%\r(Reading database ... 70%\r(Reading database ... 75%\r(Reading database ... 80%\r(Reading database ... 85%\r(Reading database ... 90%\r(Reading database ... 95%\r(Reading database ... 100%\r(Reading database ... 36191 files and directories currently installed.)\r\nRemoving tree (2.1.0-1) ...\r\nProcessing triggers for man-db (2.11.2-2) ...\r\n",
    "stdout_lines": [
        "Reading package lists...",
        "Building dependency tree...",
        "Reading state information...",
        "The following packages will be REMOVED:",
        "  tree",
        "0 upgraded, 0 newly installed, 1 to remove and 0 not upgraded.",
        "After this operation, 116 kB disk space will be freed.",
        "(Reading database ... ",
        "(Reading database ... 5%",
        "(Reading database ... 10%",
        "(Reading database ... 15%",
        "(Reading database ... 20%",
        "(Reading database ... 25%",
        "(Reading database ... 30%",
        "(Reading database ... 35%",
        "(Reading database ... 40%",
        "(Reading database ... 45%",
        "(Reading database ... 50%",
        "(Reading database ... 55%",
        "(Reading database ... 60%",
        "(Reading database ... 65%",
        "(Reading database ... 70%",
        "(Reading database ... 75%",
        "(Reading database ... 80%",
        "(Reading database ... 85%",
        "(Reading database ... 90%",
        "(Reading database ... 95%",
        "(Reading database ... 100%",
        "(Reading database ... 36191 files and directories currently installed.)",
        "Removing tree (2.1.0-1) ...",
        "Processing triggers for man-db (2.11.2-2) ..."
    ]
}
```

```sh
ansible all -m package -a "name=tree state=absent"
```

```
rocky | SUCCESS => {
    "changed": false,
    "msg": "Nothing to do",
    "rc": 0,
    "results": []
}
debian | SUCCESS => {
    "changed": false
}
suse | SUCCESS => {
    "changed": false,
    "name": [
        "tree"
    ],
    "rc": 0,
    "state": "absent",
    "update_cache": false
}
```

git

```sh
ansible all -m package -a "name=git state=absent"
```

```
suse | CHANGED => {
    "changed": true,
    "cmd": [
        "/usr/bin/zypper",
        "--quiet",
        "--non-interactive",
        "--xmlout",
        "remove",
        "--type",
        "package",
        "git"
    ],
    "name": [
        "git"
    ],
    "rc": 0,
    "state": "absent",
    "stderr": "",
    "stderr_lines": [],
    "stdout": "<?xml version='1.0'?>\n<stream>\n<install-summary download-size=\"0\" space-usage-diff=\"-3662\" space-usage-installed=\"0\" space-usage-removed=\"3662\" packages-to-change=\"1\" need-restart=\"0\" need-reboot=\"0\">\n<to-remove>\n<solvable type=\"package\" name=\"git\" edition=\"2.51.0-150600.3.12.1\" arch=\"x86_64\" repository=\"@System\" summary=\"Fast, scalable, distributed revision control system\">\n<description>Git is a fast, scalable, distributed revision control system with an\nunusually rich command set that provides both high-level operations and\nfull access to internals.\n\nThis package itself only provides the README of git but with the\npackages it requires, it brings you a complete Git environment\nincluding GTK and email interfaces and tools for importing source code\nrepositories from other revision control systems such as subversion,\nCVS, and GNU arch.</description></solvable>\n</to-remove>\n</install-summary>\n<prompt id=\"0\">\n<text>Backend:  classic_rpmtrans\nContinue?</text>\n<option default=\"1\" value=\"y\" desc=\"Yes, accept the summary and proceed with installation/removal of packages.\"/>\n<option value=\"n\" desc=\"No, cancel the operation.\"/>\n<option value=\"v\" desc=\"Toggle display of package versions.\"/>\n<option value=\"a\" desc=\"Toggle display of package architectures.\"/>\n<option value=\"r\" desc=\"Toggle display of repositories from which the packages will be installed.\"/>\n<option value=\"m\" desc=\"Toggle display of package vendor names.\"/>\n<option value=\"d\" desc=\"Toggle between showing all details and as few details as possible.\"/>\n<option value=\"g\" desc=\"View the summary in pager.\"/>\n</prompt>\n</stream>\n",
    "stdout_lines": [
        "<?xml version='1.0'?>",
        "<stream>",
        "<install-summary download-size=\"0\" space-usage-diff=\"-3662\" space-usage-installed=\"0\" space-usage-removed=\"3662\" packages-to-change=\"1\" need-restart=\"0\" need-reboot=\"0\">",
        "<to-remove>",
        "<solvable type=\"package\" name=\"git\" edition=\"2.51.0-150600.3.12.1\" arch=\"x86_64\" repository=\"@System\" summary=\"Fast, scalable, distributed revision control system\">",
        "<description>Git is a fast, scalable, distributed revision control system with an",
        "unusually rich command set that provides both high-level operations and",
        "full access to internals.",
        "",
        "This package itself only provides the README of git but with the",
        "packages it requires, it brings you a complete Git environment",
        "including GTK and email interfaces and tools for importing source code",
        "repositories from other revision control systems such as subversion,",
        "CVS, and GNU arch.</description></solvable>",
        "</to-remove>",
        "</install-summary>",
        "<prompt id=\"0\">",
        "<text>Backend:  classic_rpmtrans",
        "Continue?</text>",
        "<option default=\"1\" value=\"y\" desc=\"Yes, accept the summary and proceed with installation/removal of packages.\"/>",
        "<option value=\"n\" desc=\"No, cancel the operation.\"/>",
        "<option value=\"v\" desc=\"Toggle display of package versions.\"/>",
        "<option value=\"a\" desc=\"Toggle display of package architectures.\"/>",
        "<option value=\"r\" desc=\"Toggle display of repositories from which the packages will be installed.\"/>",
        "<option value=\"m\" desc=\"Toggle display of package vendor names.\"/>",
        "<option value=\"d\" desc=\"Toggle between showing all details and as few details as possible.\"/>",
        "<option value=\"g\" desc=\"View the summary in pager.\"/>",
        "</prompt>",
        "</stream>"
    ],
    "update_cache": false
}
rocky | CHANGED => {
    "changed": true,
    "msg": "",
    "rc": 0,
    "results": [
        "Removed: perl-Git-2.47.3-1.el9_6.noarch",
        "Removed: git-2.47.3-1.el9_6.x86_64"
    ]
}
debian | CHANGED => {
    "changed": true,
    "stderr": "",
    "stderr_lines": [],
    "stdout": "Reading package lists...\nBuilding dependency tree...\nReading state information...\nThe following packages were automatically installed and are no longer required:\n  git-man liberror-perl patch\nUse 'sudo apt autoremove' to remove them.\nThe following packages will be REMOVED:\n  git\n0 upgraded, 0 newly installed, 1 to remove and 0 not upgraded.\nAfter this operation, 46.0 MB disk space will be freed.\n(Reading database ... \r(Reading database ... 5%\r(Reading database ... 10%\r(Reading database ... 15%\r(Reading database ... 20%\r(Reading database ... 25%\r(Reading database ... 30%\r(Reading database ... 35%\r(Reading database ... 40%\r(Reading database ... 45%\r(Reading database ... 50%\r(Reading database ... 55%\r(Reading database ... 60%\r(Reading database ... 65%\r(Reading database ... 70%\r(Reading database ... 75%\r(Reading database ... 80%\r(Reading database ... 85%\r(Reading database ... 90%\r(Reading database ... 95%\r(Reading database ... 100%\r(Reading database ... 36183 files and directories currently installed.)\r\nRemoving git (1:2.39.5-0+deb12u2) ...\r\n",
    "stdout_lines": [
        "Reading package lists...",
        "Building dependency tree...",
        "Reading state information...",
        "The following packages were automatically installed and are no longer required:",
        "  git-man liberror-perl patch",
        "Use 'sudo apt autoremove' to remove them.",
        "The following packages will be REMOVED:",
        "  git",
        "0 upgraded, 0 newly installed, 1 to remove and 0 not upgraded.",
        "After this operation, 46.0 MB disk space will be freed.",
        "(Reading database ... ",
        "(Reading database ... 5%",
        "(Reading database ... 10%",
        "(Reading database ... 15%",
        "(Reading database ... 20%",
        "(Reading database ... 25%",
        "(Reading database ... 30%",
        "(Reading database ... 35%",
        "(Reading database ... 40%",
        "(Reading database ... 45%",
        "(Reading database ... 50%",
        "(Reading database ... 55%",
        "(Reading database ... 60%",
        "(Reading database ... 65%",
        "(Reading database ... 70%",
        "(Reading database ... 75%",
        "(Reading database ... 80%",
        "(Reading database ... 85%",
        "(Reading database ... 90%",
        "(Reading database ... 95%",
        "(Reading database ... 100%",
        "(Reading database ... 36183 files and directories currently installed.)",
        "Removing git (1:2.39.5-0+deb12u2) ..."
    ]
}
```

```sh
ansible all -m package -a "name=git state=absent"
```

```
suse | SUCCESS => {
    "changed": false,
    "name": [
        "git"
    ],
    "rc": 0,
    "state": "absent",
    "update_cache": false
}
rocky | SUCCESS => {
    "changed": false,
    "msg": "Nothing to do",
    "rc": 0,
    "results": []
}
debian | SUCCESS => {
    "changed": false
}
```

nmap

```sh
ansible all -m package -a "name=nmap state=absent"
```

```
suse | CHANGED => {
    "changed": true,
    "cmd": [
        "/usr/bin/zypper",
        "--quiet",
        "--non-interactive",
        "--xmlout",
        "remove",
        "--type",
        "package",
        "nmap"
    ],
    "name": [
        "nmap"
    ],
    "rc": 0,
    "state": "absent",
    "stderr": "",
    "stderr_lines": [],
    "stdout": "<?xml version='1.0'?>\n<stream>\n<install-summary download-size=\"0\" space-usage-diff=\"-25883492\" space-usage-installed=\"0\" space-usage-removed=\"25883492\" packages-to-change=\"1\" need-restart=\"0\" need-reboot=\"0\">\n<to-remove>\n<solvable type=\"package\" name=\"nmap\" edition=\"7.94-lp156.1.2\" arch=\"x86_64\" repository=\"@System\" summary=\"Network exploration tool and security scanner\">\n<description>Nmap (&quot;Network Mapper&quot;) is a utility for network exploration or\nsecurity auditing. It may as well be used for tasks such as network\ninventory, managing service upgrade schedules, and monitoring host or\nservice uptime. Nmap uses raw IP packets to determine what hosts are\navailable on the network, what services (application name and\nversion) those hosts are offering, what operating systems (and OS\nversions) they are running, what type of packet filters/firewalls are\nin use, and dozens of other characteristics. It scans large networks,\nand works fine against single hosts.</description></solvable>\n</to-remove>\n</install-summary>\n<prompt id=\"0\">\n<text>Backend:  classic_rpmtrans\nContinue?</text>\n<option default=\"1\" value=\"y\" desc=\"Yes, accept the summary and proceed with installation/removal of packages.\"/>\n<option value=\"n\" desc=\"No, cancel the operation.\"/>\n<option value=\"v\" desc=\"Toggle display of package versions.\"/>\n<option value=\"a\" desc=\"Toggle display of package architectures.\"/>\n<option value=\"r\" desc=\"Toggle display of repositories from which the packages will be installed.\"/>\n<option value=\"m\" desc=\"Toggle display of package vendor names.\"/>\n<option value=\"d\" desc=\"Toggle between showing all details and as few details as possible.\"/>\n<option value=\"g\" desc=\"View the summary in pager.\"/>\n</prompt>\n</stream>\n",
    "stdout_lines": [
        "<?xml version='1.0'?>",
        "<stream>",
        "<install-summary download-size=\"0\" space-usage-diff=\"-25883492\" space-usage-installed=\"0\" space-usage-removed=\"25883492\" packages-to-change=\"1\" need-restart=\"0\" need-reboot=\"0\">",
        "<to-remove>",
        "<solvable type=\"package\" name=\"nmap\" edition=\"7.94-lp156.1.2\" arch=\"x86_64\" repository=\"@System\" summary=\"Network exploration tool and security scanner\">",
        "<description>Nmap (&quot;Network Mapper&quot;) is a utility for network exploration or",
        "security auditing. It may as well be used for tasks such as network",
        "inventory, managing service upgrade schedules, and monitoring host or",
        "service uptime. Nmap uses raw IP packets to determine what hosts are",
        "available on the network, what services (application name and",
        "version) those hosts are offering, what operating systems (and OS",
        "versions) they are running, what type of packet filters/firewalls are",
        "in use, and dozens of other characteristics. It scans large networks,",
        "and works fine against single hosts.</description></solvable>",
        "</to-remove>",
        "</install-summary>",
        "<prompt id=\"0\">",
        "<text>Backend:  classic_rpmtrans",
        "Continue?</text>",
        "<option default=\"1\" value=\"y\" desc=\"Yes, accept the summary and proceed with installation/removal of packages.\"/>",
        "<option value=\"n\" desc=\"No, cancel the operation.\"/>",
        "<option value=\"v\" desc=\"Toggle display of package versions.\"/>",
        "<option value=\"a\" desc=\"Toggle display of package architectures.\"/>",
        "<option value=\"r\" desc=\"Toggle display of repositories from which the packages will be installed.\"/>",
        "<option value=\"m\" desc=\"Toggle display of package vendor names.\"/>",
        "<option value=\"d\" desc=\"Toggle between showing all details and as few details as possible.\"/>",
        "<option value=\"g\" desc=\"View the summary in pager.\"/>",
        "</prompt>",
        "</stream>"
    ],
    "update_cache": false
}
rocky | CHANGED => {
    "changed": true,
    "msg": "",
    "rc": 0,
    "results": [
        "Removed: nmap-3:7.92-3.el9.x86_64"
    ]
}
debian | CHANGED => {
    "changed": true,
    "stderr": "",
    "stderr_lines": [],
    "stdout": "Reading package lists...\nBuilding dependency tree...\nReading state information...\nThe following packages were automatically installed and are no longer required:\n  git-man libblas3 liberror-perl liblinear4 liblua5.3-0 libpcap0.8 libpcre3\n  lua-lpeg nmap-common patch\nUse 'sudo apt autoremove' to remove them.\nThe following packages will be REMOVED:\n  nmap\n0 upgraded, 0 newly installed, 1 to remove and 0 not upgraded.\nAfter this operation, 4540 kB disk space will be freed.\n(Reading database ... \r(Reading database ... 5%\r(Reading database ... 10%\r(Reading database ... 15%\r(Reading database ... 20%\r(Reading database ... 25%\r(Reading database ... 30%\r(Reading database ... 35%\r(Reading database ... 40%\r(Reading database ... 45%\r(Reading database ... 50%\r(Reading database ... 55%\r(Reading database ... 60%\r(Reading database ... 65%\r(Reading database ... 70%\r(Reading database ... 75%\r(Reading database ... 80%\r(Reading database ... 85%\r(Reading database ... 90%\r(Reading database ... 95%\r(Reading database ... 100%\r(Reading database ... 35285 files and directories currently installed.)\r\nRemoving nmap (7.93+dfsg1-1) ...\r\nProcessing triggers for man-db (2.11.2-2) ...\r\n",
    "stdout_lines": [
        "Reading package lists...",
        "Building dependency tree...",
        "Reading state information...",
        "The following packages were automatically installed and are no longer required:",
        "  git-man libblas3 liberror-perl liblinear4 liblua5.3-0 libpcap0.8 libpcre3",
        "  lua-lpeg nmap-common patch",
        "Use 'sudo apt autoremove' to remove them.",
        "The following packages will be REMOVED:",
        "  nmap",
        "0 upgraded, 0 newly installed, 1 to remove and 0 not upgraded.",
        "After this operation, 4540 kB disk space will be freed.",
        "(Reading database ... ",
        "(Reading database ... 5%",
        "(Reading database ... 10%",
        "(Reading database ... 15%",
        "(Reading database ... 20%",
        "(Reading database ... 25%",
        "(Reading database ... 30%",
        "(Reading database ... 35%",
        "(Reading database ... 40%",
        "(Reading database ... 45%",
        "(Reading database ... 50%",
        "(Reading database ... 55%",
        "(Reading database ... 60%",
        "(Reading database ... 65%",
        "(Reading database ... 70%",
        "(Reading database ... 75%",
        "(Reading database ... 80%",
        "(Reading database ... 85%",
        "(Reading database ... 90%",
        "(Reading database ... 95%",
        "(Reading database ... 100%",
        "(Reading database ... 35285 files and directories currently installed.)",
        "Removing nmap (7.93+dfsg1-1) ...",
        "Processing triggers for man-db (2.11.2-2) ..."
    ]
}
```

```sh
ansible all -m package -a "name=nmap state=absent"
```

```
rocky | SUCCESS => {
    "changed": false,
    "msg": "Nothing to do",
    "rc": 0,
    "results": []
}
debian | SUCCESS => {
    "changed": false
}
suse | SUCCESS => {
    "changed": false,
    "name": [
        "nmap"
    ],
    "rc": 0,
    "state": "absent",
    "update_cache": false
}
```

- Copiez le fichier `/etc/fstab` du _Control Host_ vers tous les _Target Hosts_ sous forme d'un fichier `/tmp/test3.txt`.

```sh
ansible all -m copy -a "src=/etc/fstab dest=/tmp/test3.txt"
```

```
debian | CHANGED => {
    "changed": true,
    "checksum": "0fe1d6fcaf1695fb3ef9d8a42d45d04e5e0c11c2",
    "dest": "/tmp/test3.txt",
    "gid": 0,
    "group": "root",
    "md5sum": "31623c38118cbe8247061a6bd3f239a4",
    "mode": "0644",
    "owner": "root",
    "size": 679,
    "src": "/home/vagrant/.ansible/tmp/ansible-tmp-1762426441.2849739-6619-274689494565799/source",
    "state": "file",
    "uid": 0
}
rocky | CHANGED => {
    "changed": true,
    "checksum": "0fe1d6fcaf1695fb3ef9d8a42d45d04e5e0c11c2",
    "dest": "/tmp/test3.txt",
    "gid": 0,
    "group": "root",
    "md5sum": "31623c38118cbe8247061a6bd3f239a4",
    "mode": "0644",
    "owner": "root",
    "secontext": "unconfined_u:object_r:user_home_t:s0",
    "size": 679,
    "src": "/home/vagrant/.ansible/tmp/ansible-tmp-1762426441.290878-6618-171127139765770/source",
    "state": "file",
    "uid": 0
}
suse | CHANGED => {
    "changed": true,
    "checksum": "0fe1d6fcaf1695fb3ef9d8a42d45d04e5e0c11c2",
    "dest": "/tmp/test3.txt",
    "gid": 0,
    "group": "root",
    "md5sum": "31623c38118cbe8247061a6bd3f239a4",
    "mode": "0644",
    "owner": "root",
    "size": 679,
    "src": "/home/vagrant/.ansible/tmp/ansible-tmp-1762426441.302528-6620-45163697859709/source",
    "state": "file",
    "uid": 0
}
```

```sh
ansible all -m copy -a "src=/etc/fstab dest=/tmp/test3.txt"
```

```
rocky | SUCCESS => {
    "changed": false,
    "checksum": "0fe1d6fcaf1695fb3ef9d8a42d45d04e5e0c11c2",
    "dest": "/tmp/test3.txt",
    "gid": 0,
    "group": "root",
    "mode": "0644",
    "owner": "root",
    "path": "/tmp/test3.txt",
    "secontext": "unconfined_u:object_r:user_home_t:s0",
    "size": 679,
    "state": "file",
    "uid": 0
}
debian | SUCCESS => {
    "changed": false,
    "checksum": "0fe1d6fcaf1695fb3ef9d8a42d45d04e5e0c11c2",
    "dest": "/tmp/test3.txt",
    "gid": 0,
    "group": "root",
    "mode": "0644",
    "owner": "root",
    "path": "/tmp/test3.txt",
    "size": 679,
    "state": "file",
    "uid": 0
}
suse | SUCCESS => {
    "changed": false,
    "checksum": "0fe1d6fcaf1695fb3ef9d8a42d45d04e5e0c11c2",
    "dest": "/tmp/test3.txt",
    "gid": 0,
    "group": "root",
    "mode": "0644",
    "owner": "root",
    "path": "/tmp/test3.txt",
    "size": 679,
    "state": "file",
    "uid": 0
}
```

- Supprimez le fichier `/tmp/test3.txt` sur les _Target Hosts_ en utilisant le module `file` avec le paramètre `state=absent`.

```sh
ansible all -m file -a "path=/tmp/test3.txt state=absent"
```

```
debian | CHANGED => {
    "changed": true,
    "path": "/tmp/test3.txt",
    "state": "absent"
}
rocky | CHANGED => {
    "changed": true,
    "path": "/tmp/test3.txt",
    "state": "absent"
}
suse | CHANGED => {
    "changed": true,
    "path": "/tmp/test3.txt",
    "state": "absent"
}
```

```sh
ansible all -m file -a "path=/tmp/test3.txt state=absent"
```

```
rocky | SUCCESS => {
    "changed": false,
    "path": "/tmp/test3.txt",
    "state": "absent"
}
debian | SUCCESS => {
    "changed": false,
    "path": "/tmp/test3.txt",
    "state": "absent"
}
suse | SUCCESS => {
    "changed": false,
    "path": "/tmp/test3.txt",
    "state": "absent"
}
```

- Enfin, affichez l'espace utilisé par la partition principale sur tous les _Target Hosts_. Que remarquez-vous ?

```sh
ansible all -m command -a "df -h /"
```

![Capture d'écran de l'espace utilisé par la partition principale](taille_disque.png)

- Quittez le Control Host et supprimez toutes les VM de l'atelier.

```sh
exit
vagrant destroy -f
```
