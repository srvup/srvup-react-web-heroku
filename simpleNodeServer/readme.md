Srvup React.js using Node.js
====
Simple deploy

```

$ git clone https://github.com/srvup/srvup-react-web-heroku
$ cd srvup-react-web-heroku/simpleNodeServer/
$ rm -rf .git
$ git init
$ git add --all
$ git commit -m "Initial commit"
$ heroku apps:create
$ git push heroku master
```


Updating the client:
Assuming you're using some version of [this repo](https://github.com/srvup/srvup-react-web), then you can do the following within that repo:
```
$ cd path/to/your/srvup-react-web/
$ npm run build

```

Copy the `build/` director from `srvup-react-web` to your `srvup-react-web-heroku` directory.

```
cp -a path/to/your/srvup-react-web/build/. path/to/your/srvup-react-web-heroku/simpleNodeServer/build/
```

In my case, it was:
```
cp -a /Users/jmitch/dev/srvup-react-web/build/. /Users/jmitch/dev/srvup-react-web-heroku/simpleNodeServer/build/
```

```
$ git add --all
$ git commit -m "Updated srvup-react-web client"
$ git push heroku master
```

Boom you're project is up.