#npm tricks

## Set you npm init defaults
I find my self using ```npm init``` a lot for any new project or test I start, then introducing
always the same info, author, version ( I don't like that 1.0.0 default :( ), license, etc.

Here comes a piece of advice, you can set you npm init default to anything suitable for you.
I find specailly helpfull these ones:

```
$ npm config set init.author.name "Alvaro Pinot"
$ npm config set init.author.email foo@gmail.com
$ npm config set init.author.url http://github.com/alvaropinot
$ npm config set init.version 0.0.1
$ npm config set init.license MIT
```

If your are a bit curious or you just want to see your new defaults you can run ```$ npm config ls -l```  for a full list of
npm settings.

## Override package.json config at runtime with arguments
Extracted from 
```$ npm help 7 config```

> "config" keys are overwritten in the environment if there is  a  config
param  of  <name>[@<version>]:<key>.   For example, if the package.json
has this:

 ```js
 { "name" : "foo"
 , "config" : { "port" : "8080" }
 , "scripts" : { "start" : "node server.js" } }
 ```

> and the server.js is this:

 ```js
http.createServer(...).listen(process.env.npm_package_config_port)
```

> then the user could change the behavior by doing:

 ```$ npm config set foo:port 80```

> See npm help 5 package.json for more information.
