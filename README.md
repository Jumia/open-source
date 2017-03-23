<p align="center"><img src="https://about.jumia.com/img/logo.png"></p>
<p align="center">
    <a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/license.svg" alt="License"></a>
</p>

How to Open Source at Jumia
==================

A guide to releasing an open-source project at [Jumia](https://www.jumia.com). 
Please feel free to use this as a template for your own organization's open source planning, policymaking, and development efforts. If there's a topic we've missed, or if you have a suggestion for making this better, let us know via our Issues tracker. 

We're really grateful to [Zalando](http://zalando.com) for creating a great documentation on how to companies should open source.

### Why Open Source?

Because it can: improve quality, mitigate risk, increase trust, save us money, expand our technology choices, be fun, enable us to give back to the community, strengthen our tech brand, and attract talent.

### Our Open Source First Principles

**Vision**: 
*We strongly believe that open source software benefits the tech community, and that providing broadly useful code to the world is a virtue. We strive to work in an open source way to the betterment of Jumia and the world.*

- **Do “Open Source First”**: If your Jumia project can also be useful to non-Jumias, release it as open source from the start.
- **Take Ownership**: Your team is responsible for ensuring that it’s possible to open-source your project. Your delivery lead is available for guidance.
- **Share Your Code**: All code shared between teams must be open source.
- **Be Safe**: To ensure the broadest possible use of your project, use the MIT License only.
- **Deliver Quality**: Provide a great out-of-the-box experience.
- **Provide Documentation**: Include a clear README and default working configuration.
- **Stay Secure**: Make sure your project doesn’t include Jumia specifics, such as credentials and private identifiers.
- **Ask for Help**: Find colleagues to brainstorm ideas for your project and to review your work.
- **Promote**: Tell the world about your project via blog posts, social media and conference talks.
- **Join the Open Source Team**: Help us make open source stronger at Jumia! Come on, it'll be fun. :)

### Project Design

#### What to Ask (and Answer) Before You Open Source

Join the Jumia Open Source team on [Slack](https://opensource-jumia.slack.com) and bring answers to these questions:
- Who cares?
- Are we still using it?
- Are we committed to it?
- Can it be developed in one public tree?

#### Never open-source these:

- PCI DSS-related projects: e.g. payment services
- Domain knowledge
- Customer data
- Unique Selling Points (USPs)
- Anything that would risk our competitive advantage. This typically means technologies we build that are intrinsic to generating or reinforcing the uniqueness of our customer experience, and that—if made public—would enable our competitors to implement it and erase our uniqueness. This could be:
  - confidential source code
  - recommendation algorithms
  - search functionalities that give us an edge over competitors 

If you're open-sourcing a project that has contained sensitive information in the past, the sensitive information can still be retrieved from the Git commit history. Create an entirely new Git repo for it before pushing it to GitHub.

No issues? Great! On to the next section ...

### Where to Publish: Public or Incubator?

1. Create your project within your team's organization
1. Talk with OSS Team to review your project. We'll do:
    1. Push to incubator 
    1. Docs review 
    1. Code review 
1. After these checks there are two options:
    1. Keep in Incubator
        1. Stays private - either has company secrets or is rejected in one of the previous rules
    1. Move to public Main Org
        1. Considered by the OSS team to be public ready 

#### What Makes a Project “Open Source”

- **is useful beyond Jumia**. It is free of Jumia dependencies and simple for a non-Jumia to install and start using.
- **has high-quality documentation** that is up-to-date and clear about what the project does.
- **is tested**. It has automated tests and takes advantage of test coverage.
- **is under active development**, or is stable enough to be considered a “finished” product. If the project is incomplete, at least one maintainer has worked on it in the last three months. If it’s stable and doesn’t require constant maintenance, you’ve stated as much in your README.
- **is innovative**. If it duplicates an existing project, it does at least one thing better, faster, differently, etc., or is higher-quality.
- **meets our non-negotiable guidelines** regarding security and compliance. 
- **is an MVP**. It either meets or surpasses “minimum viable product” status. An outside developer could use it and even contribute to it. If it’s buggy or very early-stage, it includes a brief development status in the intro stating as much. (This template can help you.)
- **has a plan**. Its maintainers care about making it a success. They commit to responding to PRs and issues in a timely manner (48-72 hours), thank contributors, and convert quality contributors to trusted maintainers as appropriate. If you need some guidance, check out [Mozilla's helpful resources](https://mozilla.github.io/open-leadership-training-series/articles/open-project-maintenance/open-project-maintenance/) on this topic.

##### Quick Incubator FAQ

###### Why did we make the Incubator?

To support our Open Source First principle, "Share Your Code,” while reserving our main GitHub org for projects useful beyond Jumia.

###### Can you launch a project directly to the Incubator? 

Yes. And you should, if it meets “coding in the open” criteria.

###### Do Incubator projects have to follow our security and compliance guidelines?

Yes, even if we are developing them for Jumias only, “experimental,” etc.

###### Can an Incubator project ever appear in the main Jumia GitHub org?

Absolutely. Even if Incubator projects are not currently useful outside of Jumia, we'd like to think that one day they might be.

###### What happens when you transfer a repo from one org to another?

The URL is re-routed to the new organization (jumia-incubator). All git clone, git fetch, or git push operations targeting the previous location will continue to function as if made on the new location. Links will be transferred to the new repository. 

That said, GitHub strongly recommends that anyone who had a reference to the old link locally change to the new URL. [Read GitHub’s documentation](https://help.github.com/articles/transferring-a-repository/#redirects-and-git-remotes) to learn more.

###### What happens if I “code in the open” on the main org?

The Open Source Team will ask you to transfer the project yourself to the Incubator. If we don’t get any response within 14 days, or if you agree to the transfer but don’t take action within a week (seven days), your project will be relocated to the Incubator for you.

###### Is it possible to transfer GitHub issues from one project to the other? 

No, GitHub doesn’t allow it. (There are migration tools that can copy issues and their comments to another project, but these don't transfer the relevant author info; they assign ownership to the account used by the migration tool.)

###### Is it possible to transfer the ownership of a Github repo to someone else? 
Yes.

## Project Basics

### Code Review

Ask your team and other peers to:
- review your code
- install and
- test your project prior to public release. 

Not sure what to ask for, or how to peer-review? This list of [11 best practices](https://smartbear.com/learn/code-review/best-practices-for-peer-code-review/) should help.

### Creating a README

#### Do:

- [Use this checklist](https://github.com/Jumia/how-to-open-source/READMEtemplate.md). 
- Break up text often, for better readability.
- Think about SEO.

#### Don't:

- Refer to Jumia specifics, such as internal teams and processes
- Include large chunks of code without explaining what they represent
- Include any code that presents security vulnerabilities

#### Syntax and Formatting

Markdown is the simplest and most easily understood syntax; we recommend using it for all your documentation. However, we realize that there are exceptions: PyPi, for example, uses reStructuredText, and the Python community in general doesn’t use Markdown. If Markdown isn’t practical, then we recommend using only one [GitHub-supported](https://github.com/github/markup#markups) markup format.

### Official Namespace

The official namespace for our projects is ‘**org.jumia**’, where applicable.

### Applying Changes

All repository changes, including those made by maintainers, should come from GitHub pull requests so that we can streamline review and change tracking (as per [GitHub Flow](https://guides.github.com/introduction/flow/)). Everyone should have their own fork, though you can still edit READMEs/documentation/related files with the GitHub “Edit” button. The ‘master’ branch should be the accepted development head; pull requests get merged there.

### Versioning

Version all project artifacts should be [semantically](http://semver.org/). Tag all versions in GitHub with the exact version name (like ‘0.1.0’; do not prefix tags with “v.” or similar). For a better user experience, use the GitHub “release notes” feature to add notes whenever you change something in the new version.

### Maintainers

Maintainers are the contact people for a project. They are also the only contributors who can package new versions and apply changes to the repository (i.e., merge pull requests). Every project must have at least one maintainer. This should be described in the project's readme.md

The Open Source Team reserves the right to contact maintainers to ensure a project remains active/maintained. If the project is not being maintained, we will work with you to either find a new maintainer or remove the project from our organization page. Please be responsive to all internal queries about your project and its status.

#### Create a Maintainers File

Every project needs a ‘[MAINTAINERS](https://github.com/Jumia/how-to-open-source/MAINTAINERS.md)’ file (listing all maintainers) at its root.

#### Be Prompt and Responsive

Respond promptly to pull requests and issues. “Within 72 hours” is a good window. Open issues do not make your project “look popular.” Instead, they make it look like you're neglecting your project. If project workload becomes unmanageable, ask the OpenSource Team or the community for help.

If you are away/on vacation and can’t respond to PRs/issues promptly, find someone who can.

If you're not going to accept a PR, reject it ASAP and include a brief explanation why.

If you're feeling maintainer burnout or facing some trolling behavior, give Jon Schinklert's [Maintainers Guide to Staying Positive](https://github.com/jonschlinkert/maintainers-guide-to-staying-positive) a read; it might help you to feel better.

#### Use Issues Creatively

Issues can be good for planning or for onboarding contributors. Issues should include a description of the point, question, discovery, or other detail prompting the issue.

Issues that consist solely of a title appear unprofessional and do not do much to invite discussion from the community.

Label your issues with clear tags. This is a great way to organize and categorize issues.

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

For documents like this how-to, we recommend using [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/).

##### Must I use MIT?

Yes, for all newly created open-source projects.

##### I don't like the MIT license. Can I use another license?

Not without a compelling reason.

##### What if I fork an external project and/or contribute to it?

Keep the original license.

##### I'm open-sourcing a library. What should I do?

Consider using a weak copyleft license that won’t restrict the software that uses it to the same license; will allow usage in closed source software; and will potentially increase the number of users and contributors.

##### What if my team uses an external project whose license is not Jumia-recommended?

You can can use GPL code — but only internally. Be sure it's a version of the GPL that continues to allow for the ASP loophole. AGPL and versions of the GPL with additional restrictions won't work.

##### Who is the license owner?

Jumia

##### Does my project need a LICENSE file?

Yes, at the root of the repository that contains the copy of the selected license (see above). [Here is an example](https://opensource.org/licenses/MIT) for MIT.

##### Do I need to add a license header to every source file?

No. In fact, we discourage it because it blows up file sizes, requires some build checking/pre-processing, and sometimes leads to situations [like this](http://trillian.mit.edu/~jc/humor/ATT_Copyright_true.html). It's also not needed for the licenses we use. Having one `LICENSE` file in the repository is enough.

##### What about a README note?

Yep. Every README{.md,.rst} file must state the following at the end:

>The MIT License (MIT)
>Copyright © [yyyy] Jumia, https://jumia.com

>Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

>The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

>THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
>

Replace the [yyyy] field with the year that you created the project, and do not update it. Do not provide multiple years.

##### I still have licensing questions. What can I do?

Ask the Open Source Team or your delivery lead.

##### But I am a delivery lead.

Ask your department head.

##### But I am a delivery head.

Management can work with Legal to determine Intellectual Property concerns.

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

#### Restrictions Imposed by the License

“Dependency” typically means “being linked with,” “included in your artifact,” or “depends on it during runtime.” Dependencies can limit you. To remain in compliance, check the licenses of your projects. Your build tool’s license does not affect your software’s license. A jar file or Python dependency will affect your software.

##### Unusual Additions

As stated by Jumia Legal, it is OK to use React and other Facebook open-source software projects for Jumia projects.

#### There Is No License

If there is no license statement, the author automatically receives a copyright. [This](http://choosealicense.com/no-license/) implies that no one has the right to modify or redistribute the software. If you really need the software, contact the author (who is likely unaware) and ask him/her to provide a proper license.

### Other Repository Information

#### Python Packages

Host Python packages on [PyPI](https://pypi.python.org/pypi/) (PyPI has no namespaces) and make sure that multiple persons have “maintainer” rights.

#### Node Modules

[Node](https://www.npmjs.com/) modules [now have namespaces](http://blog.npmjs.org/post/116936804365/solving-npms-hard-problem-naming-packages). Prefix them with a short product name: e.g. [karma](https://karma-runner.github.io/0.12/index.html) plugins are prefixed “karma-”; the same goes for gulp, grunt, etc. Host your Node modules in the public NPM registry. Here is [how to publish to NPM](https://gist.github.com/coolaj86/1318304).

#### Docker Images

@TODO 

### Working with External Contributors

The Open Source Team enthusiastically supports you in recruiting non-Jumias to contribute to your project. Collaboration and community are part of the fun of open source. 

Give GitHub's ["Creating a new contributor on-ramp" doc](https://github.com/blog/2128-creating-a-new-contributor-on-ramp) a look for some expert guidance. (TL;DR version = be welcoming, inclusive, and clear about what sorts of contributions you're looking for most).

Please ask external contributors to sign a contributor licensing agreement (CLA). A few good models to follow and adapt: [.Net Foundation](https://cla2.dotnetfoundation.org/) example (electronic submission via GitHub account); [Google’s CLA](https://github.com/angular/angular.js/blob/master/CONTRIBUTING.md#-signing-the-cla) for contributing to AngularJS is a simple click-through form with a Googlebot that automatically checks for signatures;

### Make Forks Meaningful

*“Forks are for making your own snapshot of a codebase so that you can make a new version of it with your own special sauce, or so that you can contribute a change in the form of a pull request. Simply, you must make a fork whenever you need to modify the codebase, but do not have direct access to do so. New users don’t understand this and end up equating the ‘fork’ button with ‘download’ or ‘bookmark’. Little do they know, you can download code directly from the original repository and you can bookmark things using Github’s stars.”* —[Eric Greer](http://ericgreer.info/github/funny/stupidity/2016/02/28/judging-the-stupidity-of-github-projects.html)

To fork, or not to fork? Some guidelines:
- Only keep the fork open as long as needed.
- “True/Long-Lived forks” are highly discouraged, even from Jumia projects. We avoid internal forks in order to avoid diverging widely from what we have published, and the inevitable hassle of getting the project to a state where we can support both code bases
- Avoid two forks of the same project.

If your goal is to make a small fix to a project, use your own/personal GitHub account.

### Deprecate Responsibly

#### How to Deprecate

Add “Deprecated” at the top of your README, as well as a notice stating your plans for the project: deletion, finding a new owner, etc.

After announcing your decision to deprecate the project:
   - notify your users. Put a notice on your README.
   - Wait 60 days.
   - Try to find a new owner. Internal options first, then seek an external owner. Ask the Guild for help.
   - Try to find an external owner. More guidance on this to come soon; for now, alert the Guild of any such plans.

#### Tips for Finding a New Owner

Internally, you can use internal mailing lists and HipChat to announce your need. Externally, social media platforms and community boards work well. Add 1-2 sentences to your announcements suggesting how your project might have potential to evolve into something bigger and better.

### Project Promotion

#### jumia.github.io: Our Open-Source Projects Dashboard

All Jumia open-source projects are listed on [jumia.github.io](http://jumia.github.io/).

#### Proactively Communicate

Share your project with:
- relevant LinkedIn Groups
- community forums/boards
- e-newsletters and websites/newsletters dedicated to the problem(s) your project is trying to solve, the relevant languages, etc.
- if you have contacts at a university, pitch your project to their students
- major players in the industry

### Contributing to Non-Jumia Open-Source Projects

We encourage you to contribute to other open-source projects in ways that benefit Jumia. Some ways you might contribute:

— making bug fixes in Apache
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

Please let the Guild know about your external contributions so we can help you get the recognition and support you deserve.

##### CLAs 

For typical CLAs, we are safe — but ask our legal team (guild can provide their contact info) to double-check whenever you’re in doubt. CLAs that are safe: Oracle, Apache, Google Projects.
