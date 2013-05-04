# Heroku buildpack for meteor

## Usage

```
% heroku create --stack cedar --buildpack https://github.com/asyazwan/heroku-buildpack-meteor.git
```

## Example

Create a sample app with 'meteor'

```
% meteor create --example wordplay
wordplay: created.

To run your new app:
   cd wordplay
   meteor
```

Put it in git.

```
% cd wordplay
% git init
Initialized empty Git repository in /tmp/a/wordplay/.git/
% git add .
% git commit -m "Sample wordplay app!"
```

Create your heroku app

```
% heroku create --stack cedar --buildpack https://github.com/asyazwan/heroku-buildpack-meteor.git
```

Configure your ROOT_URL and MONGOLAB_URI settings
```
% heroku config:add ROOT_URL=<insert_url_created_above_here>
% heroku config:add MONGOLAB_URI=<insert_mongolab_uri_here>
```

Deploy it

```
% git push heroku
```

Enjoy!
