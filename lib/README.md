# ng2-cache

> ng2-cache library compatible with AoT compilation &amp; Tree shaking like an official package.

This lib allows you to use ng2-cache library for **Angular v19+** apps written in _TypeScript_, _ES6_ or _ES5_. 


## How to use

1. `npm install @pscoped/ng2-cache --save`
2. Import it in your main app module
    ```
    @NgModule({
    declarations: [
        ....
    ],
    imports: [
        ....
        Ng2CacheModule
    ],
    providers: [],
    bootstrap: [AppComponent]
    })
    export class AppModule { }
    ```

3. Use it inside your `Component` by DI

    ````
    ...
    import { CacheService, CacheStoragesEnum } from 'ng2-cache';
    ...

    export class AppComponent {
    
    constructor(private _cacheService: CacheService) { 
        this._cacheService.set('key', ['some data']);

        const cachedData = this._cacheService.get('key');
    } 
    ````
That's it.


## To contribute

- Git Repo: https://github.com/paritosh64ce/ng2-cache/tree/ng19

### Run tasks

To create a production bundle:

```sh
npm run build
```


## License

MIT
