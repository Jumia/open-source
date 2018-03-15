How to Open Source at Jumia
==================

A guide to releasing an open-source project at [Jumia](https://group.jumia.com), The leading e-commerce ecosystem in Africa. Please feel free to use this as a template for your own organization's open source planning, policymaking, and development efforts. If there's a topic we've missed, or if you have any suggestions for making this better, let us know via our Issues tracker. 

We're really grateful to [Zalando](http://zalando.com) for creating a great documentation on how to companies should open source. This document is based on that guide.

**Note:** All the files inside templates folder are only for reference and must be adapted to the project reality.

### Why Open Source?

Because it can: improve quality, mitigate risk, increase trust, save us money, expand our technology choices, be fun, enable us to give back to the community, strengthen our tech brand, and attract talent.

### Our Open Source First Principles

**Vision**: 
*We strongly believe that open source software benefits the tech community, and that providing broadly useful code to the world is a virtue. We strive to work in an open source way to the betterment of Jumia and the world.*

- **Do “Open Source First”**: If your Jumia project can also be useful to non-Jumia, consider releasing it as open source and ask for guidance.
- **Take Ownership**: Your team is responsible for ensuring that it’s possible to open-source your project. Your lead is available for guidance.
- **Be Safe**: To ensure the broadest possible use of your project, use the MIT License only.
- **Deliver Quality**: Provide a great out-of-the-box experience.
- **Provide Documentation**: Include a clear README and default working configuration.
- **Stay Secure**: Make sure your project doesn’t include Jumia specifics, such as credentials and private identifiers.
- **Ask for Help**: Find colleagues to brainstorm ideas for your project and to review your work.
- **Promote**: Tell the world about your project via blog posts, social media and conference talks.
- **Join the Open Source Team**: Help us make open source stronger at Jumia! Come on, it'll be fun. :)

### Project Design

#### What to Ask (and Answer) Before You Open Source

- Who cares?
- Are we still using it?
- Are we committed to it?
- Can it be developed in one public tree?

#### Never open-source these:
- PCI DSS-related projects: e.g. payment services
- Jumia-specific projects: things tightly coupled to/dependent upon our systems
- Projects you don't plan to maintain and grow a community around
- Domain knowledge
- Customer data
- Anything that would risk our competitive advantage. This typically means technologies we build that are intrinsic to generating or reinforcing the uniqueness of our customer experience, and that—if made public—would enable our competitors to implement it and erase our uniqueness. This could be:
  - confidential source code
  - recommendation algorithms
  - search functionalities that give us an edge over competitors

If you're open-sourcing a project that has contained sensitive information in the past, the sensitive information can still be retrieved from the Git commit history. Create an entirely new Git repo for it before pushing it to GitHub.

No issues? Great! On to the next section ...

### Our Main GitHub Org and InnerSource

The InnerSource is where your Jumia project will first appear public within the company. It is a proving ground for brand-new projects that meet all the above criteria. It is where we can experiment and publish projects that show clear promise of being useful to others because they are A) out-of-the-box usable to non-Jumia project and B) highlight a compelling technical challenge that we are solving with software.

InnerSource projects are the repositories we use internally at 
Jumia. They appear on /Jumia, and are not accessible to the public. No one outside of Jumia Tech can see or contribute to them. 

The steps to open-source a project are:
1. Get approval from your manager if you identify a open-sourceable project
1. Request to Jumia Open-source Team a repository 
1. Project will be in InnerSource until it respects all standards to open-source it.
1. Project is open-sourced under /Jumia organization

The next sections offer more details on differences between open source and “coding in the open”.

#### The Main Org and What Makes a Project “Open Source”

