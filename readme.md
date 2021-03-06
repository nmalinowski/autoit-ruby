# Ruby Wrapper for AutoIt

**A wrapper for the AutoItX3 DLL on windows to control the windows API**

## What is AutoIt?

_Taken from the [AutoIt Website](http://www.autoitscript.com/autoit3/index.shtml)_

AutoIt v3 is a freeware BASIC-like scripting language designed for automating the Windows GUI and general scripting. It uses a combination of simulated keystrokes, mouse movement and window/control manipulation in order to automate tasks in a way not possible or reliable with other languages (e.g. VBScript and SendKeys). AutoIt is also very small, self-contained and will run on all versions of Windows out-of-the-box with no annoying "runtimes" required! 

AutoIt was initially designed for PC "roll out" situations to reliably automate and configure thousands of PCs. Over time it has become a powerful language that supports complex expressions, user functions, loops and everything else that veteran scripters would expect.

**Also supplied is a combined COM and DLL version of AutoIt called AutoItX that allows you to add the unique features of AutoIt to your own favourite scripting or programming languages!**

## Problems with AutoIt and how Ruby can help

To use AutoIt normally you have to learn an entirely new programming language. This language is similar to Visual Basic, and doesn't have support for a lot of Ruby's advanced features. 

The goal of this project is to bring Windows API access and automation to Ruby. Hopefully this will attract more people to using Ruby on Windows and suppress all doubts that Windows is not a first-class language for windows.

## Example Use

1. The AutoItX3 DLL must be installed using the [main AutoIt installer](http://www.autoitscript.com/autoit3/downloads.shtml).

2. Include the file in your project like this:

        require 'autoitwrapper.rb' # make sure the file is in the same directory
        include AutoIt # useful if you don't want to always use AutoIt:: before everything

3. Start automating windows. (TODO: more examples to come)

        # Clipboard Access
        Clipboard.puts "I love ruby!", " Go to http://github.com/stevenheidel/ruby-autoit to contribute."
        Clipboard.gets.upcase[0..11] #=> "I LOVE RUBY!"

4. Read the documentation for how to use. (TODO: generate RDoc documentation)

5. Contribute your opinions on how you'd like to be able to use AutoIt from Ruby.

## Contribute

Things to do:

- Add remainder of functions as described in the AutoItX3 help file
- Standardize the return values and error outcomes
- Send me ideas on what functions/classes should do in order to make the most sense
- Add tests, documentation, and more examples

## Useful Links

- [AutoItX3 Support Forum](http://www.autoitscript.com/forum/index.php?s=2d5bc3fac66e734a24edf8caaa6a1842&showforum=14)
- [Good idea to make a library](http://tech.waltco.biz/2008/02/23/use-swig-to-build-a-ruby-extension-to-wrap-a-windows-dll/)
- [Useful Introduction](http://actsasbuffoon.wordpress.com/2008/12/30/introduction-to-autoitx3/)
* [Eventual Goal: No relying on AutoIt](http://raa.ruby-lang.org/project/win32-guitest/)