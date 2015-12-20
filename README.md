# Here be dragons

This is an extreme work in progress, so be cautious about cloning this
code any time soon.

Also, this code at the moment is (c) Harish Narayanan 2015 **All
Rights Reserved**. So you probably shouldn't be pulling it anyway
since that doesn't give you much scope to do anything with it.

## TODO

The following list is in addition to the liberal `TODO`s sprinkled all
over the code.

- Expose RSS feed
- Replace the above non-license with something friendlier
- Replace this file with a useful README
- Go through the TODOs in the code and this list and create a
  collection of isues on GitHub
- Replace placeholder favicon.ico, apple-touch-icon.png, tile.png
  etc. with something custom
- Grep for and remove all remaining egregious uses of inline styling
- Make large images in article pages overflow the container and go to
  the full width of the page
- Create archetypes for each primary content type on the site
- Incorporate some taxonomy for the articles (e.g. tags like Devops,
  Kubernetes, Django) to later start connecting up sets of
  articles. Similarly for research articles.
- Reintroduce a meta section of the site... or perhaps move relevant
  information in this README and link to it?
- Incorporate online learning portfolio somewhere?
- Highlight recommended classes
- Add the winter in Asia gallery?
- Look at GitHub for a reminder of recent projects
- Canonicalize breakpoints of Pure and Skeleton
- Computational biology
- - applied mathematician
  - computational biologist
  - all-around web technologist
- Embed relevant talks in research articles
- Incorporate good ideas from https://github.com/h5bp/server-configs-nginx

## Notes

### Setup the server
````
cd config
ansible-playbook site.yml -i servers/personal-site
````

### Editing the site
````
git clone git@github.com:hnarayanan/harishnarayanan.org.git
cd harishnarayanan.org
$PATH/hugo server --buildDrafts --watch
````

### Update Site

````
../hugo --buildDrafts
rsync -aPvhe ssh --delete --exclude-from=/Users/harish/Scratch/Backup/exclude2 public/ ubuntu@harishnarayanan.org:/home/ubuntu/harishnarayanan.org
````

### Check Links

````
wget --spider -o wget.log -e robots=off -w 1 -r -p https://harishnarayanan.org/
````
