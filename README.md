# CocoaPods Packager

[![Gem Version](http://img.shields.io/gem/v/cocoapods-packager-next.svg?style=flat)](http://badge.fury.io/rb/cocoapods-packager-next)

CocoaPods plugin which allows you to generate a framework or static library from a podspec.

This plugin is for CocoaPods *developers*, who need to distribute their Pods not only via CocoaPods, but also as frameworks or static libraries for people who do not use Pods.

## Why should I use Pods if I'm targeting developers who don't use Pods?

There are still a number of advantages to developing against a `podspec`, even if your public distribution is closed-source:

1. You can easily use the Pod in-house in an open-source style. This makes step-by-step debugging and multi-project development a breeze.
2. You can pull in third-party dependencies using CocoaPods. (CocoaPods Packager is even capable of mangling symbols to improve compatibility with any symbols that might appear in the integrating app.)
3. You can declaratively specify build settings (e.g. frameworks, compiler flags) in your `podspec`. This is easier to maintain and replicate than build settings embedded in your Xcode project.

## Installation

```sh
$ gem install cocoapods-packager-next
```

or add a line to your Gemfile:

```ruby
gem "cocoapods-packager-next"
```

then run `bundle install`.

This installs Packager as a CocoaPods plugin.

## Usage

```bash
$ pod package KFData.podspec
```

See also `pod --help`.
