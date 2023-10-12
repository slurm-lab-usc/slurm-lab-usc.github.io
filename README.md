# Instructions for Updating Lab Website

Install dependencies. On Ubuntu:

```
sudo apt install ruby-bundler ruby-dev
```

Inside the `~/slurm-lab-usc.github.io` directory, run `bundle install`.

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
http://127.0.0.1:4000 in your web browser. 

If you are updating this website, make changes locally and preview to make sure
it is correct. **Then submit a pull request. Do NOT submit it directly to the
`main` branch.**

For adding photos, please add them to the `img/people` folder. Please also make
them roughly in "portrait" mode in a 1.5-to-1 ratio, so that the photo is about
1.5x "taller" than it is wide.


# References

The code for this website is from https://github.com/daattali/beautiful-jekyll.
