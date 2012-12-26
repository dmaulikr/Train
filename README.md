Train
=====

a simple dependency injection framework for objective c, written while traveling in a train!

## Usage
1. Add an Ivar to your Class file with the IOC prefix _ioc_ and the service you want to inject:
2. Use the service in your class.

```objectivec
    // .m
    @interface MyClass () {
        MyService* _ioc_MyService;
    }
    
    @implementation MyClass
    
    -(NSString*) foo {
        return [_ioc_MyService goo];
    }
    
    @end
```

3. When an instance of MyClass is needed, initialize it with:

```objectivec
    MyClass* myClass = [ObjectInstancializationService instantialize:[Myclass class]];
```

### It is recursive!

MyClass will be initialized with the default constractor [MyClass alloc] init]. Every Ivar in it with the IOC prefix will be initialized recursively!

### IOC prefix

The IOC prefix can be set in IOCDefines.h

### Sample project

Check it out!

Thats it, You are ready to go.