# CSSMIN [![Build Status](https://secure.travis-ci.org/matthiassiegel/cssmin.png)](http://travis-ci.org/matthiassiegel/cssmin)

Ruby port of YUI compressor's CSS engine.

Based on the original [YUI compressor Java code](https://github.com/yui/yuicompressor) and the Javascript port by Stoyan Stefanov. The Ruby port is complete and passes all test cases that are included in the Java version. However, code and performance improvements are always welcome.

The motivation for this port was to have a native Ruby version without a Java or Javascript dependency.

## Usage

    require 'path/to/lib/cssmin.rb'
    
    CssCompressor.compress('/* a comment */ .test { display: block; }')
    # => minified CSS
    
    CssCompressor.compress(File.read('path/to/styles.css'))
    # => minified CSS
    
    CssCompressor.compress(File.open('path/to/styles.css'))
    # => minified CSS

Files or strings are acceptable as input.

You can pass in a second argument to control the maximum output line length (default 5000 characters):

    CssCompressor.compress(File.read('path/to/styles.css'), 200)

Note: in most cases line length will only be approximated.

## Compatibility
Tested with Ruby 1.9.2, 1.9.3, jruby-19mode, rbx-19mode

## Changelog
See [CHANGES](https://github.com/matthiassiegel/cssmin/blob/master/CHANGES.md).

## Credits, Copyright and License
See [LICENSE](https://github.com/matthiassiegel/cssmin/blob/master/LICENSE.md) for details.