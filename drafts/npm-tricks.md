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
