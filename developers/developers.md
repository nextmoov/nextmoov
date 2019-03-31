
# For Developers

We made it clear [already](/nextmoov): we want to use the best tools only along with some strong coding conventions to smooth our collaboration.

As of today (20181224 🎄), here is a list of the MUST and SHOULD tools we use:

*   All our private codebases are stored in Bitbucket so you'll definitely get your own access to it. As soon as the first line of code is written, all our projects must use Git and they must be pushed to BitBucket. They must be pushed at least every Friday at 13:00 as the full completion of tasks assigned to that week for you will only be judged upon code pushed online.
*   Our infrastructure runs on Docker + Rancher + Drone + Sentry + Traefik and is hosted on servers provided by DigitalOcean.  \
[If you want to learn more about it.](https://docs.google.com/document/d/1gSAxu_PtrcKic1PAhEltk6zUNjKFZ49bMxTeOvfcIWk/edit)
*   We warmly recommend you Atom or VSCode as IDEs and, in any case, find a way to lint your code according to our standards (see next).
*   We use the Uneo bootstrap as template for our websites.

Code-wise, you should use UNIX line breaks and two-spaces indent, and you should use our preset configurations for IDEs. All our repositories must follow [Conventional Commits](http://conventionalcommits.org/) inspired by [AngularJS](https://docs.google.com/document/d/1QrDFcIiPjSLDn3EL15IJygNPiHORgU1_OOAqWjiDU5Y/preview).