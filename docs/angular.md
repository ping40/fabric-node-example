https://stackblitz.com/edit/angular-bmtjzs-test-eccgngpingping?file=src/app/product-details/product-details.component.html

--------------
npm config set http-proxy http://127.0.0.1:1081
npm config set https-proxy http://127.0.0.1:1081
--------------


$ ng build  --prod
An unhandled exception occurred: Could not find module "@angular-devkit/build-angular" from "/home/huangping/work/angular/example".
See "/tmp/ng-TEHYnV/angular-errors.log" for further details.

npm install --save-dev @angular-devkit/build-angular
---------------------
ng update @angular/cli @angular/core 升级当前项目的代码
---------------------
修改angular.json 中关于tsconfig.app.json位置的定义
---------------------
路由参数总会是字符串。 JavaScript 的 (+) 操作符会把字符串转换成数字，英雄的 id 就是数字类型。
---------------------
$ 是一个命名惯例，用来表明 heroes$ 是一个 Observable，而不是数组。
--------------------
<li *ngFor="let hero of heroes$ | async" >
$ 是一个命名惯例，用来表明 heroes$ 是一个 Observable，而不是数组。

*ngFor 不能直接使用 Observable。 不过，它后面还有一个管道字符（|），后面紧跟着一个 async，它表示 Angular 的 AsyncPipe。

AsyncPipe 会自动订阅到 Observable，这样你就不用再在组件类中订阅了。


---------------------
1： 组件依赖服务:
方式1：  providers:  [ HeroService ]  https://www.angular.cn/guide/architecture-components
方式2：  使用依赖注入（  做练习的时候，是用这个方法， 但是 docs  里面描述是个上面的方法）
---------------------
数据绑定：

<li>{{hero.name}}</li>
<app-hero-detail [hero]="selectedHero"></app-hero-detail>
<li (click)="selectHero(hero)"></li>

1：  dom <---- component
{{hero.name}}插值表达式在 <li> 标签中显示组件的 hero.name 属性的值。

2：  dom <---- component
[hero]属性绑定把父组件 HeroListComponent 的 selectedHero 的值传到子组件 HeroDetailComponent 的 hero 属性中。

3：  dom ----> component
当用户点击某个英雄的名字时，(click) 事件绑定会调用组件的 selectHero 方法。

4: 双向数据绑定（主要用于模板驱动表单中），它会把属性绑定和事件绑定组合成一种单独的写法。下面这个来自 HeroDetailComponent 模板中的例子通过 ngModel 指令使用了双向数据绑定：

src/app/hero-detail.component.html (ngModel)
content_copy
<input [(ngModel)]="hero.name">
在双向绑定中，数据属性值通过属性绑定从组件流到输入框。用户的修改通过事件绑定流回组件，把属性值设置为最新的值。
---------------------
https://www.angular.cn/guide/template-syntax

---------------------
<input [(ngModel)]="name">
要使用这个：必须在app.module.ts增加：

import { FormsModule } from '@angular/forms';
且在 imports 增加： FormsModule

存在问题： 双向绑定是针对这个变量， 不是针对这个应用。

---------------------
样式模块化特性是通过 style 里面的[]属性选择器来实现，比如：

<h1 _ngcontent-hts-c0="">Tour of Heroes</h1>
h1[_ngcontent-hts-c0] {
    font-weight: normal;
}
---------------------
服务单例： 为什么 items.component.ts删除不掉，从业务上。我已经确定它是没有用了。

---------------------
子注入器的创建：
每当 Angular 创建一个在 @Component() 中指定了 providers 的组件实例时，它也会为该实例创建一个新的子注入器。 
类似的，当在运行期间加载一个新的 NgModule 时，Angular 也可以为它创建一个拥有自己的提供商的注入器

当 Angular 销毁 NgModule 或组件实例时，也会销毁这些注入器以及注入器中的那些服务实例。

---------------------
---------------------
---------------------
---------------------
https://www.angular.cn/guide/file-structure
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------
---------------------

