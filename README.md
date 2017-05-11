# Web page archiver

Web page archiver is a gem for building web archives. It supports mht (this gem is actually based on takuya's mht gem) and html with data urls (the rename from the original mht name is just to emphasize the support for this alternative format).
mht is known as mhtml that internet explorer's web page archive.
this package can make web archives from local files and URI's

## Contributing to web page archiver
 
* Check out the latest master to make sure the feature hasn't been implemented or the bug hasn't been fixed yet
* Check out the issue tracker to make sure someone already hasn't requested it and/or contributed it
* Fork the project
* Start a feature/bugfix branch
* Commit and push until you are happy with your contribution
* Make sure to add tests for it. This is important so I don't break it in a future version unintentionally.
* Please try not to mess with the Rakefile, version, or history. If you want to have your own version, or is otherwise necessary, that is fine, but please isolate to its own commit so I can cherry-pick around it.

## Example

```ruby

#rails use
#URI or file
require 'web_page_archiver'

uri = 'http://murb.github.com/web-page-archiver/static/'

result_a = WebPageArchiver::MhtmlGenerator.generate(uri, true)
result_b = WebPageArchiver::DataUriHtmlGenerator.generate(uri, true)

```

or

```ruby

#rails use
#Inline HTML
require 'web_page_archiver'

inline_html = '<html><head><title>Inline</title></head><body><h1>Hello, World!</h1></body></html>'

result_a = WebPageArchiver::MhtmlGenerator.generate(inline_html, false)
result_b = WebPageArchiver::DataUriHtmlGenerator.generate(inline_html, false)

```

## Copyright

Copyright (c) 2012 murb. See LICENSE.txt for further details.
Portions copyright (c) 2011 takuya. See LICENSE.txt for further details.

