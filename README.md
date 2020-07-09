# Ruby Cheatsheet

![ruby](https://user-images.githubusercontent.com/1612112/74456286-b1bcd100-4eda-11ea-9738-7e0a27199021.png)

<p align="center">
<a href="https://www.ruby-lang.org"><img alt="Ruby" src="https://cdn.emojidex.com/emoji/mdpi/Ruby.png"/></a>
<a href="https://github.com/lifeparticle/Ruby-Cheatsheet/issues"><img alt="contributions welcome" src="https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat"/></a>
</p>

Table of Contents
=================
   * [Installation](#installation)
      * [Troubleshooting](#troubleshooting)
         * [macOS](#macos)
      * [How to install Ruby](#how-to-install-ruby)
      * [How to install ruby gem manager, bundler gem](#how-to-install-ruby-gem-manager-bundler-gem)
      * [What is a Gemfile and Gemfile.lock](#what-is-a-gemfile-and-gemfilelock)
      * [How to install a specific version of a particular ruby gem](#how-to-install-a-specific-version-of-a-particular-ruby-gem)
      * [How to update a single gem using Bundler](#how-to-update-a-single-gem-using-bundler)
      * [How to update every gem in the Gemfile using Bundler](#how-to-update-every-gem-in-the-gemfile-using-bundler)
   * [Introduction](#introduction)
   * [Reserved Words](#reserved-words)
   * [Comment](#comment)
   * [Operators](#operators)
      * [Logical operators](#logical-operators)
      * [Bitwise operators](#bitwise-operators)
      * [Arithmetic operators](#arithmetic-operators)
      * [Comparison operators](#comparison-operators)
      * [Assignment operators](#assignment-operators)
   * [Variables and Scope](#variables-and-scope)
      * [Pseudo variables](#pseudo-variables)
      * [Pre-defined variables](#pre-defined-variables)
      * [Pre-defined global constants](#pre-defined-global-constants)
      * [How to check scope of variables](#how-to-check-scope-of-variables)
   * [Conditional structures](#conditional-structures)
      * [If elsif else expression](#if-elsif-else-expression)
      * [unless expression](#unless-expression)
      * [Shorthand](#shorthand)
      * [Case Expressions](#case-expressions)
   * [Data types](#data-types)
      * [How to check the data type](#how-to-check-the-data-type)
   * [Symbol](#symbol)
   * [String](#string)
      * [How to convert String to lower or upper case](#how-to-convert-string-to-lower-or-upper-case)
      * [Helpful methods](#helpful-methods)
   * [Range](#range)
      * [Helpful methods](#helpful-methods-1)
      * [How to use step with Range](#how-to-use-step-with-range)
   * [Methods](#methods)
      * [How to declare a method](#how-to-declare-a-method)
      * [How to call a method](#how-to-call-a-method)
      * [How to define a default value for a method parameter](#how-to-define-a-default-value-for-a-method-parameter)
      * [How to use another parameter for the default value](#how-to-use-another-parameter-for-the-default-value)
      * [How to pass variable length argument to a method parameter](#how-to-pass-variable-length-argument-to-a-method-parameter)
      * [Boolean method](#boolean-method)
      * [Class method](#class-method)
   * [Blocks](#blocks)
      * [How to check if a block is given](#how-to-check-if-a-block-is-given)
   * [Procs](#procs)
   * [Lambdas](#lambdas)
   * [Blocks VS Procs VS Lambdas](#blocks-vs-procs-vs-lambdas)
   * [Array](#array)
      * [How to iterate an Array](#how-to-iterate-an-array)
         * [each](#each)
         * [each_with_index](#each_with_index)
         * [each_with_object](#each_with_object)
         * [each_index](#each_index)
         * [map](#map)
         * [select](#select)
         * [reject](#reject)
         * [inject](#inject)
         * [reduce](#reduce)
         * [collect](#collect)
         * [detect](#detect)
         * [while](#while)
         * [until](#until)
         * [for](#for)
         * [times](#times)
         * [upto](#upto)
         * [downto](#downto)
         * [step](#step)
      * [Boolean Enumerable methods](#boolean-enumerable-methods)
         * [all?](#all)
         * [any?](#any)
         * [one?](#one)
         * [none?](#none)
         * [empty?](#empty)
      * [How to check if a value exists in an Array (include?)](#how-to-check-if-a-value-exists-in-an-array-include)
      * [How to get array size](#how-to-get-array-size)
      * [How to clear an Array](#how-to-clear-an-array)
      * [How to get the last element of an Array](#how-to-get-the-last-element-of-an-array)
      * [How to merge two Arrays](#how-to-merge-two-arrays)
      * [How to sort an Array](#how-to-sort-an-array)
      * [How to get the maximum from an Array](#how-to-get-the-maximum-from-an-array)
   * [Hash](#hash)
      * [How to group by count](#how-to-group-by-count)
      * [What's the difference between Hash.new(0) and {}](#whats-the-difference-between-hashnew0-and-)
      * [How to sort a Hash](#how-to-sort-a-hash)
      * [How to get the maximum from a Hash](#how-to-get-the-maximum-from-a-hash)
   * [Loop](#loop)
      * [How to break out from loop](#how-to-break-out-from-loop)
      * [How to skip inside a loop](#how-to-skip-inside-a-loop)
      * [How to repeat the current iteration](#how-to-repeat-the-current-iteration)
      * [How to restart a loop](#how-to-restart-a-loop)
   * [Classes](#classes)
      * [How to inherit a class](#how-to-inherit-a-class)
      * [How to check instance type](#how-to-check-instance-type)
      * [Print all method names of a class](#print-all-method-names-of-a-class)
      * [Check if a Class has a particular method](#check-if-a-class-has-a-particular-method)
   * [Modules](#modules)
   * [Operator Overloading](#operator-overloading)
   * [Exception Handling](#exception-handling)
   * [Regular expression](#regular-expression)
   * [Miscellaneous](#miscellaneous)
      * [How to generate random number](#how-to-generate-random-number)
      * [Check the syntax of a Ruby file](#check-the-syntax-of-a-ruby-file)
      * [Concatenate String in a loop](#concatenate-string-in-a-loop)
      * [CamelCase String split](#camelcase-string-split)
      * [Ruby scripts](#ruby-scripts)
   * [Books and other resources](#books-and-other-resources)
   * [Bug Reports and Feature Requests](#bug-reports-and-feature-requests)
   * [Contribution Guidelines](#contribution-guidelines)
   * [Author](#author)
   * [License](#license)



Installation
============

Troubleshooting
-----

### macOS

List all the installed Ruby versions
```
which -a ruby
```

Get information about currently used Ruby
```
ruby -v
gem env
```

How to install Ruby
-----

First things first, make sure you have [Ruby](https://www.ruby-lang.org/en/documentation/installation/) installed on your machine. In case you don’t want to install Ruby natively, you can use [docker](https://docs.docker.com/engine/install/).

```
docker run -it --rm ruby:latest
# check which version of Ruby you're running
RUBY_VERSION
```

Run a specific version of Ruby.

```
docker run -it --rm ruby:2.7
# check which version of Ruby you're running
RUBY_VERSION
```

How to install ruby gem manager, bundler gem
-----

```
# access the bash for executing the following commands
docker run -it --rm ruby:latest bash
```

```
gem install bundler
bundle -v
gem update bundler
gem uninstall bundler
```

[Further reading](https://bundler.io/)

What is a Gemfile and Gemfile.lock
-----
Gemfile is a configuration file for Bundler (also a gem), which contains a list of gems for your project (dependencies).

[Further reading](https://bundler.io/v2.0/man/gemfile.5.html)

```
# specify your gems in a Gemfile in your project’s root
ruby '2.5.6'

source 'https://rubygems.org'
gem 'nokogiri'
gem 'rack', '~>1.1'
gem 'rspec', :require => 'spec'
```

```bash
# install all the gems in the Gemfile
bundle install
```

How to install a specific version of a particular ruby gem
-----
```bash
gem install bundler -v 1.17
gem install minitest -v 5.8.4
```

How to update a single gem using Bundler
-----
```bash
bundle update nokogiri
```

Bundler attempted to update `gem_name` but its version stayed the same.

1. Another gem depends on the `gem_name`.
2. The version number is specified in your Gemfile for `gem_name`.
```
'gem_name', '~> 2.0.5'
```

How to update every gem in the Gemfile using Bundler
-----
```bash
bundle update
```

For best observance lookout at this video - [Ruby + RoR](https://medium.com/ruby-on-rails-web-application-development/how-to-install-rubyonrails-on-windows-7-8-10-complete-tutorial-2017-fc95720ee059)

Introduction
============
In Ruby everything is an object.

Reserved Words
============

```
__ENCODING__ , __LINE__ , __FILE__ , BEGIN , END , alias , and , begin , break , case , class , def ,
defined? , do , else , elsif , end , ensure , false , for , if , in , module , next , nil , not , or ,
redo, rescue , retry , return , self , super , then , true , undef , unless , until , when , while , yield
```

[Further reading](https://ruby-doc.org/core-2.6.4/doc/keywords_rdoc.html)

Comment
============

```ruby
# single line comment

=begin
multiline
comment
=end
```

Operators
============
Logical operators
-----
| No | Operator |
|---|---|
| 1 | and   |
| 2 | or    |
| 3 | not   |
| 4 | &&    |
| 5 | \|\|  |
| 6 | !     |


Bitwise operators
-----
| No | Operator |
|---|---|
| 1 | &     |
| 2 | \|    |
| 3 | ^     |
| 4 | ~     |
| 5 | <<    |
| 6 | >>    |

Arithmetic operators
-----
| No | Operator |
|---|---|
| 1 | +     |
| 2 | -     |
| 3 | *     |
| 4 | /     |
| 5 | %     |
| 6 | **    |

Comparison operators
-----
| No | Operator |
|---|---|
| 1  | ==     |
| 2  | !=     |
| 3  | >      |
| 4  | <      |
| 5  | >=     |
| 6  | <=     |
| 7  | <=>    |
| 8  | ===    |
| 9  | eql?   |
| 10 | equal? |

Assignment operators
-----
| No | Operator |
|---|---|
| 1 | =     |
| 2 | +=    |
| 3 | -=    |
| 4 | *=    |
| 5 | /=    |
| 6 | %=    |
| 7 | **=   |


Variables and Scope
============
There are five different types of variables. The first character determines the scope.

| No | Name | Scope | Example | Note |
|---|---|---|---|---|
| 1 | [a-z] or _  | local             | count = 10 or _count = 10 | Local variables must be initialized.                                                                |
| 2 | @           | instance variable | @id = []                  | Instance variables have the `nil` value until they are initialized.                                 |
| 3 | @@          | class variable    | @@name = []               | Class variable must be initialized.                                                                 |
| 4 | $           | global variable   | $version = "0.8.9"        | Global variables have the `nil` value until they are initialized.                                   |
| 5 | [A-Z]       | constant          | PI = 3.14                 | Constant variables must be initialized and you can change the constant but you will get a warning. |


1. Scope of a local variable is one of

```
proc{ ... }
loop{ ... }
def ... end
class ... end
module ... end
the entire program (unless one of the above applies)
```

2. Scope of an instance variable is
```
Instance variables cannot be altered except some methods, and it's distinct to each object of a class
```

3. Scope of a class variable is one of
```
Can be called from a class by calling ClassName.class_variable and it's independent of any object of a class
```

4. Scope of a global variable is
```
It can be referred from anywhere in a program
```

5. Scope of a constant variable is
```
Accessible outside the class
```

Pseudo variables
-----

| No | Name | Note |
|---|---|---|
| 1  | self        | The receiver object of the current method  |
| 2  | true        | Instance of the TrueClass  |
| 3  | false       | Instance of the FalseClass  |
| 4  | nil         | Instance of the NilClass   |
| 5  | `__FILE__`  | The name of current source file name  |
| 6  | `__LINE__`  | The current line number of current source file |


Pre-defined variables
-----

| No | Name | Note |
|---|---|---|
| 1 | $! | The exception information message. raise sets this variable. |
| 2 | $@ | The backtrace of the last exception, which is the array of the String that indicates the point where methods invoked from. The elements in the format like: "filename:line" or "filename:line:in `methodname'" (Mnemonic: where exception occurred at.) |
| 3 | $& |  The String matched by the last successful pattern match in this scope, or nil if the last pattern match failed. (Mnemonic: like & | in some editors.) This variable is read-only. |
| 4 | $` | The String preceding whatever was matched by the last successful pattern match in the current scope, or nil if the last pattern match failed. (Mnemonic: ` often precedes a quoted string.) This variable is read-only. |
| 5 | $' | The String following whatever was matched by the last successful pattern match in the current scope, or nil if the last pattern match failed. (Mnemonic: ' often follows a quoted string.) |
| 6 | $+ | The last bracket matched by the last successful search pattern, or nil if the last pattern match failed. This is useful if you don't know which of a set of alternative patterns matched. (Mnemonic: be positive and forward looking.) |
| 7 | $1, $2... | Contains the subpattern from the corresponding set of parentheses in the last successful pattern matched, not counting patterns matched in nested blocks that have been exited already, or nil if the last pattern match failed. (Mnemonic: like \digit.) These variables are all read-only. |
| 8 | $~ | The information about the last match in the current scope. Setting this variables affects the match variables like $&, $+, $1, $2.. etc. The nth subexpression can be retrieved by $~[nth]. (Mnemonic: ~ is for match.) This variable is locally scoped. |
| 9 | $= | The flag for case insensitive, nil by default. (Mnemonic: = is for comparison.) |
| 10 | $/ | The input record separator, newline by default. Works like awk's RS variable. If it is set to nil, whole file will be read at once. (Mnemonic: / is used to delimit line boundaries when quoting poetry.) |
| 11 | $\ | The output record separator for the print and IO#write. The default is nil. (Mnemonic: It's just like /, but it's what you get "back" from Ruby.) |
| 12 | $, | The output field separator for the print. Also, it is the default separator for Array#join. (Mnemonic: what is printed when there is a , in your print statement.) |
| 13 | $; | The default separator for String#split. |
| 14 | $. | The current input line number of the last file that was read. |
| 15 | $< | The virtual concatenation file of the files given by command line arguments, or stdin (in case no argument file supplied). $<.file returns the current filename. (Mnemonic: $< is a shell input source.) |
| 16 | $> | The default output for print, printf. $stdout by default. (Mnemonic: $> is for shell output.) |
| 17 | $_ | The last input line of String by gets or readline. It is set to nil if gets/readline meet EOF. This variable is locally scoped. (Mnemonic: partly same as Perl.) |
| 17 | $0 | Contains the name of the file containing the Ruby script being executed. On some operating systems assigning to $0 modifies the argument area that the ps(1) program sees. This is more useful as a way of indicating the current program state than it is for hiding the program you're running. (Mnemonic: same as sh and ksh.) |
| 18 | $* | Command line arguments given for the script. The options for Ruby interpreter are already removed. (Mnemonic: same as sh and ksh.) |
| 19 | $$ | The process number of the Ruby running this script. (Mnemonic: same as shells.) |
| 20 | $? | The status of the last executed child process. |
| 21 | $: | The array contains the list of places to look for Ruby scripts and binary modules by load or require. It initially consists of the arguments to any -I command line switches, followed by the default Ruby library, probabl "/usr/local/lib/ruby", followed by ".", to represent the current directory. (Mnemonic: colon is the separators for PATH environment variable.) |
| 22 | $" | The array contains the module names loaded by require. Used for prevent require from load modules twice. (Mnemonic: prevent files to be doubly quoted(loaded).) |
| 23 | $DEBUG | The status of the -d switch. |
| 24 | $FILENAME | Same as $<.filename. |
| 25 | $LOAD_PATH | The alias to the $:. |
| 26 | $stdin | The current standard input. |
| 27 | $stdout | The current standard output. |
| 28 | $stderr | The current standard error output. |
| 29 | $VERBOSE | The verbose flag, which is set by the -v switch to the Ruby interpreter. |

Option variables: The variables which names are in the form of $-?, where ? is the option character, are called option variables and contains the information about interpreter command line options.

| No | Name | Note |
|---|---|---|
| 1 | $-0 | The alias to the $/. |
| 2 | $-a | True if option -a is set. Read-only variable. |
| 3 | $-d | The alias to the $DEBUG. |
| 4 | $-F | The alias to the $;. |
| 5 | $-i | In in-place-edit mode, this variable holds the extention, otherwise nil. Can be assigned to enable (or disable) in-place-edit mode. |
| 6 | $-I | The alias to the $:. |
| 7 | $-l | True if option -lis set. Read-only variable. |
| 8 | $-p | True if option -pis set. Read-only variable. |
| 9 | $-v | The alias to the $VERBOSE. |

[Source](https://ruby-doc.org/docs/ruby-doc-bundle/Manual/man-1.4/variable.html#variables)

Pre-defined global constants
-----

| No | Name | Note |
|---|---|---|
| 1 | TRUE | The typcal true value. All non-false values (everything except nil and false) is true in Ruby. |
| 2 | FALSE | The false itself. |
| 3 | NIL | The nil itself. |
| 4 | STDIN | The standard input. The default value for $stdin. |
| 5 | STDOUT | The standard output. The default value for $stdout. |
| 6 | STDERR | The standard error output. The default value for $stderr. |
| 7 | ENV | The hash-like object contains current environment variables. Setting a value in ENV changes the environment for child processes. |
| 8 | ARGF | The alias to the $<. |
| 9 | ARGV | The alias to the $*. |
| 10 | DATA | The file object of the script, pointing just after the __END__. Not defined unless the script is not read from the file. |
| 11 | VERSION | The Ruby version string. |
| 12 | RUBY_RELEASE_DATE | The relase date string. |
| 13 | RUBY_PLATFORM | The platform identifier. |

[Source](https://ruby-doc.org/docs/ruby-doc-bundle/Manual/man-1.4/variable.html#constants)

How to check scope of variables
-----
```ruby
defined? count
"local-variable"
defined? @id
"instance-variable"
defined? @@name
"class variable"
defined? $version
"global-variable"
defined? PI
"constant"
```

Conditional structures
============

If elsif else expression
-----

```ruby
temp = 19

if temp >= 25
    puts "hot"
elsif temp < 25 && temp >= 18
    puts "normal"
else
    puts "cold"
end

# output
# normal
```

unless expression
-----

```ruby
# The unless is opposite of if, evaluates when the statement is false

name = "rob"

unless name == "bob"
    puts "hello stranger"
else
    puts "hello bob"
end

# output
# hello stranger
```

Shorthand
-----

```ruby
count = 1
puts "hello world" if count == 1
# output
# hello world

count = 2
puts "hello universe" if count != 1
# or using unless
puts "hello universe" unless count == 1
# output
# hello universe
```

Case Expressions
-----

```ruby
# case returns the value of the last expression executed

case input
# check an integer, 19
when 19
puts "It's 19"
# check a float number, 33.3
when 33.3
puts "It's 33.3"
# check an exact string, "Zaman"
when "Zaman"
puts "Hi Zaman"
when 10
puts "It's 10"
# check against a range
when 7..11
puts "It's between 7 and 11"
# check against multiple values, "coffee"
when "tea", "coffee"
puts "Happy days"
# check against a regular expression, "aA6"
when /^a[A-Z]+[0-6]+$/
puts "It's a valid match"
# check any string by comparing against the String class, "any string"
when String
puts "It's a String"
end

# using short syntax
case input
when 19 then puts "It's 19"
end

# optional fallthrough
case input
when 19 then puts "It's 19"
else
puts "It's not 19"
end

# get the return value
marks = 86

result = case marks
    when 0..49 then "Fail"
    when 50..64 then "Pass"
    when 65..74 then "Credit"
    when 75..84 then "Distinction"
    when 85..100 then "High Distinction"
    else "Invalid marks"
end

puts marks
# output
# 86
```
Data types
============

| No | Type  | Example  | Class  | Doc  |
|---|---|---|---|---|
| 1 | Integer  | a = 17                       | a.class > Integer <br>a.class.superclass > Numeric         | [link](https://ruby-doc.org/core-2.6.3/Integer.html)  |
| 2 | Float    | a = 87.23                    | a.class > Float <br>a.class.superclass > Numeric           | [link](https://ruby-doc.org/core-2.6.3/Float.html)    |
| 3 | String   | a = "Hello universe"         | a.class > String                                           | [link](https://ruby-doc.org/core-2.6.3/String.html)   |
| 4 | Array    | a = [12, 34]                 | a.class > Array                                            | [link](https://ruby-doc.org/core-2.6.3/Array.html)    |
| 5 | Hash     | a = {type: "tea", count: 10} | a.class > Hash                                             | [link](https://ruby-doc.org/core-2.6.3/Hash.html)     |
| 6 | Boolean  | a = false<br>a = true        | a.class > FalseClass <br>a.class > TrueClass               | [TrueClass](https://ruby-doc.org/core-2.6.3/TrueClass.html) <br> [FalseClass](https://ruby-doc.org/core-2.6.3/FalseClass.html)  |
| 7 | Symbol   | a = :status                  | a.class > Symbol                                           | [link](https://ruby-doc.org/core-2.6.3/Symbol.html)   |
| 8 | Range    | a = 1..3                     | a.class > Range                                            | [link](https://ruby-doc.org/core-2.6.3/Range.html)    |
| 9 | Nill     | a = nil                      | a.class > NilClass                                         | [link](https://ruby-doc.org/core-2.6.3/NilClass.html) |

[Further readings](https://www.digitalocean.com/community/tutorials/understanding-data-types-in-ruby)

How to check the data type
-----

```ruby
# both are synonymous
a = 37
a.kind_of? Integer
# true
a.is_a? Integer
# true
```

Symbol
============

Symbol objects represent names. Symbols are immutable, which means every symbol is unique, and we can't change it. Referencing the same symbol multiple times is the same as referencing the same object everywhere in your program. As a result, we can save both time and memory by referencing the same memory location.

Symbols as hash keys.
```
week_days = {sunday: 11, monday: 222}
```

String
============

How to convert String to lower or upper case
-----

| No | Method name | Output |
|---|---|---|
| 1 | downcase   | "HELLO World".downcase <br> "hello world"   |
| 2 | upcase     | "hello worlD".upcase <br> "HELLO WORLD"     |
| 3 | capitalize | "hEllo wOrlD".capitalize <br> "Hello world" |
| 4 | swapcase   | "hEllo WOrlD".swapcase <br> "HeLLO woRLd"   |

Helpful methods
-----

| No | Method name | Output | Note |
|---|---|---|---|
| 1 | length or size                   | "HELLO World".length <br> 11 <br> "HELLO World".size <br> 11                                       | returns the length of the string  |
| 2 | reverse                          | "hello worlD".reverse <br> "Dlrow olleh"                                                           | returns the reversed string |
| 3 | include? other_str               | "hEllo wOrlD".include? "w" <br> true                                                               | returns true if the string or charecter is present or otherwise false |
| 4 | gsub(pattern, replacement)       | "hEllo wOrlD".gsub(" ", "_") <br> "hEllo_wOrlD"                                                    | gsub or global substitute substitutes one or more string with provided strings |
| 5 | gsub(pattern, hash)              | "organization".gsub("z", 'z' => 's') <br>"organisation"                                            | gsub or global substitute substitutes one or more string with provided hash |
| 6 | gsub(pattern) { \|match\| block} | "Price of the phone is 1000 AUD".gsub(/\d+/) { \|s\| '$'+s } <br>"Price of the phone is $1000 AUD" | gsub or global substitute substitutes one or more string with provided block |
| 7 | strip                            | "  hEllo WOrlD  ".strip <br> "hEllo WOrlD"                                                         | It will remove (trim) any of the following leading and trailing characters: null("\x00"), horizontal tab("\t"), line feed(\n), vertical tab("\v"), form feed(f), carriage return(\r), space(" ") |
| 8 | prepend                          | a = "world" <br> a.prepend("hello ") <br> "hello world"                                            | Add string before another string  |
| 9 | insert                           | a = "hello" <br> a.insert(a.length, " world") <br> "hello world"                                   | Insert string at a specific position |


Range
============

Ranges allow us to declare data with a beginning and an end, it has two operators to generate ranges.

```ruby
# .. for creating inclusive ranges

range = 1..10
range.to_a
# output
# [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

```ruby
# ... for creating exclusive ranges

range = 1...10
range.to_a
# output
# [1, 2, 3, 4, 5, 6, 7, 8, 9]
```

Helpful methods
-----
| No | Method name | Output |
|---|---|---|
| 1 | cover?   | (1..5).cover?(5) <br> true                 |
| 2 | end      | ('a'..'z').end <br> "z"                    |
| 3 | first    | (1..5).first <br> 1                        |
| 4 | first(3) | ('A'..'Z').first(2) <br> ["A", "B"]        |
| 5 | eql?     | ((0..2).eql?(0..5) <br> false              |

How to use step with Range
-----
```ruby
(1..20).step(2) { |number| puts "#{number}"}
# output
# 1
# 3
# 5
# 7
# 9
# 11
# 13
# 15
# 17
# 19
```


Methods
============

How to declare a method
-----

```ruby
# In Ruby last statement evaluated is the return value of that method

# both methods does the same thing, depend on your preference you can choose either of them
def method_name(parameter1, parameter2)
    puts "#{parameter1} #{parameter2}"
    parameter1 + parameter2
end

res = method_name(20, 10)
# output
# 30
```

```ruby
def method_name(parameter1, parameter2)
    puts "#{parameter1} #{parameter2}"
    return parameter1 + parameter2
end
# output
# 30
```

How to call a method
-----

```ruby
res = method_name(parameter1, parameter2)
# In Ruby you can call methods without parentheses
res = method_name parameter1, parameter2
```

How to define a default value for a method parameter
-----

```ruby
def method_name(parameter1, parameter2, type = "ADD")
    puts "#{parameter1} #{parameter2}"
    return parameter1 + parameter2 if type == "ADD"
    return parameter1 - parameter2 if type == "SUB"
end

res = method_name(20, 10)
# output
# 30
```

How to use another parameter for the default value
-----
```ruby
def method_name(num1, num2 = num1)
    return num1 + num2
end

res = method_name(10)
# output
# 20
```

How to pass variable length argument to a method parameter
-----
```ruby
def method_name(type, *values)
    return values.reduce(:+) if type == "ADD"
    return values.reduce(:-) if type == "SUB"
end

numbers = [2, 2, 2, 3, 3, 3]

res = method_name("ADD", *numbers)
# output
# 15

res = method_name("SUB", *numbers)
# output
# -11

# or you can provide the values like this
res = method_name("ADD", 2, 2, 2, 3, 3, 3)
# output
# 15
```

Boolean method
-----
In ruby methods that end with a question mark (?) are called boolean methods, which either returns true or false.

```ruby
"some text".nil?
# false
nil.nil?
# true
```

You can have your own boolean methods.

```ruby
def is_vowel?(char)
    ['a','e','i','o','u'].include? char
end

is_vowel? 'a'
# true
is_vowel? 'b'
# false
```

Class method
-----
A class method is a class-level method. There are multiple ways of defining a class method.

```ruby
class Mobile
    def self.ring
        "ring ring ring..."
    end
end

Mobile.ring
```

```ruby
class Mobile
    def Mobile.ring
        "ring ring ring..."
    end
end

Mobile.ring
```

```ruby
class Mobile
    class << self
    def ring
        "ring ring ring..."
       end
    end
end

Mobile.ring
```

A class method is an instance method of the class object. When a new class is created, an object of type `Class` is initialized and assigned to a global constant (Mobile in this case).


```ruby
Mobile = Class.new do
    def self.ring
        "ring ring ring..."
    end
end

Mobile.ring
```

```ruby
Mobile = Class.new

class << Mobile
    def ring
        "ring ring ring..."
    end
end

Mobile.ring
```

Blocks
============
Codes between ```do``` and ```end``` (for multiline) or curly brackets ```{``` and ```}``` (for a single line) are called blocks, and they can have multiple arguments defined between two pipes ```(|arg1, arg2|)```.
A block can be passed as a method parameter or can be associated with a method call. A block returns the last evaluated statement.

```ruby
# return value
def give_me_data
    data = yield
    puts "data = #{data}"
end

give_me_data { "Big data" }

# output
# data = Big data
```

```ruby
# single line block
salary = [399, 234, 566, 533, 233]
salary.each { |s| puts s }

# puts s = block body
# |s| = block arugments
```

```ruby
# multiline block
salary.each do |s|
    a = 10
    res = a * s
    puts res
end

# block body
# a = 10
# res = a * s
# puts res

# block arugments
# |s|
```

Methods can take blocks implicitly and explicitly. If you want to call a block implicitly use the `yield` keyword. Yield finds the block and calls the passed block. Since you can pass implicit blocks, you don't have to call yield, and the block will be ignored.

```ruby
# passing a block implicitly
def give_me_data
    puts "I am inside give_me_data method"
    yield
    puts "I am back in give_me_data method"
end

give_me_data { puts "Big data" }

# output
# I am inside give_me_data method
# Big data
# I am back in give_me_data method

# call multiple times
def give_me_data
    yield
    yield
    yield
end

give_me_data { puts "Big data" }

# output
# Big data
# Big data
# Big data

# call with block arguments

def give_me_data
    yield 10
    yield 100
    yield 30
end

give_me_data { |data| puts "Big data #{data} TB" }

# output
# Big data 10 TB
# Big data 100 TB
# Big data 30 TB

# call with multiple block arguments

def give_me_data
    yield "Big data", 10, "TB"
    yield "Big data", 100, "GB"
    yield "Big data", 30, "MB"
end

give_me_data { |text, data, unit| puts "#{text} #{data} #{unit}" }

# output
# Big data 10 TB
# Big data 100 GB
# Big data 30 MB

#  block will try to return from the current context
give_me_data
    puts "I am inside give_me_data method"
end

def test
    puts "I am inside test method"
    give_me_data { return 10 } # code returns from here
    puts "I am back in test method"
end

return_value = test

# output
# I am inside test method
# I am inside give_me_data method
# 10
```

```ruby
# passing a block explicitly by using an ampersand parameter, here we are explicitly defining the method with block parameter and calling it
def give_me_data(&block)
    block.call
    block.call
end

give_me_data { puts "Big data" }

# output
# Big data
# Big data
```

How to check if a block is given
-----
block parameter is mandatory when you call yield inside a method; otherwise, it will raise an exception

```ruby
def give_me_data
    yield
end

give_me_data

# output
# LocalJumpError: no block given (yield)

# you can use block_given? method to handle the exception and make the block optional

def give_me_data
    return "no block" unless block_given?
    yield
end

give_me_data { puts "Big data" }
give_me_data

# output
# Big data

def give_me_data(&block)
    block.call if block
end

give_me_data { puts "Big data" }
give_me_data

# output
# Big data
```

Procs
============
A proc is like a block that can be stored in a variable.

```ruby
p = Proc.new { puts "Hello World" }

def give_me_data(proc)
    proc.call
end

give_me_data p

# output
# Hello World

# arbitrary arguments
p = Proc.new { |count| "Hello World " * count }

def give_me_data(proc)
    proc.call 5, 2
end

give_me_data p

# output
# "Hello World Hello World Hello World Hello World Hello World "

#  proc will try to return from the current context
p = Proc.new { return 10 }
p.call

# output
LocalJumpError: unexpected return

# because you can’t return from the top-level context

def give_me_data
    puts "I am inside give_me_data method"
    p = Proc.new { return 10 }
    p.call # code returns from here
    puts "I am back in give_me_data method"
end

return_value = give_me_data
puts return_value

# output
# I am inside give_me_data method
# 10
```

Lambdas
============
Lambda is an anonymous function, wrap the lambda with ```do and end``` (for multiline) or curly brackets ```{ and }``` (for a single line). Lambda returns the last evaluated statement.

```ruby
# there are multiple ways to declare a lambda
l = lambda { puts "Hello World" }
# shorthand
l = -> { puts "Hello World" }

# call the lambda
l.call

# output
# Hello World

# there are multiple ways you can call a lambda
l.()
l[]

# strict arguments
l = -> (count) { "Hello World " * count }
l.call 5

# output
# "Hello World Hello World Hello World Hello World Hello World "

l.call 5, 2

# output
wrong number of arguments (given 2, expected 1)

# lambdas return from the lambda itself, like a regular method
l = -> { return 10 }
l.call

# output
# 10

def give_me_data
    puts "I am inside give_me_data method"
    l = -> { return 10 }
    l.call
    puts "I am back in give_me_data method"
end

return_value = give_me_data
puts return_value

# output
# I am inside give_me_data method
# I am back in give_me_data method
# nil # because puts return nil
```

Blocks VS Procs VS Lambdas
============

All of them are used for executing a single line or multiline code.

| Name | Object | Example | Object type | When to use |
|---|---|---|---|---|
| Blocks  | No  | { puts "Hello World" }              | -                                           | 1. when you want to pass blocks of code to a methods                <br> 2. arbitrary arguments <br> 3. blocks return from the current method |
| Procs   | Yes | p = Proc.new { puts "Hello World" } | p.class <br> Proc <br> p.lambda? <br> false | 1. similar to blocks but can store in variables                     <br> 2. arbitrary arguments <br> 3. Procs return from the current method  |
| Lambdas | Yes | l = lambda { puts "Hello World" }   | l.class <br> Proc <br> l.lambda? <br> true  | 1. it's a proc but acts like methods and can be stored in variables <br> 2. strict arguments    <br> 3. lambdas return from the lambda itself |


Array
============

How to iterate an Array
-----
There are multiple ways you can iterate an Array.

| No | Name | When to use |
|---|---|---|
| 1  | each             | when you want to just iterate                                                                                                                                                                                                                                        |
| 2  | each_with_index  | when you want both index and value                                                                                                                                                                                                                               |
| 3  | each_with_object | when you want to build a hash or reduce a collection to one object. It Iterates the given block for each element with an arbitrary object given and returns the first given object. It only works with a mutable object like Hash but not an immutable object like integer |
| 4  | each_index       | when you want just the indexes                                                                                                                                                                                                                                       |
| 5  | map              | returns an array containing the values returned by the block                                                                                                                                                                                                            |
| 6  | select           | adds value to a new array if your block returns true, returns ```[]``` otherwise. helpful when you are looking for a subset                                                                                                                                        |
| 7  | reject           | removes a value from a new array if your block returns true, returns ```[]``` otherwise. helpful when you are looking for a subset                                                                                                                                   |
| 8  | inject           | when you want a single value. helpful when you want to accumulate, concatenate                                                                                                                                                                                       |
| 9  | reduce           | reduce and inject methods are aliases                                                                                                                                                                                                                                |
| 10 | collect          | same as map                                                                                                                                                                                                                                                          |
| 11 | detect           | returns the first item in the array if your block returns true, returns ```nil``` otherwise. helpful when you are looking for something based on a business logic                                                                                                    |
| 12 | while            | when you want to iterate for a certain number of times                                                                                                                                                                                                                 |
| 13 | until            | when you want to iterate until something happens                                                                                                                                                                                                                     |
| 14 | for              | similar to each                                                                                                                                                                                                                                                      |
| 15 | times            | when you want to iterate ```n``` number of times                                                                                                                                                                                                                     |
| 16 | upto             | when you want to iterate upto ```n```, starting from ```m```, both inclusive, where ```n >= m```. when ```n < m``` it will run zero times                                                                                                                            |
| 17 | downto           | when you want to iterate downto ```n```, starting from ```m```, both inclusive, where ```n <= m```. when ```n > m``` it will run zero times                                                                                                                          |
| 18 | step             | when you want to iterate upto or downto ```n``` by incrementing or decrementing ```x``` steps starting from ```m```, both inclusive. the default value of step is ```1``` and for ```n``` it's infinity                                                                  |

### each

```ruby
# when you have single line block
salary = [399, 234, 566, 533, 233]
salary.each { |s| puts s }
# output
# 399
# 234
# 566
# 533
# 233
```

```ruby
# when you have a multiline block, you can replace the curly brackets {} with do and end
salary.each do |s|
  a = 10
  res = a * s
  puts res
end
# output
# 3990
# 2340
# 5660
# 5330
# 2330

# or you can do the same thing just using curly brackets {} and semicolons as separators instead of new lines
salary.each { |s| a = 10 ; res = a * s ; puts res }
```

### each_with_index

```ruby
salary = [399, 234, 566, 533, 233]
salary.each_with_index { |value, index| puts "#{index} #{value}" }
# output
# 0 399
# 1 234
# 2 566
# 3 533
# 4 233
```

### each_with_object

```ruby
colors = [{color: "red", count: 3}, {color: "red", count: 5}, {color: "black", count: 4}]
colors.each_with_object(Hash.new(0)) { |color, hash| hash["color_"+color[:color]] = color[:color].upcase; hash["count_"+color[:color]] += color[:count] }
# output
{"color_red"=>"RED", "count_red"=>8, "color_black"=>"BLACK", "count_black"=>4}

[1, 2, 3].each_with_object(0) { |number, sum| sum += number}
# output
# 0
# beacuse 0 is immutable, since the initial object is 0, the method returns 0
```

### each_index

```ruby
salary = [399, 234, 566, 533, 233]
salary.each_index { |i| puts i}
# output
# 0
# 1
# 2
# 3
# 4
```

### map

```ruby
salary = [399, 234, 566, 533, 233]
salary.map { |s|  s * 10  }
# returns
# [3990, 2340, 5660, 5330, 2330]

# on the other hand each returns the originl values
salary = [399, 234, 566, 533, 233]
salary.each { |s|  s * 10  }
# returns
# [399, 234, 566, 533, 233]
```

### select

```ruby
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
numbers.select { |n| n % 2 == 0 }
# now you have an array of even numbers, how cool is that
# [2, 4, 6, 8, 10]
# returns an empty array if there is no value that satisfy your logic
[1, 1, 1].select { |n| n % 2 == 0 }
# no even numbers
# []
```

### reject

```ruby
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
numbers.reject { |n| n % 2 == 0 }
# reject if the number is even, so now we have an array of odd numbers
# [1, 3, 5, 7, 9]
```

### inject

```ruby
numbers = [2, 2, 2, 2, 2]
numbers.inject{ |res, n| res + n }
# output is the result of the sum of all numbers
# if you do not set an initial value for res, then the first element of the array is used as the initial value of res
# 10

# now set the value of res with 11
numbers = [2, 2, 2, 2, 2]
numbers.inject(11) { |res, n| res + n }
# so 11 + 2, 13 + 2, 15 + 2, 17 + 2 and 19 + 2
# 21

# using symbol
numbers = [2, 2, 2, 2, 2]
numbers.inject(:+)
# output
# 10

# using initial value and a symbol
numbers = [2, 2, 2, 2, 2]
numbers.inject(11, :+)
# output
# 21
```

### reduce

```ruby
numbers = [2, 2, 2, 2, 2]
numbers.reduce(11, :+)
# output
# 21
```

### collect

```ruby
salary = [399, 234, 566, 533, 233]
salary.collect { |s| s > 400 }
# output
# [false, false, true, true, false]
```

### detect

```ruby
planets = ["Mercury", "Venus", "Earth", "Mars", "Jupiter", "Saturn", "Uranus", "Neptune"]
planets.detect { |name| name.start_with?("E") and name.end_with?("h") }
# output
# Earth

salary = [399, 234, 566, 533, 233]
salary.detect { |s| s > 1000 }
# output
# nil
```

### while

```ruby
planets = ["Mercury", "Venus", "Earth", "Mars", "Jupiter", "Saturn", "Uranus", "Neptune"]
index = 0
while index < planets.size
    puts "#{planets[index]}"
    index += 1
end
```

```ruby
a = 1
star = '*'
while a <= 10
    puts star
    star += '*'
    a += 1
end
```

### until

```ruby
planets = ["Mercury", "Venus", "Earth", "Mars", "Jupiter", "Saturn", "Uranus", "Neptune"]
index = planets.size - 1
until index < 0
    puts "#{planets[index]}"
    index -= 1
end
```

```ruby
a = 1
star = '*'
until star.length > 10
    puts star
    star += '*'
    a += 1
end
```

### for

```ruby
for value in [2, 3, 5, 7]
    puts value
end
```
### times

```ruby
10.times { puts "#{rand(1..100)}"}
# output
# will print 10 random numbers
```

```ruby
# just because you can doesn't mean you should iterate an array like this
data_sample = [2, 3, 5, 7]
data_sample.size.times { |index| puts "#{data_sample[index]}" }
# output
# 2
# 3
# 5
# 7
```

### upto

```ruby
data_sample = [2, 3, 5, 7]
0.upto((data_sample.size - 1) / 2) { |index| puts "#{data_sample[index]}" }
# output
# 2
# 3
```

### downto

```ruby
data_sample = [2, 3, 5, 7]
(data_sample.size - 1).downto(data_sample.size / 2) { |index| puts "#{data_sample[index]}" }
# output
# 7
# 5
```

### step

```ruby
1.step(20, 2) { |number| puts "#{number}"}
# output
# 1
# 3
# 5
# 7
# 9
# 11
# 13
# 15
# 17
# 19
```

```ruby
19.step(1, -2) { |number| puts "#{number}"}
# output
# 19
# 17
# 15
# 13
# 11
# 9
# 7
# 5
# 3
# 1
```

Boolean Enumerable methods
-----

| No | Name | When to use |
|---|---|---|
| 1  | all?     | when you want to check if all the elements satisfy your condition                       |
| 2  | any?     | when you want to check if at least one item satisfies your condition                   |
| 3  | one?     | when you want to check if precisely one element satisfies your requirement |
| 4  | none?    | when you want to check if none of the items satisfy your condition, opposite of all? |
| 5  | empty?   | when you want to check if the object is empty or not                                 |
| 6  | include? | when you want to check if the element exists in the object                              |

### all?

```ruby
[2, 4, 6, 8, 10].all? { |num| num % 2 == 0 }
# true
[1, 4, 6, 8, 10].all? { |num| num % 2 == 0 }
# false
```

### any?

```ruby
[1, 3, 5, 7, 10].any? { |num| num % 2 == 0 }
# true
[1, 3, 5, 7, 19].any? { |num| num % 2 == 0 }
# false
```

### one?

```ruby
[1, 3, 2, 5, 7].one? { |num| num % 2 == 0 }
# true
[1, 3, 2, 5, 4].one? { |num| num % 2 == 0 }
# false
```

### none?

```ruby
[1, 3, 5, 7, 9].none? { |num| num % 2 == 0 }
# true
[2, 3, 5, 7, 9].none? { |num| num % 2 == 0 }
# false
```

### empty?

```ruby
[].empty?
# true
[1, 3, 5, 7, 9].empty?
# false
```

How to check if a value exists in an Array (```include?```)
-----

```ruby
planets = ["Mercury", "Venus", "Earth", "Mars", "Jupiter", "Saturn", "Uranus", "Neptune"]
planets.include? "Mars"
# output
# true

planets.include? "Pluto"
# output
# false
```

How to get array size
-----

```ruby
# you can either use size or length, both are synonymous
planets = ["Mercury", "Venus", "Earth", "Mars", "Jupiter", "Saturn", "Uranus", "Neptune"]
planets.size
# output
# 8

planets.length
# output
# 8
```

How to clear an Array
-----

```ruby
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
numbers.clear
# output
# []
```

How to get the last element of an Array
-----

```ruby
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
numbers[-1]
# or
numbers.last
# output
# 10
```

How to merge two Arrays
-----

```ruby
a = ["tom", "mot", "otm"]
b = [2, 3, 5]

a.zip(b)

# outout
# [["tom", 2], ["mot", 3], ["otm", 5]]
```

How to sort an Array
-----

```ruby
primes = [7, 2, 3, 5]
sorted_primes = primes.sort
puts "#{sorted_primes}"
# output
# [2, 3, 5, 7]
```

or in-place sort

```ruby
primes = [7, 2, 3, 5]
primes.sort!
puts "#{primes}"
# output
# [2, 3, 5, 7]
```

```ruby
planets = ["Mercury", "Venus", "Earth", "Mars", "Jupiter", "Saturn", "Uranus", "Neptune"]
planets.sort
# output
# ["Earth", "Jupiter", "Mars", "Mercury", "Neptune", "Saturn", "Uranus", "Venus"]

planets.sort_by { |p| p }
# output
# ["Earth", "Jupiter", "Mars", "Mercury", "Neptune", "Saturn", "Uranus", "Venus"]

planets.sort_by { |p| p.length }
# output
# ["Mars", "Earth", "Venus", "Saturn", "Uranus", "Neptune", "Jupiter", "Mercury"]
```

How to get the maximum from an Array
-----

```ruby
primes = [7, 2, 3, 5]
primes.max_by { |p| p }
# output
# 7
```


Hash
============

```ruby
students = {name: 'John', email: 'john@col.com'}
# or
students = Hash.new
students = {name: 'John', email: 'john@col.com'}

puts "#{students[:name]}"
```

How to group by count
-----

```ruby
numbers = [1, 1, 1, 2, 4, 65, 55, 54, 55]
freq_hash = numbers.each_with_object(Hash.new(0)) { |number, hash| hash[number] += 1 }
puts "#{freq_hash}"
# output
# {1=>3, 2=>1, 4=>1, 65=>1, 55=>2, 54=>1}
```

or

```ruby
numbers = [1, 1, 1, 2, 4, 65, 55, 54, 55]
freq_hash = Hash.new(0)
numbers.each { |number| freq_hash[number] += 1 }
puts "#{freq_hash}"
# output
# {1=>3, 2=>1, 4=>1, 65=>1, 55=>2, 54=>1}
```

or from Ruby 2.7+

```ruby
numbers = [1, 1, 1, 2, 4, 65, 55, 54, 55]
numbers.tally
# output
# {1=>3, 2=>1, 4=>1, 65=>1, 55=>2, 54=>1}
```

What's the difference between Hash.new(0) and {}
-----

```ruby
# Hash.new(0) sets a default value of 0 for every key that do not exist in the hash.
# {} or Hash.new() sets nil for every key

h1 = Hash.new(0)
h1[:count] += 1
puts "#{h1[:count]}"
# output
# 1

puts "#{h1[:new_key]}"
# output
# 0

h2 = {}
h2[:count] += 1
# error
undefined method `+' for nil:NilClass
```

How to sort a Hash
-----

```ruby
hash = {e: 2, d: 3, c: 5, b: 7, a: 11}
hash.sort
# output
# [[:a, 11], [:b, 7], [:c, 5], [:d, 3], [:e, 2]]

hash.sort_by { |k, v| k }
# output
# [[:a, 11], [:b, 7], [:c, 5], [:d, 3], [:e, 2]]

hash.sort_by { |k, v| v }
# output
# [[:e, 2], [:d, 3], [:c, 5], [:b, 7], [:a, 11]]
```

How to get the maximum from a Hash
-----

```ruby
hash = {e: 2, d: 3, c: 5, b: 7, a: 11}
hash.max_by { |k, v| v }
# output
# [:a, 11]
```

Loop
============
How to break out from loop
-----

```ruby
# by using break keyword
salary = [399, 234, 566, 533, 233]
salary.each do |s|
    break if s == 566
    puts s
end
#output
# 399
# 234
```

How to skip inside a loop
-----

```ruby
# by using next keyword
salary = [399, 234, 566, 533, 233]
salary.each do |s|
    next if s == 533
    puts s
end
# output
# 399
# 234
# 566
# 233
```

How to repeat the current iteration
-----

```ruby
data = [456, 3000]
retry_count = 0
status = "network failure"
sum = 0
data.each do |d|
    if retry_count == 3
        status = "connection established"
        retry_count = 0
        redo
    elsif status == "network failure" and retry_count < 5
        puts "network failure #{retry_count}"
        retry_count += 1
        redo
    elsif status == "connection established"
        puts d
        sum += d
    end
end

# output of sum
# 3456
```

How to restart a loop
-----

```ruby
numbers = [2, 2, 44, 44]
sum = 0
begin
    numbers.each do |s|
        if rand(1..10) == 5
            puts "hi 5, let's do it again!"
            sum = 0
            raise "hi 5"
        end
        puts s
        sum += s
    end
rescue
    retry
end
```

Classes
============

```ruby
class Person
    # when you create a new object, it looks for a method named initialize and executes it, like a constructor in java
    # def initialize(name, number)
    #    @name = name
    #    @number = number
    # end

    # instance variable
    # @name

    # class variable
    # @@count

    # attr_accessor acts as a getter and setter for the following instance attributes
    attr_accessor :name, :number

    # class variable must be initialized
    @@count = 0

    def self.count
        @@count
    end

    def self.count=(count)
        @@count = count
    end

    def initialize
        @@count += 1
    end
end

# create an instance of the Person class
p1 = Person.new

# set attributes of the Person class
p1.name = "Yukihiro Matsumoto"
p1.number = 9999999999

# get attributes of the Person class
puts "#{p1.name}"
puts "#{p1.number}"
puts "#{Person.count}"

# Yukihiro Matsumoto
# 9999999999
# 1

p2 = Person.new
p2.name = "Yukihiro Matsumoto"
p2.number = 9999999999

# get attributes of the Person class
puts "#{p2.name}"
puts "#{p2.number}"
puts "#{Person.count}"

# Yukihiro Matsumoto
# 9999999999
# 2

# set class variable
Person.count = 3
puts "#{Person.count}"
# 3
```

How to inherit a class
-----

```ruby
class Person
    attr_accessor :name, :number
end

# use < symbol to inherit methods and attributes from the parent class
class Student < Person
    attr_accessor :id
end

s = Student.new

s.name = "James Bond"
s.number = 700
s.id = 678

puts "#{p.name}"
James Bond

puts "#{p.number}"
700

puts "#{p.id}"
678
```

How to check instance type
-----
```ruby
# Returns true if the object is an instance of the given class, not a subclass or superclass
class Vehicle; end
class Car < Vehicle; end
class Audi < Car; end

car = Car.new
car.instance_of? Vehicle
false
car.instance_of? Car
true
car.instance_of? Audi
false

a = 7
a.instance_of? Integer
true
a.instance_of? Numeric
false
```
Print all method names of a class
-----

```ruby
puts (String.methods).sort
# Exclude methods that are inherited from Object class
puts (String.methods - Object.public_instance_methods).sort
```

Check if a Class has a particular method
-----

```ruby
String.respond_to?(:prepend)
true
String.respond_to?(:append)
false
```

Modules
============
Modules are used for combining similar methods, so that other classes or modules can use it. You can not instantiate a module (like abstract classes in Java)

```ruby
module MyRandomHelper
    def roll_dice
      rand(1..6)
    end
end

class Person
    attr_accessor :name, :number
end

class Player < Person
    include MyRandomHelper
    attr_accessor :score
end

p = Player.new
p.roll_dice
```

```ruby
TODO
```

Operator Overloading
============
```ruby
class Vector
    attr_accessor :x, :y

     def initialize(x, y)
        @x = x
        @y = y
    end

    def +(second)
        Vector.new(@x + second.x, @y + second.y)
    end

    def -(second)
        Vector.new(@x - second.x, @y - second.y)
    end

    def *(second)
        Vector.new(@x * second.x, @y * second.y)
    end

    def /(second)
        Vector.new(@x / second.x, @y / second.y)
    end

    def to_s
        return "(#{@x}, #{@y})"
    end

end
```

```ruby
v1 = Vector.new(5, 10)
v2 = Vector.new(4, 9)

puts v1 + v2
puts v1 - v2
puts v1 * v2
puts v1 / v2
```

Exception Handling
============
```ruby
begin
    puts 'before the raise'
    raise 'raise an exception'
    puts 'after the raise'
rescue
    puts 'rescued'
end
```
```ruby
begin
    raise StandardError, 'standard error occurred'
rescue StandardError => e
    puts "#{e.class}: #{e.message}"
    puts e.backtrace.inspect
end
```

```$!``` contains the raised exception
```$@``` contains the exception backtrace

```ruby
begin
    raise StandardError, 'standard error occurred'
rescue StandardError
    puts "#{$!.class}: #{$!.message}"
    puts "#{$@}"
end
```

```retry``` re-executes the code inside begin end block

```ruby
retry_count = 1

begin
    puts "retry count: #{retry_count}"
    retry_count += 1
    raise 'raise an exception'
rescue
    retry if retry_count <= 5
end
```

Custom exception

```ruby
class MyException < Exception
end

begin
    raise MyException, 'my exception occurred'
rescue MyException
    puts "#{$!.class}: #{$!.message}"
    puts "#{$@}"
end
```

Catch multiple exceptions

```ruby
begin
    raise 'i am a string'.call
rescue NoMethodError => e
    puts "#{$!.class}: #{$!.message}"
rescue ZeroDivisionError => e
    puts "#{$!.class}: #{$!.message}"
end

```

[Further readings](https://ruby-doc.org/core-2.6.4/Exception.html)


Regular expression
============

```ruby
a = "Better a diamond with a flaw than a pebble without"
a[/(\w+)/]

# output
# "Better"

a[/(\w+) (\w+)/]

# output
# "Better a"

a[/(?<one>\w+) (?<two>\w+)/, :two]
# output
# "a"
```

Miscellaneous
============
How to generate random number
-----

```ruby
rand(max=0)

# when calling it without an argument, rand returns a floating point number between 0.0 (including) and 1.0 (excluding), under the hood max.to_i.abs == 0
rand

# output
# 0.055758056734957595

# when the argument value is greater than or equal to 1, rand returns a integer between 0 (including) and that number (excluding), under the hood max.to_i.abs >= 1
rand(100)

# output
# 7

# generating number between 2 numbers both inclusive
rand(150..170)

# output
# 167

# generating number between 2 numbers, the last number is not inclusive
rand(1...10)

# output
# 4
```

Check the syntax of a Ruby file
-----
```ruby
ruby -c filename.rb
```

Concatenate String in a loop
-----

```ruby
words = ["Lorem", "ipsum", "dolor", "sit", "amet"]
words.map { |word| word.downcase }.join(' ')

# output
# "lorem ipsum dolor sit amet"
```

CamelCase String split
-----

```ruby
sentence = "ThereIsNoSpoon"
words = sentence.split(/(?=[A-Z])/)

# output
# ["There", "Is", "No", "Spoon"]
```

Ruby scripts
-----
<a href="https://github.com/lifeparticle/Ruby-Cheatsheet/tree/master/Scripts"><img alt="ruby-scripts" src="https://img.shields.io/badge/ruby-scripts-red.svg?style=flat"/></a>

Books and other resources
============
1. [Ruby doc](https://ruby-doc.org/)
2. [How to use Ruby’s English and/or operators without going nuts](http://www.virtuouscode.com/2014/08/26/how-to-use-rubys-english-andor-operators-without-going-nuts/)
3. [What is attr_accessor in Ruby?](https://stackoverflow.com/questions/4370960/what-is-attr-accessor-in-ruby)
4. [Ruby Module Mixin Awesomeness](https://johnmcaliley.wordpress.com/2010/03/10/ruby-module-mixin-awesomeness/)
5. [Tutorials](https://www.cosmiclearn.com/ruby/index.php)
6. [Pattern matching - New feature in Ruby 2.7](https://speakerdeck.com/k_tsj/pattern-matching-new-feature-in-ruby-2-dot-7?slide=24)

Bug Reports and Feature Requests
============
Please create an issue with as much information you can. Thank you.

Contribution Guidelines
============
<a href="https://github.com/lifeparticle/Ruby-Cheatsheet/blob/master/CONTRIBUTING.md"><img alt="contribution guidelines" src="https://img.shields.io/badge/contribution-guidelines-brightgreen.svg?style=flat"/></a>

Author
============
Neilblaze (https://github.com/neilblaze)

License
============
MIT License
