# HANUMAN Jekyll Theme

[![Build Status](https://travis-ci.org/samanyougarg/hanuman.svg?branch=master)](https://travis-ci.org/samanyougarg/hanuman)

Hanuman is a minimal yet powerful Jekyll theme for your blogs and websites.

It is built using the open source AMP Start framework and can be customized as per your requirements.

## Live Demo
## [Hanuman](https://samanyougarg.com/hanuman)
![Hanuman](/Screenshots/hanuman.jpg "Hanuman Preview")


## Features

- Minimal
- Responsive
- Syntax Highlighting for code
- Cover Images for homepage and blog posts
- Social Sharing
- Simple Navigation Menu
- Pagination
- Google Analytics
- Can be easily installed via "theme gem"
- Github Pages support
- Easily Customisable


## Installation

There are different ways to install the theme - 

### 1. Cloning the repository and updating settings
1. Fork this repository and clone the forked repository.
2. Update the _config.yml file as per your requirements.
3. Add your posts to the _posts directory.
4. Deploy to Github Pages or your own server.

### 2. Ruby Gem Method
Add this line to your Jekyll site's `Gemfile`:

```ruby
gem "hanuman"
```

And add this line to your Jekyll site's `_config.yml`:

```yaml
theme: hanuman
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install hanuman

You'll also need to copy or create the _config.yml file just like in this repository. Similarly, you'll need to have a navigation.yml and author.yml in your _data directory.

### 3. Jekyll Remote Theme
1. Create or update your Gemfile with the following - 

```ruby
source "https://rubygems.org"
gem "github-pages", group: :jekyll_plugins
gem "jekyll-remote-theme"
```

2. Update the bundled gems using `bundle` command.

3. Add `remote_theme: "hanuman"` to your `_config.yml`.

4. Add `jekyll-remote-theme` to the plugins array of your `_config.yml` - 

```yaml
plugins:
  - jekyll-remote-theme
```    
  
## Deploying to Github Pages

There are 2 methods you can use to deploy the site to Github Pages - 

1. Run `bundle exec jekyll serve` inside your cloned repository. Push the contents of the resulting _site to your Github Pages repository.

2. Using Travis CI
- Set up travis-ci for your fork. 
- Generate your secure token with the travis gem:
  Run `gem install travis` on your terminal.
- Grab the GH_TOKEN from https://github.com/settings/tokens
- Then run `travis encrypt 'GIT_NAME="YOUR_USERNAME" GIT_EMAIL="YOUR_EMAIL" GH_TOKEN=YOUR_TOKEN'`
- Add the token to your .travis.yml file.

  Now you just need to push the files. Travis will generate the HTML files and automatically push them to your gh-pages branch. 
This is the setup I am using.

## Usage

### _config.yml
Update _config.yml with your respective settings like updating your site's name, description etc...

### Styling
AMP has a limitation that you can only use inline css.
All the CSS for this theme is in the styles.scss file in the includes directory.

#### Changing the Default Color
In the styles.scss file in the includes directory, you can change the hex value of $theme-color to the color you would like your site to use.

### Author Information
Author information is present in the author.yml file in the _data folder. You can update the fields of that file as per your requirements.

### Sidenav
Sidenav can be updated from the navigation.yml file in the _data folder.

## Writing Posts
You can write posts just as you would in Jekyll, the only difference being that AMP has some strict guidelines on including external content.

You cannot use Markdown format or normal HTML tags. AMP provides its own custom tags for images, videos etc...

### Examples - 

**Images**
`<amp-img src="welcome.jpg" alt="Welcome" height="400" width="800"></amp-img>`

**Videos**
`<amp-youtube data-videoid="mGENRKrdoGY" layout="responsive" width="480" height="270"></amp-youtube>`

[See Full AMP Documentation.](https://www.ampproject.org/docs/)

### Using AMP Components
Some AMP components require you to specify external scripts before using them.
You can specify these scripts in the head.html file in the includes directory after the already imported scripts and then use these components in any post.

## Validating your page with AMP
AMP provides built-in validator to validate your pages so that they can rendered quickly. 

You can access this validator by opening the Developer Console in your browser and adding #development=1 to any url of your site.

Example - 
http://localhost:4000/#development=1

If you have errors on your page, AMP will list those for you in the console. If you do not have any errors, you'll get a message "AMP Validation Successful" on your console.

## Enabling Google Analytics
1. Set up your Analytics Tracking ID in _config.yml.
2. Remove {% comment %} and {% endcomment %} tags in the default.html file in layouts directory.

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/samanyougarg/hanuman. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

To submit a pull request - 

1. Fork/clone the repository.
2. Develop.
3. Create a new branch from the master branch.
4. Open a pull request on Github describing what was fixed or added.

## Thanks
Hanuman is based on [amplify](https://github.com/ageitgey/amplify) jekyll theme. Thank You.

## License

The theme is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