Jumia's main GitHub organization is [/Jumia](https://github.com/Jumia). This organization is reserved for projects meeting these criteria:
- **does it build**.
- **is useful beyond Jumia**. It is free of Jumia dependencies and simple for a non-Jumia to install and start using.
- **has user-friendly documentation** that is up-to-date and clear about what the project does, and how to install/start/configure/run it. ([This template can help you](Templates/README.md).)
- **is tested**. It has automated tests and takes advantage of test coverage.
- **is under active development**, or is stable enough to be considered a “finished” product. If the project is incomplete, at least one maintainer has worked on it in the last three months. If it’s stable and doesn’t require constant maintenance, you’ve stated as much in your README.
- **is innovative**. If it duplicates an existing project, it does at least one thing better, faster, differently, etc., or is higher-quality.
- **meets our non-negotiable guidelines** regarding security and compliance. You need to include a LICENSE.md, for example.
- **is an MVP**. It either meets or surpasses “minimum viable product” status. An outside developer could use it and even contribute to it. If it’s buggy or very early-stage, it includes a brief development status in the intro stating as much. (This template can help you.)
- **has a CONTRIBUTING.md.** For a template, [go here](Templates/CONTRIBUTING.md).
- **has a plan**. Its maintainers care about making it a success. They commit to responding to PRs and issues in a timely manner (48-72 hours), thank contributors, and convert quality contributors to trusted maintainers as appropriate. If you need some guidance, check out [Mozilla's helpful resources](https://mozilla.github.io/open-leadership-training-series/articles/open-project-maintenance/open-project-maintenance/) on this topic.


**Wait, I thought we were “Open Source First.” Doesn’t keeping repos on GHE contradict that?**

Nope. Not every project we create is appropriate for sharing publicly. Some projects will be [too sensitive for publication](https://github.com/Jumia/open-source#never-open-source-these). Other projects would act as “noise,” because they are too tightly coupled to what we do internally. An organization's open source footprint says a lot about that organization, especially if the org cannot maintain a good signal-to-noise ratio.

However, we still want you to share these projects inside Jumia, on GHE. This is why we advocate the InnerSource collaboration model. InnerSource operates just like open-source in that project teams invite, accept and reject PRs; provide quality documentation; and build them gradually. The main difference is that InnerSource is limited to Jumia Tech. Make your GHE organization open to other internal teams so they can find out about your work, fix bugs, make PRs, and even add features that your own team currently has no time to develop. 

We request that you use private GHE repositories only if they include sensitive information that can't store elsewhere.


##### How to InnerSource
[Here's our homegrown how-to](innersource.md) with materials to get you started.

## Project Basics

### Code Review

Ask your team and other peers to:
- review your code
- install and
- test your project prior to public release. 

Not sure what to ask for, or how to peer-review? This list of [11 best practices](https://smartbear.com/learn/code-review/best-practices-for-peer-code-review/) should help.

### Creating a README

#### Do:
- [Use this checklist](Templates/README.md). 
- Break up text often, for better readability.
- Think about SEO.

#### Don't:
- Refer to Jumia specifics, such as internal teams and processes
- Include large chunks of code without explaining what they represent
- Include any code that presents security vulnerabilities

#### Syntax and Formatting
Markdown is the simplest and most easily understood syntax; we recommend using it for all your documentation. However, we realize that there are exceptions: PyPi, for example, uses reStructuredText, and the Python community in general doesn’t use Markdown. If Markdown isn’t practical, then we recommend using only one [GitHub-supported](https://github.com/github/markup#markups) markup format.

### Official Namespace

The official namespace for our projects is ‘**Jumia/**’, ‘**org.jumia**’, where applicable.

### Applying Changes

All repository changes, including those made by maintainers, should come from GitHub pull requests so that we can streamline review and change tracking (as per [GitHub Flow](https://guides.github.com/introduction/flow/)). Everyone should have their own fork, though you can still edit READMEs/documentation/related files with the GitHub “Edit” button. The ‘master’ branch should be the accepted development head; pull requests get merged there.

### Versioning

Version all project artifacts should be [semantically](http://semver.org/). Tag all versions in GitHub with the exact version name (like ‘0.1.0’; do not prefix tags with “v.” or similar). For a better user experience, use the GitHub “release notes” feature to add notes whenever you change something in the new version.

### Maintainers

Maintainers are the contact people for a project. They are also the only contributors who can package new versions and apply changes to the repository (i.e., merge pull requests). Every project must have at least one maintainer.

The Jumia Open Source Team reserves the right to contact maintainers to ensure a project remains active/maintained. If the project is not being maintained, we will work with you to either find a new maintainer or remove the project from our organization page. Please be responsive to all internal queries about your project and its status.

#### Create a Maintainers File

Every project needs a ‘MAINTAINERS’ file (listing all maintainers) at its root. 
Format:

     [full name] <email address>
     [second full name] <email address>
     etc.

#### Be Prompt and Responsive

Respond promptly to pull requests and issues. “Within 72 hours” is a good window. Open issues do not make your project “look popular.” Instead, they make it look like you're neglecting your project. If project workload becomes unmanageable, ask the Jumia Opensource Team or the community for help.

If you are away/on vacation and can’t respond to PRs/issues promptly, find someone who can.

If you're not going to accept a PR, reject it ASAP and include a brief explanation why.

If you're feeling maintainer burnout or facing some trolling behavior, give Jon Schinklert's [Maintainers Guide to Staying Positive](https://github.com/jonschlinkert/maintainers-guide-to-staying-positive) a read; it might help you to feel better.

#### Use Issues Creatively
Issues can be good for planning or for onboarding contributors. Issues should include a description of the point, question, discovery, or other detail prompting the issue.

Issues that consist solely of a title appear unprofessional and do not do much to invite discussion from the community.

Label your issues with clear tags. This is a great way to organize and categorize issues.

#### Provide a Pull-Request Template

The Issues Tracker is the entry point for onboarding contributors, so use our [pull request template](pull_request_template.md) to create a roadmap for your project or to track bugs. A pull request template improves development quality and provides a common guideline for contributors to follow. It also enables you to reference issues and shows others your development progress.

Add a `PULL_REQUEST_TEMPLATE.md` into the root of your project folder. Once you merge it, every new pull request will use this template. [GitHub's help section](https://help.github.com/articles/creating-a-pull-request-template-for-your-repository/) offers a step-by-step guide with more information about PR templates.

### Stay Secure
##### Two-Factor Authentication Is Required
GitHub organization members must enable [Two-Factor Authentication (2FA/MFA)](https://help.github.com/articles/about-two-factor-authentication/) in keeping with our Open Source First principle to "Stay Secure." Read [GitHub's post on 2FA](https://help.github.com/articles/about-two-factor-authentication/) for more information.

Don't have a smartphone, and/or want to give your phone number to GitHub? According to GitHub support, SMS or a TOTP app are currently the only primary 2FA methods that work. There are mobile and desktop TOTP apps that also work. See [GitHub's article on 2FA via TOTP apps](https://help.github.com/articles/configuring-two-factor-authentication-via-a-totp-mobile-app/) for more information. You can set up 2FA with a Google Voice SMS number, but should add a U2F device as backup.

### About Licensing

#### Quick FAQ

##### Which license do we use?
[The MIT license](https://opensource.org/licenses/MIT). MIT is succinct, straightforward, and easy use in closed-source projects. It allows the most broad usage of our source code, and keeps open-sourcing easy and safe. You must include a separate license file in your repository with the entire text of the MIT license included. 

If your project uses the MIT license and incorporates third-party OSS components, then you must attach this sentence in your license file: “This software is licensed under the MIT license (see below), unless otherwise stated in the license files in higher directories (if any)." Please also provide the license files for every third-party source you add.

[This helpful blog post](https://writing.kemitchell.com/2016/09/21/MIT-License-Line-by-Line.html) breaks down the license line by line for you. (If you're really interested in open source licensing, check out [Rosenlaw & Einschlag's free online book](http://www.rosenlaw.com/oslbook.htm) and/or [O'Reilly's/Andrew M. St. Laurent's](http://www.oreilly.com/openbook/osfreesoft/book/). These are a little dated, but still useful.)

##### Must I use MIT?
Yes, for all newly created open-source projects.

##### I don't like the MIT license. Can I use another license?

Not without a compelling reason.

##### What if I fork an external project and/or contribute to it?

Keep the original license.

##### I'm open-sourcing a library. What should I do?
Consider using a weak copyleft license that won’t restrict the software that uses it to the same license; will allow usage in closed source software; and will potentially increase the number of users and contributors.

##### What if my team uses an external project whose license is not Jumia-recommended?

You can use GPL code — but only internally. Be sure it's a version of the GPL that continues to allow for the ASP loophole. AGPL and versions of the GPL with additional restrictions won't work.

##### Who is the license owner?

Jumia

##### Does my project need a LICENSE file?

Yes, at the root of the repository that contains the copy of the selected license (see above). [Here is an example](https://opensource.org/licenses/MIT) for MIT.

##### Do I need to add a license header to every source file?

No. In fact, we discourage it because it blows up file sizes, requires some build checking/pre-processing. It's also not needed for the licenses we use. Having one `LICENSE` file in the repository is enough.

##### What about a README note?

Yep. Every README{.md,.rst} file must state the following at the end:

>The MIT License (MIT)
>Copyright © [yyyy] Jumia, https://group.jumia.com/

>Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

>The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

>THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
>

Replace the [yyyy] field with the year that you created the project, and do not update it. Do not provide multiple years.

##### I still have licensing questions. What can I do?

Ask the Open Source Team or your manager. 

#### Repository of Meta Information

Many package managers include a feature to make the applied license machine readable. Use these! An example for [Maven](https://maven.apache.org/pom.html#Licenses):

```xml
<licenses>
    <license>
        <name>MIT</name>
        <url>https://opensource.org/licenses/MIT</url>
        <distribution>repo</distribution>
    </license>
</licenses>
```

An example for [Node](https://docs.npmjs.com/files/package.json#license), according to [this](https://gist.github.com/robertkowalski/7620849):

```
“license”: “MIT”
```
An example for Scala (with sbt):
```
licenses += ("MIT", url("http://opensource.org/licenses/MIT"))
```

An example for PHP (with composer):
```json
{
    "license": "MIT"
}
```
https://getcomposer.org/doc/04-schema.md#license

#### Restrictions Imposed by the License
“Dependency” typically means “being linked with,” “included in your artifact,” or “depends on it during runtime.” Dependencies can limit you. To remain in compliance, check the licenses of your projects. Your build tool’s license does not affect your software’s license. A jar file or Python dependency will affect your software.

#### There Is No License

If there is no license statement, the author automatically receives a copyright. [This](http://choosealicense.com/no-license/) implies that no one has the right to modify or redistribute the software. If you really need the software, contact the author (who is likely unaware) and ask him/her to provide a proper license.

### Other Repository Information

#### JVM Artifacts
Host JVM artifacts (*.jar) on Maven Central in [the ‘org.jumia’ group](https://repo1.maven.org/maven2/org/jumia/). To do this, get a [Sonatype](http://central.sonatype.org/) account. If you don't have an account yet, register with Sonatype using your Jumia email address.

If you want to push to Sonatype but not to *.jumia, register a different Sonatype account with a non-jumia email address.

#### Python Packages
Host Python packages on [PyPI](https://pypi.python.org/pypi/) (PyPI has no namespaces) and make sure that multiple persons have “maintainer” rights.

#### Node Modules
[Node](https://www.npmjs.com/) modules [now have namespaces](http://blog.npmjs.org/post/116936804365/solving-npms-hard-problem-naming-packages). Prefix them with a short product name: e.g. [karma](https://karma-runner.github.io/0.12/index.html) plugins are prefixed “karma-”; the same goes for gulp, grunt, etc. Host your Node modules in the public NPM registry. Here is [how to publish to NPM](https://gist.github.com/coolaj86/1318304).

#### Docker Images
You can currently browse it [here](https://hub.docker.com/u/jumia/). 
Even if pushed to local registries the generally available image should always be on docker hub too in order to maximize contribution to the community as well as a fallback registry. Automated builds should be set from our github repositories at all times.

### Working with External Contributors

The Open source Team enthusiastically supports you in recruiting non-Jumia to contribute to your project. Collaboration and community are part of the fun of open source. 

Give GitHub's ["Creating a new contributor on-ramp" doc](https://github.com/blog/2128-creating-a-new-contributor-on-ramp) a look for some expert guidance. (TL;DR version = be welcoming, inclusive, and clear about what sorts of contributions you're looking for most).

Please ask external contributors to sign a contributor licensing agreement (CLA). A few good models to follow and adapt: [.Net Foundation](https://cla2.dotnetfoundation.org/) example (electronic submission via GitHub account); [Google’s CLA](https://github.com/angular/angular.js/blob/master/CONTRIBUTING.md#-signing-the-cla) for contributing to AngularJS is a simple click-through form with a Googlebot that automatically checks for signatures; Selenium/Software Freedom Conservancy uses a [Google form](https://docs.google.com/a/zalando.de/forms/d/11Z8LoYpTGUIwCegifVH1YtL9smxVDNk-fOykUZTAWhE/viewform?hl=en_US&formkey=dFFjXzBzM1VwekFlOWFWMjFFRjJMRFE6MQ#gid=0).

### Deprecate Responsibly

#### How to Deprecate
Add “Deprecated” at the top of your README, as well as a notice stating your plans for the project: deletion, finding a new owner, etc.

After announcing your decision to deprecate the project:
   - notify your users. Put a notice on your README.
   - Wait 60 days.
   - Try to find a new owner. Internal options first, then seek an external owner. Ask the Open Source Team for help.
   - Try to find an external owner. More guidance on this to come soon; for now, alert the Open Source Team of any such plans.

#### Tips for Finding a New Owner
Internally, you can use internal mailing lists and HipChat to announce your need. Externally, social media platforms and community boards work well. Add 1-2 sentences to your announcements suggesting how your project might have potential to evolve into something bigger and better.

### Project Promotion

#### Proactively Communicate
Share your project with:
- relevant LinkedIn Groups
- community forums/boards
- e-newsletters and websites/newsletters dedicated to the problem(s) your project is trying to solve, the relevant languages, etc.
- if you have contacts at a university, pitch your project to their students
- major players in the industry

### Contributing to Non-Jumia Open-Source Projects

We encourage you to contribute to other open-source projects in ways that benefit Jumia. Some ways you might contribute:

- making bug fixes to projects you're using on the job
- submitting a patch or change to a language (for example, [Clojure](http://clojure.org/community/contributing))
- pitching a feature request that your team/dept needs to a project we're using, getting confirmation from the maintainers to go forward, and doing the work
  - a good idea is to review the project's GitHub Issues Tracker to see if anyone else has made the same feature request; restart that conversation and see if you can get them + others to work collaboratively to make the needed change 

#### How to Become a Contributor

Before writing a line of code to change a project, we highly recommend reaching out to the project maintainers via the Issues Tracker and letting them know about your plans (many projects already require this as a first step). There might already be an issue filed that matches your needs, and/or someone working on the changes you're recommending. You don't ever want to invest a lot of time and work into making a change, only to have the project maintainers reject it as out of scope. This will frustrate you, and it will frustrate them.

These articles from others in the community provide more detailed advice for getting started:

- [How to Become an Amazing Contributor](https://opensource.com/life/11/3/how-become-amazing-contributor-open-source-project) by Daniel Doubrovkine for opensource.com/RedHat
- [How to Contribute to Open Source Projects](http://www.drdobbs.com/open-source/how-to-contribute-to-open-source-project/231000080) by Brian Behlendorf for Dr. Dobb's
- [The Eight Essential Traits of a Great Open Source Contributor](https://blog.newrelic.com/2014/10/21/open-source-contributors/) by Ander Lester/New Relic
- [14 Ways to Contribute to Open Source Without Being a Programming Genius or a Rock Star](http://blog.smartbear.com/programming/14-ways-to-contribute-to-open-source-without-being-a-programming-genius-or-a-rock-star/) also by Andy Lester, this time for SmartBear

#### How to Become a Core Contributor

Ah, so you want to get more serious about contributing! Excellent. Becoming a core contributor to a major project is a fantastic way to learn from others, grow your network and keep the open source infrastructure we depend on strong and reliable. Others in the general open source community have written great how-to's on this topic. Here are a few:

- [Tips for Becoming a Core Contributor](https://www.wordfugue.com/tips-becoming-core-contributor/) by Philip James 
- [On Becoming a Core Contributor](http://glasnt.com/blog/2016/06/08/on-becoming-a-core-contributor.html) by Katie McLaughlin
- [Apache Software Foundation's how-to](https://community.apache.org/contributors/), including "Moving From Contributor to Committer," [FAQ](https://www.apache.org/dev/committers.html) and [guide](https://www.apache.org/dev/new-committers-guide.html)

Please let the Jumia Open source team know about your external contributions so we can help you get the recognition and support you deserve.
