# Contributing to Hyperstack

We welcome and encourage contribution and would be delighted if you participated in this project.
If you're new to Hyperstack but have experience with Ruby (and Rails) and would like to contribute then start with the [ToDo tutorial](https://hyperstack.org/edge/docs/tutorials/todo)
that way you understand the basic capabilities and lingo of Hyperstack.

Next would be to start an experimental project that's based on the *edge* Hyperstack codebase.
If you just want to build a website with Hyperstack without contributing to Hyperstack itself you're better of sticking to released versions of Hyperstack.
But presuming you do want to contribute, you can change your `Gemfile` in the following way to get your project on *edge*.

```ruby
git 'https://github.com/hyperstack-org/hyperstack', branch: 'edge', glob: 'ruby/*/*.gemspec' do
  gem 'rails-hyperstack'
  gem 'hyper-component'
  gem 'hyper-i18n'
  gem 'hyper-model'
  gem 'hyper-operation'
  gem 'hyper-router'
  gem 'hyper-state'
  gem 'hyperstack-config'
  gem 'hyper-trace', group: :development
end

gem 'foreman', group: :development
```
The *edge* branch is the latest work in progress, where specs (automated tests) are passing, for the individual gem.
The difference between *edge* and *master*, is that *master* guarantees that all specs across all gems pass, plus *master* is the branch from which new versions are released.

With this configuration you can track development of Hyperstack itself and discuss changes with the other developers.
It's the basic starting point from which you can make different types of contributions listed below

- [Contributing Code](#contributing-code)
- [Improving Documentation](#improving-documentation)
- [Improving The Website](#improving-the-website)
- [If you found a possible bug](#if-you-found-a-possible-bug)
- [If you would like to fix a bug](#if-you-would-like-to-fix-a-bug)

Also, to get in contact with us, check out the [communication section](#communication).

## Contributing Code

With the `Gemfile` configuration above you can track Hyperstack development. But you can't contribute code.

For that you need to

  - `git clone https://github.com/hyperstack-org/hyperstack.git`
  - `cd hyperstack`
  - Change to the *edge* branch: `git checkout edge` (*edge* is the default branch but just to be sure).

Now you're free to fix bugs and create new features.

Reconfigure the `Gemfile` of your website project with a [filesystem path](https://bundler.io/gemfile.html) to create a local development environment.

```
TODO: Actually provide an example Gemfile..
```

And if your improvements could be interesting to others then push it to Github and create a pull request.
Then keep reminding the existing developers that you would like your code pulled into the Hyperstack repository.
When they find the time to look at it and like your code they will kindly ask you to also write some specs before your code is merged. That's a good thing, your code is considered valuable, but does require those tests.
Please understand that your code can also be rejected because it has security issues, is slow, hard to maintain or buggy (among other things).
Nobody likes it when this happens, but it can happen. If what you're trying to achieve is making sense then please keep at it.
If you have wild out of the box ideas that would not match Hyperstack then please use the power to fork away and prove your ideas independently.
But Hyperstack and Opal are quite happily pushing boundaries, so we might like your crazy ideas.

**Pro tip:** Talk trough your plans for changes before writing a lot of code. Push a few small fixes before starting mayor rewrites.

Hyperstack's [license is MIT](https://github.com/hyperstack-org/hyperstack/blob/edge/LICENSE). All code contributions must be under this license. If code is submitted under a different open source license then this must be explicitly stated. Preferably with an explanation why it can't be MIT.


## Improving Documentation

Each page on [the website](https://hyperstack.org) has an ***Improve this page*** button which will allow you to edit the underlying markdown file on Github and create a ***pull request***. This is to make it as easy as possible to contribute to the documentation.
And make small fixes quickly.

If you're planning on making sustained contributions to the documentation we would suggest to do a `git clone https://github.com/hyperstack-org/hyperstack.git` as documented above with code contributions.
Most documentation is written in .md files under the docs directory and can be edited with dedicated markdown editors or even plain text editors.
Push your changes and create a ***pull request*** as if it's a code contribution.

## Improving The Website

The website's code can be found in [this repository](https://github.com/hyperstack-org/website).
By running `git clone https://github.com/hyperstack-org/website.git` you can check out your own copy.
Please note that this repository does not contain the documentation. The website pulls the most recent markdown files from the *edge* hyperstack repository.

Before you write code to change the website, please create an issue describing your plans and reach out to us in the Slack chat. Our goal for this site is that it acts as a showcase for all that Hyperstack can do, so your creativity is very welcome.

## If you found a possible bug

You can ask on [slack](https://hyperstack.org/slack-invite) if you're making a mistake or actually found a bug.
Also check the GitHub issue list and if you don't find it mentioned there, please create an issue.
If you can reproduce the problem in a branch you push to GitHub we will love you even more.

We also have a [feature matrix](https://github.com/hyperstack-org/hyperstack/blob/edge/docs/feature_matrix.md), which is an attempt to list known issues and the current status.
Having people expanding and maintaining this table would be excellent.

## If you would like to fix a bug

Please ask in [slack](https://hyperstack.org/slack-invite) if you need pointers. There is always tons to do so we would appreciate the help.
You can see the list of GitHub issues labelled '[Help Wanted](https://github.com/hyperstack-org/hyperstack/issues?utf8=%E2%9C%93&q=is%3Aopen+is%3Aissue+label%3A%22help+wanted%22+)'
or look at the [feature matrix](https://github.com/hyperstack-org/hyperstack/blob/edge/docs/feature_matrix.md) for things that have the status 'bugged'.

## Communication

We use Slack as our main project communication platform.

- First, join our Slack group here: https://hyperstack.org/slack-invite
- Once you have joined, you can access Slack through the multi-platform app (you can add `Hyperstack-org` if you already use Slack for work) or if you prefer not to use the app, you can use your browser with a shortcut here: https://hyperstack.org/slack

### StackOverflow

We are using SO for all technical Q&A now. Please feel free to also ask and discuss in the Slack chat, but we are trying to get as many good Q&A in SO as we can, so we might ask you to re-ask in SO as well. Our tag is `hyperstack` but we like to add the `ruby-on-rails`, `ruby` and `react-js` tags as well to bring the project to wider attention (please mention you are using Hyperstack and even add a link to the project if you can).

- To ask a question use: https://hyperstack.org/question
- To see all `hyperstack` questions use https://hyperstack.org/questions

