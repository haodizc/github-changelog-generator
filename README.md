GitHub Changelog Generator
==================

[![Gem Version](https://badge.fury.io/rb/github_changelog_generator.svg)](http://badge.fury.io/rb/github_changelog_generator)

Changelog generation has never been so easy.

This script automatically generate change-log from your tags and merged pull-requests.

## Installation:
	[sudo] gem install github_changelog_generator

## Usage
**It's really simple**: 

- `cd` to your Project folder with configured git and just type:

		github_changelog_generator

- from anywhere:

		github_changelog_generator -u github-username -p github-project
     
As output you will get `CHANGELOG.md` file with *pretty Markdown-formatted* changelog.

## Params:
Type `github_changelog_generator --help` for detailed usage.

    Usage: changelog_generator [options]
    -u, --user [USER]                Username of the owner of target GitHub repo
    -p, --project [PROJECT]          Name of project on GitHub
    -t, --token [TOKEN]              To make more than 50 requests this script required your OAuth token for GitHub. You can generate it on https://github.com/settings/applications
    -h, --help                       Displays Help
    -v, --[no-]verbose               Run verbosely. Default is true
        --[no-]issues                Include closed issues to changelog. Default is true
        --[no-]issues-without-labels Include closed issues without any labels to changelog. Default is true
        --[no-]pull-requests         Include pull-requests to changelog. Default is true
    -l, --last-changes               Generate log between last 2 tags only
    -f, --date-format [FORMAT]       Date format. Default is %d/%m/%y
    -o, --output [NAME]              Output file. Default is CHANGELOG.md
        --labels  x,y,z              List of labels. Issues with that labels will be included to changelog. Default is 'bug,enhancement'

## Examples:

- Look at changelog for **[CHANGELOG.md](https://github.com/skywinder/Github-Changelog-Generator/blob/master/CHANGELOG.md)** for this project
- This changelog: [ActionSheetPicker-3.0/CHANGELOG.md](https://github.com/skywinder/ActionSheetPicker-3.0/blob/master/CHANGELOG.md)  was generated by command:

		github_changelog_generator -u skywinder -p ActionSheetPicker-3.0


## FAQ:
Since GitHub allow to make only 50 requests without authentication it's recommended to run this script with token

**You can easily [generate it here](https://github.com/settings/applications)**.

And:

- Run with key `-t [your-16-digit-token]` that 
- Or add to your shell variable CHANGELOG_GITHUB_TOKEN and specify there your token

So, if you got error like this:
>! /Library/Ruby/Gems/2.0.0/gems/github_api-0.12.2/lib/github_api/response/raise_error.rb:14:in `on_complete'

It's time to create this token or wait for 1 hour before GitHub reset the counter for your IP.

## Am I missed some essential feature?

**Nothing is impossible!** Open an [issue](https://github.com/skywinder/Github-Changelog-Generator/issues/new) and let's get this generator better together!

*Bug reports, feature requests, patches, well-wishes are always welcome!*

## Contributing

1. Create an issue to discuss about your idea
2. [Fork it] (https://github.com/skywinder/Github-Changelog-Generator/fork)
3. Create your feature branch (`git checkout -b my-new-feature`)
4. Commit your changes (`git commit -am 'Add some feature'`)
5. Push to the branch (`git push origin my-new-feature`)
6. Create a new Pull Request

## License

Github Changelog Generator is released under the [MIT License](http://www.opensource.org/licenses/MIT).
