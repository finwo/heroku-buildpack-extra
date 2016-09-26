Heroku buildpack: extra
=======================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for adding custom steps to building your application.

Need extra steps like gulp, a custom permission script or something more exotic? You can now add them using this buildpack to prevent your endless search for the right tools.

## Installation

#### Heroku toolchain
```
heroku buildpacks:add "https://github.com/finwo/heroku-buildpack-extra.git"
```

#### `.buildpacks` file

```
echo "https://github.com/finwo/heroku-buildpack-extra.git" >> /path/to/app/.buildpacks
```

## Usage

Create or modify the `.extra` file inside your app's root directory. It's run like a regular executable, so feel free to make this a bash script, nodejs script or any other system executable.

Example:
```
#!/usr/bin/env bash

# Run the gulp build task
gulp build
```

## Contributing

After checking the [Github issues](http://github.com/finwo/heroku-buildpack-extra/issues) and confirming that your request isn't already being worked on, feel free to spawn a new fork of the `develop` branch & send in a pull request. Keep in mind to describe what your intent is and why you want the feature you've just build merged into the main repository.

The `develop` branch is merged into the `master` periodically after confirming it's stable, to ensure the master always contains a production-ready version.

## License

MIT License

Copyright (c) 2016 Finwo

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
