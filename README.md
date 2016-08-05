# Gaspar

Convert PDF tables into HTML / Json / Xml / CSV files without losing text. This gem uses pdf-table-extract to do the conversion.

![Hay PDF, Hay Tabla](https://cloud.githubusercontent.com/assets/445798/17439517/82155610-5af6-11e6-9a3e-cfb0a019b1a1.jpg)

## Installation

Add this line to your application's Gemfile:

    gem 'gaspar'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install gaspar

## Usage

You need to install [pdf-table-extract](https://github.com/5rabbits/pdf-table-extract/releases) on your system to use this gem.

```ruby
require 'gaspar'

# Converts document.pdf to document.html
# This requires that the pdf2htmlEX command is present in your PATH.

Gaspar.convert('document.pdf', 'document.html', { page: 1, format: 'cells_json'})

# Available options:
# page - page to parse
# format -  the type of output: [cells_csv,cells_json,cells_xml,table_csv,table_html,table_chtml,table_list]

```

Inspired by [Kristin](https://github.com/ricn/kristin)

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
