# Reverse Engineer (soon)

why => For save the old world :p The death of [flash](https://www.adobe.com/fr/products/flashplayer/end-of-life.html) meant the death of a large part of my childhood games,
I joined the titanic project of saving the [Motion Twin](https://motion-twin.com) games : « [Eternal Twin](https://gitlab.com/eternal-twin) ».
And it is legally authorized by Motion Twin ([here](http://twd.io/e/3j-m0M/2) & [here](http://twd.io/e/JF3i0M/387)).

what / how =>
 - swf decompiling & extracting with [JPEXS](https://github.com/jindrapetrik/jpexs-decompiler)
 - swf [deobfuscating](http://tech.motion-twin.com/obfu.html)
 - network analysis / survey whit [BurpSuite Community](https://portswigger.net/burp)
 - decoding of data exchange flows ([CodeC Custom Algorithme](https://github.com/Angelisium/Scripts/blob/main/javascript/CodecController.js), motion twin use a server generate key and for the version they use `"1"`. + [HaxeSerializer](https://github.com/Angelisium/Scripts/blob/main/javascript/HaxeSerializer.js) (being rewritten) + [HaxeUnserializer](https://github.com/Angelisium/Scripts/blob/main/javascript/HaxeUnserializer.js))
 - ...

where => In « [Eternal Twin](https://gitlab.com/eternal-twin) » project.
