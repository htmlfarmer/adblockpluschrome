PornBlocker Secure (project specification and code)
==========================================================

PornBlocker Secure (fork) goal is to develop a new "startup" of distributed (non centralized) security research tools for the web browser that focuses on ARTIFICIAL INTELLIGENCE and "porn" and "ad's" as well as EMERGENCY REAL TIME SURGERY in javascript of the webbrowser.  Advanced mathmatics can also be used to detect problems in browser real time! The new port seeks to bridge localized in browser research NLP with a centralized AdBlocker database.  A centralized security system fails to account for localized human expectations and centralized security can also fail at a global level.

Using a variety of simple text analytics it should be possible to greatly increase global security.

Frequency of static and dynamic program analysis to identify malicious, dangerous, and privacy infringing functionality in a webpage. This simple add in browser security features is beyond the default AdBlocker perspective.  The Security Plugin’s goal is to help the user and primarily focus on value.  With the success of the like “only” button on facebook it is proposed to build up the reputation of a website and focus the analytics primarily on the positive.

We combine Natural Language Processing (NLP) text analysis with computer security.  The AdBlocker plugin has already provided useful higher dimensional popular techniques for improving web pages.  Simple Natural Language Processing (NLP) without the use of dangerous algorithms to the user. 

#health #police #pornography #javascript 
The problems in Artificial Intelligence can be solved easier if we have a "AI BLOCKER" or "PORN BLOCKER" in browser.

Here is a new software project that works for "blocking ads" however, we need money to help develop the code ... however, the code is mostly "in browser" and basic HTML/Javascript.  

(the nice part of this project is a lot of the code is already written!  its just a fork of the adblocker project that detects PORN and new problems in AI)

this problem most likely will be solved by private industry... that is the problems in "online CHAT BOTS".  clearly the police are not helping... (or the "good" police don't know how to help?). the GOOD news is that people like you and me can have our own browser settings and solve this problem or help.

Anyway... this is just a sample page for a project if anyone wants to try and do a new startup or checkout the internal code and build their own local "adblocker that is a pornblocker and eventually AI blocker". 

(feel free to "like" this link or comment if your interested in helping with this new project...)

This repository contains the platform-specific Adblock Plus source code for
Chrome, Opera, Microsoft Edge and Firefox. It can be used to build
Adblock Plus for these platforms, generic Adblock Plus code will be extracted
from other repositories automatically (see _dependencies_ file).

Note that the Firefox extension built from this repository is the new
[WebExtension](https://developer.mozilla.org/en-US/Add-ons/WebExtensions).
The source code of the legacy Adblock Plus extension
can be found [here](https://hg.adblockplus.org/adblockplus).

Building
---------

### Requirements

- [Mercurial](https://www.mercurial-scm.org/) or [Git](https://git-scm.com/) (whichever you used to clone this repository)
- [Python 2.7](https://www.python.org)
- [The Jinja2 module](http://jinja.pocoo.org/docs) (>= 2.8)
- [The PIL module](http://www.pythonware.com/products/pil/)
- For signed builds: [PyCrypto module](https://www.dlitz.net/software/pycrypto/)

### Building the extension

Run one of the following commands in the project directory, depending on your
target platform:

    ./build.py build -t chrome -k adblockpluschrome.pem
    ./build.py build -t edge
    ./build.py build -t gecko

This will create a build with a name in the form
_adblockpluschrome-1.2.3.nnnn.crx_, _adblockplusedge-1.2.3.nnnn.appx_ or
_adblockplusfirefox-1.2.3.nnnn.xpi_.

Note that you don't need an existing signing key for Chrome, a new key
will be created automatically if the file doesn't exist.

The Microsoft Edge build _adblockplusedge-1.2.3.nnnn.appx_ is unsigned and
is only useful for uploading into Windows Store, where it will be signed. For
testing use the devenv build.

The Firefox extension will be unsigned, and therefore is mostly only useful for
upload to Mozilla Add-ons. You can also also load it for testing purposes under
_about:debugging_ or by disabling signature enforcement in Firefox Nightly.

### Development environment

To simplify the process of testing your changes you can create an unpacked
development environment. For that run one of the following commands:

    ./build.py devenv -t chrome
    ./build.py devenv -t edge
    ./build.py devenv -t gecko

This will create a _devenv.*_ directory in the repository. You can load the
directory as an unpacked extension, under _chrome://extensions_ in Chrome,
under _about:debugging_ in Firefox or in _Extensions_ menu in Microsoft Edge,
after enabling extension development features in _about:flags_.
After making changes to the source code re-run the command to update the
development environment. In Chrome and Firefox the extension should reload
automatically after a few seconds.

Builds for Microsoft Edge do not automatically detect changes, so after
rebuilding the extension you should manually force reloading it in Edge by
hitting the _Reload Extension_ button.

The build script calls the ensure_dependencies script automatically to manage
the dependencies (see _dependencies_ file). Dependencies with local
modifications won't be updated. Otherwise during development specifying a
feature-branch's name for a dependency's revision is sometimes useful.
Alternatively dependency management can be disabled completely by setting the
_SKIP_DEPENDENCY_UPDATES_ environment variable, for example:

    SKIP_DEPENDENCY_UPDATES=true ./build.py devenv -t chrome

Running the unit tests
----------------------

To verify your changes you can use the unit test suite located in the _qunit_
directory of the repository. In order to run the unit tests go to the
extension's Options page, open the JavaScript Console and type in:

    location.href = "qunit/index.html";

The unit tests will run automatically once the page loads.

Linting
-------

You can lint the code using [ESLint](http://eslint.org).

    eslint *.js lib/ qunit/ ext/ chrome/

You will need to set up ESLint and our configuration first, see
[eslint-config-eyeo](https://hg.adblockplus.org/codingtools/file/tip/eslint-config-eyeo)
for more information.
