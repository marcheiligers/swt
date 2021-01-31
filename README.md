
SWT
===

This gem contains everything required to write cross-platform desktop applications with JRuby and SWT.

Features:

 * Includes all the jar files needed.
 * Selects and loads the correct SWT jar for the platform.
 * Imports of many swt Java classes into a 1-1 mapped Ruby class hierarchy.
 * Examples to get you started. (For more see [this SWT cookbook](https://github.com/danlucraft/jruby-swt-cookbook))

## Why JRuby/SWT?

  * Fast, compatible Ruby implementation.
  * JRuby and SWT are flawlessly cross-platform.
  * SWT has native widgets (for the most part).
  * SWT powers Eclipse, so there's nothing you need that it doesn't do.
  * You don't need to touch Java! Write everything in Ruby.

## Usage

    require 'java'
    require 'swt'

## Running the Example

Linux / windows:

    jruby examples/button.rb

On OSX:

    jruby -J-XstartOnFirstThread examples/button.rb

## Development

### Updating SWT

1. Grab the latest release of "SWT Binary and Source" from [Eclipse Downloads](https://download.eclipse.org/eclipse/downloads/index.html#Latest_Release) for each platform, unzip and copy the`swt.jar`, renamed to `swt-{platform}.jar` into the `vendor/swt` directory.
1. Update the version in `lib/swt/version.rb`. The version should match the SWT version.
1. Update the CHANGELOG.md

## History

**4.6** Removed MacOS 32 bit support (SWT project doesn't seem to support it any more)
