# Instructions for Updating Lab Website

*Daniel note: these installation instructions need to be updated, but they are
mainly if you want to preview the website. You may need to fix these
instructions depending on your system.*


<details>
<summary>
Instructions to preview the lab website (on OS X systems):
</summary>

In progress.

However, Daniel was able to preview on a clean Macbook Pro (OS 13.2.1) just with this command to get things started:

```
bundle install --path vendor/bundle
```

(Run it inside the home directory, i.e., `slurm-lab-usc.github.io/`.)

Then `bundle exec jekyll serve` worked.

</details>

<details>
<summary>
Instructions to preview the lab website (on Ubuntu machines):
</summary>

Install dependencies. On Ubuntu:

```
sudo apt install ruby-bundler ruby-dev
sudo apt-get install build-essential
sudo gem install http_parser.rb -v 0.8.0
```

[Daniel (May 07, 2025): might not be needed as we already include such an exclude in `_config.yml` now.]

Add `vendor` in `_config.yml` line 285:

```
exclude:
  - vendor
```

Inside the `~/slurm-lab-usc.github.io` directory, run `bundle install`. You might need `sudo`.

Assuming that worked, then do `bundle exec jekyll serve`:

```
seita@blackcoffee:~/slurm-lab-usc.github.io$ bundle exec jekyll serve
Configuration file: /home/seita/slurm-lab-usc.github.io/_config.yml
            Source: /home/seita/slurm-lab-usc.github.io
       Destination: /home/seita/slurm-lab-usc.github.io/_site
 Incremental build: disabled. Enable with --incremental
      Generating... 
                    done in 0.25 seconds.
 Auto-regeneration: enabled for '/home/seita/slurm-lab-usc.github.io'
    Server address: http://127.0.0.1:4000
  Server running... press ctrl-c to stop.
```

And you should be able to access the website locally by going to
http://127.0.0.1:4000 in your web browser (Chrome is suggested). 

Daniel has tested this on an Ubuntu 18.04 machine.
Zeyu has tested this on an Ubuntu 20.04 physical machine and an Ubuntu 22.04 virtual machine.
</details>

**You can add yourself by editing `members.md`**. See the pattern we use for
this.  If you are updating this website, make changes locally and please
preview to make sure it is correct. **Then submit a pull request to the main branch.** You can do
this by making a fork of this repository.

For adding photos, please add them to the `img/people` folder. Please also make
them equal in height and width ratio (i.e., the image is "square"). I recommend
photos that are about 1MB or smaller in size.

For step-by-step instructions, please refer to https://docs.google.com/presentation/d/10d1aXpl_xcZ1eZSv1WFHLoQEZaeZA-bI/edit?usp=sharing&ouid=102267118200150194489&rtpof=true&sd=true

# References

The code for this website is from https://github.com/daattali/beautiful-jekyll.
