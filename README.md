# The manager mobile game
#### Video Demo:    https://youtu.be/LzGILA0zHoo?si=ayBnLwFWp-M8IPvj

#### Description:

At first, I wasn't sure about what to do, first I thought of making a web application for a Real-State business, then I thought of programming some devices and learning about Arduino, and finally a game. I decided to go with the game since I always wanted to do something like this as a child. Then, it was difficult what kind of game, and so many good options started to pop up, when asking friends for ideas one told me to make a dating app for skaters, And that way roll skaters was born, and the pet section was made in that way because I wanted to recreate an old Facebook game that was a hotel where you could improve it by playing minigames and taking care of it, that's why the game is called the manager, for now you can only have pets but in the future, I plan to improve it.

The project is a multiplatform game, delivered as a mobile game, but actually a multiplatform game, since it has the capability to be played on almost any device thanks to the [Godot engine](https://godotengine.org). Godot uses GDScript 4, a programming language designed for easy translation into other programming languages, allowing the game to be accessible across multiple platforms.

To archive this, I learned to use the engine through tutorials and [Godot's documentation](https://docs.godotengine.org/en/stable/). Coding in GDscript feels like a mix of C++ and Python, where variables must be defined before they can be used and conditionals and loops look more similar to Python's.

The project includes 4 folders: AppIcons, assets, scenes and scripts. The AppIcons and assets folder contain all the images used in the game, The scenes folder consist of .tscn files, which are used by Godot to visually represent the elements placed on the screen while also providing numerous features like image scaling and setting properties like some physics for the game, Finalle the most important folder would be scripts, it contains all the logic of the game, the folder has a set of .gd files that usually are liked through the engine to the tscn files.

*Globals.gd* is a file that can be read from any script, it is handy to save variables that are going to be used in many scenes. In this file I've created the functions that allow us to save the game data in JSON format, creating a db.json file in the user's device.

*rollskate_game.gd* Is one of the principal two mini games of the application, I learned GDscript and how to use the whole engine while making this game, It has a lot of features that are made by me like the posibility of selecting a character boy or girl, the object spawning mechanic is different, adding coins and saving them and how the game ends.
After wondering for many weeks what to do, I decided to choose a project that would allowe me to do a lot of things, in the future multiple mini games can be added.

*cowboy_game.gd* Was made with my previously acquired knowledge and all that I have learned in CS50, here you need to rescue the scaping cows.!
I decided to code this game after here "I should have been a cowboy" I had the clear picture of a game in which you could be a cowboy and capture your cattle. Prior to this script is *cow_dificultu_menu.gd* which contains the difficulty buttons, these buttons change the variable COWS in the file *Globals.gd* if you choose a more difficult game the *cowboy_game.gd* script will spawn more cows though a for loop, adding them to an array. The coins are assigned to you at the end of the mini-game, you'll get 5 coins for every cow, so here the script calls read() and save() from Globals to save in a json file the information and keep your progress after closing the game.

*character_menu.gd* and *store.gd* Allows the user to buy pets with the coins they earn by playing the other minigames, I designed the read function in a way that you can pass a key to find a value, for instance if you want to get a coin you need to call the global file where the function lives and then specify the key like `Globals.read().coin` for pets it would be `Globals.read().pet`. When you access the store the first time the program will create a db.json file to store 0 values for coins and pets, you can have from 0 to 5 in pets each number represents a pet, for instance the number 1 is the rubber duck, this way if the number 1 is found the rubber duck will be displayed as your pet. In the future I would like to add the possibility of buying a house and many other feautures.And finally the other gd files are mainly to handle buttons, redirect the user.

In the references you can find the free sources from which I got some audio and pictures, the rest was made by me with Microsoft pain.

I hope you like my project, it took me a lot of time and effort and I'm really happy with my new acquired coding skills. If you want to have some fun I invite you to play it in your browser here:

Game : https://danielmateus102.itch.io/cs50-final-projecy-the-manager

With gratitude, Daniel Mateus.

### References:


1. Pictures and animations:

    - https://www.freepik.es/vector-gratis/lindo-hamster-sosteniendo-ilustracion-dibujos-animados-mejilla_13037994.htm#fromView=author&page=3&position=15&uuid=8be874c3-fe5c-4492-a60f-a2b8caa9d611

    - https://www.freepik.es/vector-gratis/lindo-gato-fresco-gafas-dibujos-animados-vector-icono-ilustracion-animal-naturaleza-icono-concepto-aislado_23104955.htm

    - https://www.freepik.es/vector-gratis/ilustracion-vector-dibujos-animados-lindo-bulldog-comiendo-pastel-vector-aislado-concepto-comida-animal-estilo-dibujos-animados-plana_10336074.htm#fromView=search&page=1&position=51&uuid=edb6c429-5577-45fb-882a-bf4a9bd3aa4b

    - https://mitadmissions.org/blogs/entry/beaver-nation/

    - https://www.freepik.com/free-vector/supermarket-aisle-perspective-view_39845266.htm#from_view=detail_alsolike

    - https://kenney.nl/assets/onscreen-controls

    - https://grayger26.itch.io/wild-west-pixel-cowboy-pixel-art-asset-pack

    - https://www.reddit.com/r/PixelArt/comments/zbc2jx/dairy_cattle_animation/

    - https://smallmak.itch.io/topdown-fence-posts

    - https://www.reddit.com/r/PixelArt/comments/18t52md/drew_some_grass/

    - https://www.flaticon.com/free-icon/cowboy-hat_9753952?term=cowboy+hat&page=1&position=8&origin=tag&related_id=9753952

    - https://tenor.com/es/view/cs50-ddb-ddb-50-rubber-ducky-rubber-duck-gif-12464307856349287611

    - https://www.flaticon.es/icono-gratis/tronco_7833799?term=tronco&page=1&position=13&origin=search&related_id=7833799

    - https://www.flaticon.es/icono-gratis/tronco_7833799?term=tronco&page=1&position=13&origin=search&related_id=7833799

    - https://free-game-assets.itch.io/free-city-backgrounds-pixel-art

    - https://free-game-assets.itch.io/free-summer-pixel-art-backgrounds

    - https://muchopixels.itch.io/character-animation-asset-pack

2. sound:

    - https://pixabay.com/sound-effects/search/jump/

    - https://pixabay.com/sound-effects/search/quack/

3. Tutorials:

    - https://www.youtube.com/@Gwizz1027

    - https://www.youtube.com/@JumboGamedev

    - https://www.youtube.com/watch?v=nKBhz6oJYsc&ab_channel=CodingWithRuss

4. Documentation:

    - https://docs.godotengine.org/en/stable/
