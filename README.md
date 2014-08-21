Amonitor
========
const injector : Injector = new Injector;

//create a basic mapping:
injector.map(Sprite); //will instantiate a new Sprite for each request for Sprite

//map to another class:
injector.map(Sprite).toType(BetterSprite); //will instantiate a new BetterSprite for each request for Sprite

//map as a singleton:
injector.map(EventDispatcher).asSingleton(); //will lazily create an instance and return it for each consecutive request

//map an interface to a singleton:
injector.map(IEventDispatcher).toSingleton(EventDispatcher);
