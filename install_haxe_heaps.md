

# installation de haxe et heaps

## Haxe

```bash
sudo add-apt-repository ppa:haxe/releases -y
sudo apt-get update
sudo apt-get install haxe -y
mkdir ~/haxelib && haxelib setup ~/haxelib
```

## Heaps

```bash
haxelib install heaps
```

## HashLink

### Installation des binaires

https://github.com/HaxeFoundation/hashlink

Dépendances :

~~~bash
sudo apt-get install libpng-dev libturbojpeg-dev libvorbis-dev libopenal-dev libsdl2-dev libmbedtls-dev libuv1-dev build-essential
~~~

Compilation

~~~bash
cd /tmp
git clone https://github.com/HaxeFoundation/hashlink.git
cd hashlink
make
sudo make install
## rajouter le chemin des lirairies hashlink
sudo ldconfig /usr/local/lib
~~~



### Installation pour haxe

https://haxe.org/manual/target-hl-getting-started.html

```bash
haxelib git hashlink https://github.com/HaxeFoundation/hashlink.git master other/haxelib/
```

#### Hello World

To get started with Haxe/HashLink, create a new folder and save this class as `Main.hx`.

```
/**
    Multi-line comments for documentation.
**/
class Main {
    static public function main():Void {
        // Single line comment
        trace("Hello World");
    }
}
```

To compile, either run the following from the command line:

```
haxe --hl hello.hl --main Main
```

Another possibility is to create and run (double-click) a file called `compile.hxml`. In this example the hxml file should be in the same directory as the example class.

```
--hl hello.hl
--main Main
```

The compiler outputs a file called `hello.hl` in the current folder, which can be executed with `hl hello.hl` from the command line.

