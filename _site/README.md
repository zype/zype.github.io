#To View Your Site Locally:

    bundle exec jekyll serve --config _config.yml,_config_dev.yml

Then in your browser go to http://localhost:4000/ to see the site. (This uses the dev config file, so files are displayed from your local machine if they aren’t yet on prod.)

#To Add Pages

See http://jekyllrb.com for more info on using jekyll and adding pages.

#To Deploy

    bundle exec jekyll build
    git add .
    git cm -m ‘your commit msg goes here’
    (checkout master and merge if necessary)
    git push

Pushing to github will deploy the docs automatically.


#Keeping github-pages up to date

Github updates its gem a lot, so we need to keep our locals up to date and rebuild occasionally!

    bundle update github-pages

#To run a health check

Checks your GitHub Pages site for common DNS configuration issues.

    bundle exec github-pages health-check

#Github Pages Docs

    https://help.github.com/articles/using-jekyll-with-pages/#installing-jekyll
