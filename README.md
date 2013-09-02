# Behat Parallel #

<img src="http://stream1.gifsoup.com/view6/2418917/parallel-park-like-a-boss-o.gif" alt="Parallel" align="right" width="280"/>

**Version:** *0.1.0*

Run your behat tests in parallel processes.
The shell script simply wraps `find` to iterate through the test directory to get the tests,
and `xargs` to run each test in a separate process.
You can still make use of all standard Behat command line arguments.

It can be installed in whichever way you prefer, but I recommend [Composer][packagist].
```json
{
    "require": {
        "adlawson/behat-parallel": "~0.1.0"
    }
}
```


### Command line ###
```bash
$ behat-parallel -h

    Usage: behat-parallel [options] -- [behat options]

    Options:

        -b, --bin        Behat binary (default: ./vendor/bin/behat)
        -f, --features   Path to the features to run (default ./features/*.feature)
        -h, --help       This help prompt
        -p, --processes  Maximum parallel processes (default: 4)

    Example:

        behat-parallel --features=/path/to/features/**/*.feature -- --tags='@javascript'
```


### Credits ###
This project was inspired by [Linus Norton's][linus] [grunt-parallel-behat][grunt-behat] but it can be used in projects
without Grunt.


### Contributing ###
I accept contributions to the source via Pull Request.
I'm pretty pedantic about git practices, coding style and naming conventions, so don't be offended if I ask you to
ammend your commits.
```bash
$ make install
$ make tests
```

If you have [Vagrant][vagrant] installed, you can build our dev environment to assist development.
The repository will be mounted in `/srv`.
```bash
$ vagrant up
$ vagrant ssh

Welcome to Ubuntu 12.04 LTS (GNU/Linux 3.2.0-23-generic x86_64)
$ cd /srv
```


### License ###
The content of this library is released under the **MIT License** by **Andrew Lawson**.<br/>
You can find a copy of this license at http://www.opensource.org/licenses/mit or in [`LICENSE`][license]

<!-- URLs -->
[packagist]: https://packagist.org/packages/adlawson/behat-parallel
[vagrant]: http://vagrantup.com
[linus]: https://github.com/linusnorton
[grunt-behat]: https://github.com/linusnorton/grunt-parallel-behat
[license]: https://github.com/adlawson/behat-parallel/blob/master/LICENSE
