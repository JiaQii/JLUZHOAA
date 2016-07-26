## Special Install For Refinery ##

#### rails ####
Rails - Version 4.2.6

	gem install rails --version 4.2.6
#### sqlite3 ####
1. Install the Ruby Devkit for your setup (x64 or x32)
2. Download and extract the autoconf package from [Sqlite.org](https://www.sqlite.org/download.html)
3. Run msys.bat (inside the ruby devkit root folder)
4. cd into the path where you downloaded the sqlite source
5. Run "./configure"
6. Run "make"
7. Run "make install"

Get the sqlite3 gem again, specifying the platform and the path to the newly compiled binaries
	
	gem install sqlite3 --platform=ruby -- --with-sqlite3-inlcude=[path\to\sqlite3.h] --with-sqlite3-lib=[path\to\sqlite3.o]

For Example
	
	gem install sqlite3 --platform=ruby -- --with-sqlite3-inlcude="c:\sqlite3" --with-sqlite3-lib="c:\sqlite3\.libs"
#### ImageMagick ####
[ImageMagick](http://www.refinerycms.com/guides/installation-prerequisites)

[Follow the instructions](http://www.imagemagick.org/script/binary-releases.php#windows)

### Setup Instruction

http://www.refinerycms.com/download
https://github.com/refinery/refinerycms

#### Setup Fail (Windows) ####
1. cannot load such file -- sqlite3/sqlite3_native (LoadError) [Resolution1](http://stackoverflow.com/questions/17643897/cannot-load-such-file-sqlite3-sqlite3-native-loaderror-on-ruby-on-rails)
[Resolution2](http://rubyonwindowsguides.github.io/book/ch02-05.html)
2. Could not load 'active_record/connection_adapters/sqlite3_adapter'. Make sure that the adapter in config/database.yml is valid.

Ruby sucks on windows!!!

[Install Ruby on Linux](http://www.ruby-lang.org/en/documentation/installation/#apt)
