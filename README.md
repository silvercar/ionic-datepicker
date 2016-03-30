# ionic-datepicker

# Installation

1. Clone the repo `git clone git@github.com:silvercar/ionic-datepicker.git` at the same level as asf-hybrid and sc-web-core.
2. Do cd to the `ionic-datepicker/` directory.
3. Install required node modules via `npm install`.
4. Install required bower components via `bower install`.
5. Do `git pull` in `sc-web-core`, to get modified `bower.json`.
6. Do `git pull` in `asf-hybrid`, to get modified `app/bower.json`.

-- 

# Workflow 1: the shitty way

Some of this sucks because of the extra hoops you have to jump through.  :(

1. Modify files in `ionic-datepicker/src` with new code.
2. Run `gulp build` from the top level of ionic-datepicker. That crunches all `src/` changes into `dist/ionic-datepicker.bundle.min.js`.  
3. Commit the modified source to master, along with `dist/ionic-datepicker.bundle.min.js`.
4. Run `git push origin master`.
5. Do cd to `asf-hybrid/app` and run `bower update`. This should do the browser live reload with your changes.


# Workflow 2: slightly less terrible

If you want to eliminate a step, in the asf-hybrid/app/bower.json file, change:

```"ionic-datepicker": "git@github.com:silvercar/ionic-datepicker.git#master"```

to

```"ionic-datepicker": "file:///Users/demos/Documents/Projects/ionic-datepicker/.git#master"```

except change that file path to wherever your ionic-datepicker is on your Mac.  Then, you can do Workflow 1 but skip step 4 because it's looking in your local repo, rather than the one on github, so no push is necessary.


# Workflow 3: good (under construction

Should be that just modifying files in ionic-datepicker rebuilds everything for you, but I'm still working on that as a side project so it'll probably never happen.
