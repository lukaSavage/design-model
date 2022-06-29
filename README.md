# 第1章：软件生命周期与模型

## 一、软件生命周期

### 1.1 可行性分析报告和软件开发计划

- 产出可行性分析报告

### 1.2 需求分析阶段

- 由软件分析师来做，需要懂技术也需要懂业务
- 分析出软件需要完成什么功能
- 产出需求分析说明书和初步的用户手册

### 1.3 软件设计(概要设计和详细设计)

- 由架构师/项目经理来做
- 根据团队技术基础确定用什么技术栈(Java/Node/Php)
- 确定部署的操作系统
- 使用什么数据库(oracle/mysql/sqlserver)
- 设计数据库表
- 选择团队成员
- 产出软件设计文档

### 1.4 编码工作

- 开发人员来做
- 把设计编成代码
- 产出源代码以及清单

### 1.5 测试阶段

- 由测试工程师进行
- 分为白盒测试(单元测试)和黑盒测试(功能测试)
- 产出软件测试报告

### 1.6 实施和维护工作

- 由实施工程师执行
- 把项目按照需要安装和配置好，让客户使用并解决简单问题
- 产出软件维护报告

## 二、软件开发模型 

### 2.1瀑布模型

- 瀑布模型（Waterfall Model） 是一个项目开发架构
- 开发过程是通过设计一系列阶段顺序展开的，从系统需求分析开始直到产品发布和维护，每个阶段都会产生循环反馈
- 如果有信息未被覆盖或者发现了问题，那么最好 “返回”上一个阶段并进行适当的修改，项目开发进程从一个阶段“流动”到下一个阶段，这也是瀑布模型名称的由来。

![瀑布模型](img/01.jpg)

### 2.2 增量开发模型

- 增量模型是把待开发的软件系统模块化，将每个模块作为一个增量组件，从而分批次地分析、设计、编码和测试这些增量组件。

  ![增量开发模型](img/02.jpg)

### 2.3 原型开发模型

原型模型指的是在执行实际软件的开发之前，应当建立系统的一个工作原型。

![原型开发](img/03.jpg)

## 三、模型

### 3.1 模型与UML的介绍

> 建造一栋大楼前需要先把图纸将外观、内部结构描述清楚，这些图纸就是模型。
>
> `Unified Modeling Language (UML)`又称统一建模语言或标准建模语言

### 3.2 模型的特点

- 简化
- 多视角
- 通用符号

### 3.3 UML组成

![UML组成](img/04.jpg)

### 3.4 UML开发软件

[staruml](http://staruml.io/)

## 四、视图

### 4.1 用例视图

> 从<font color="#f00">3.3节UML</font>可知，用例视图即由<font color="#08e">`用例图`</font>组成

#### 4.1.1 用例图

- 用例建模最主要的功能是表达系统的功能性需求或行为

- 参互者： 参与者指的是与系统交互的角色，可以是人，也可以是事物或其它系统

- 用例是系统为参与者提供的功能。用例名称一般是一个带有动作性的词语

- 如下图例↓↓↓

  ![用例图](img/05.jpg)

用例描述

| 项目       | 内容                                                         |
| :--------- | :----------------------------------------------------------- |
| 用例名称   | 登录                                                         |
| 用例ID     | login                                                        |
| 角色       | 用户                                                         |
| 用例说明   | 描述用户的登录过程                                           |
| 前置条件   | 打开网站页面                                                 |
| 基本事件流 | 1.点击登录 2. 输入用户名和秘密 3. 点击登录 4. 服务器会使用会话保存用户登录状态 |
| 其它事件流 | 1. 用户名为空提示用户名不能为空 2。密码为空提示密码不能为空  |
| 异常事件流 | 登录超时则返回登录页                                         |
| 后置条件   | 登录成功，进入个人中心                                       |

### 4.2 逻辑视图

逻辑视图包括<font color="#08e">`类图`</font>和<font color="#08e">`对象图`</font>组成

#### 4.2.1 类图

- 类图（Class Diagram）描述类的静态结构，定义类及描述类之间的联系，如关联、依赖、聚合等，还包括类的内部结构(类的属性和操作)

- 类图是一种静态模型类型,一个类图根据系统中的类以及各个类之间的关系描述系统的静态结构

- 类图包含7个元素：

  - 类(Class)
  - 接口(Interface)
  - 协作(Collaboration)
  - 依赖关系(Dependency)
  - 泛化关系(Generalization)
  - 关联关系(Association)
  - 实现关系(Realization)

- 在UML中,类用矩形来表示,分为3个部分: 名称部分(Name)、属性部分(Attribute)和操作部分(Operation)

- 类的表示方式

  | 类型     | 示例                                           |
  | :------- | :--------------------------------------------- |
  | 属性格式 | name : attribute type = default value          |
  | 操作格式 | name (parameter list) : type of value returned |

- 类图的几种关系

  > 关系可以从强到弱为 `依赖< 关联 <聚合 <组合`。
  >
  > 依赖是方法的参数，关联是属性。

  以下是类图关系图例↓↓

  ![类图关系示意图](img/06.jpg)

  - <font color="#f00">`依赖(Dependency)关系`</font>是类与类之间的联接。依赖关系表示一个类依赖于另一个类的定义。一般而言，依赖关系在Java语言中体现为局部变量、方法的形参，或者对静态方法的调用。(从使用以及生效范围来看，并不是单纯的定义，就算是定义为实例变量，但是使用上只在一个方法范围内使用，不在其他地方使用，也可以是依赖)

    >只要在类中用到了对方，那么它们之间就存在依赖关系，如果没有对方，连编译都通过不了
    >
    >![依赖关系](img/07.jpg)

  - <font color="#f00">`关联(Association关系`</font>是类与类之间的联接，它使一个类知道另一个类的属性和方法(实例变量体现)。关联可以是双向的，也可以是单向的。两个类之前是一个层次的，不存在部分跟整体之间的关系。

    >- 关联关系实际上就是类与类之间的联系，他是依赖关系的特例。
    >- 关联关系比依赖的关系更强
    >- 关联具有导航性，即双向关系或单向关系，表示关系在那一方维护
    >- 关联具有多重性，如
    >  - `1` 表示有且仅有一个
    >  - `0...` 表示0或者多个
    >  - `0,1` 表示0个或者一个
    >  - `n..m` 表示n到m个都可以
    >  - `m...` 表示至少m个
    >
    >![关联关系](img/08.jpg)

  - <font color="#f00">`聚合(Aggregation) 关系`</font> 是关联关系的一种，是强的关联关系。聚合是整体和个体之间的关系。例如，汽车类与引擎类、轮胎类，以及其它的零件类之间的关系便整体和个体的关系。与关联关系一样，聚合关系也是通过实例变量实现的。但是关联关系所涉及的两个类是处在同一层次上的，而在聚合关系中，两个类是处在不平等层次上的，一个代表整体，另一个代表部分。

    >- 聚合关系表示的是整体和部分的关系，整体与部分可以分开
    >- 聚合关系是关联关系的特例，所有它具有关联的导向性和多重性
    >- 聚合的双方生命周期是独立的
    >
    >![聚合关系](img/09.jpg)

  - <font color="#f00">`组合(Composition)关系`</font>是关联关系的一种，是比聚合关系强的关系。它要求普通的聚合关系中代表整体的对象负责代表部分对象的生命周期，组合关系是不能共享的。代表整体的对象需要负责保持部分对象和存活，在一些情况下将负责代表部分的对象湮灭掉。代表整体的对象可以将代表部分的对象传递给另一个对象，由后者负责此对象的生命周期。换言之，代表部分的对象在每一个时刻只能与一个对象发生组合关系，由后者排他地负责生命周期。部分和整体的生命周期一样

    > - 也是整体和部分的关系，但是整理和部分不可分开
    > - 整体和部分生命周期一致
    >
    > ![组合关系](img/10.jpg)

#### 4.2.2 对象图

- 对象图描述一组对象和它们之间的关系，它是系统状态的某一时刻的快照，它的使用相当有限，它主要用于了解系统在某个特定时刻的具体状况和数据结构
- 对象图表示方法和类图大致相同，对象图中的对象属性可以有具体值，类图中的一个类可以对应成对象图中的多个对象，例如： 部门类的自关联就可以对应成多个部门之间的关联

### 4.3 并发视图

> 并发视图包括<font color="#08e">`顺序图`</font>、<font color="#08e">`协作图`</font>、<font color="#08e">`状态图`</font>、<font color="#08e">`活动图`</font>、<font color="#08e">`组件图`</font>、<font color="#08e">`配置图`</font>组成。

#### 4.3.1 顺序图（时序图）

- 时序图强调消息时间顺序的交互图
- 时序图描述类系统中类与类之间的交互，它讲这些交互建模换成消息交换
- 时序图用于描述对象之间如何随着时间进行协作
- 时序图由活动者(Actor)、对象(Object)、消息(Message)、生命线(Lifeline)和控制焦点(Focus Of Control)组成
- 不同元素有不同表示
  - 对象是一个矩形，对象名称下有下划线
  - 消息用由方向的箭头表示，调用是实线，返回消息是虚线
  - 生命线由纵向的虚线表示
  - 控制焦点是纵向的矩形，也就是活动条(Activiation Bar)

![](img/11.png)

#### 4.3.2 协作图

- 协作图是时序图的一种变种
- 协作图强调的是发送和接受消息的对象之间的组织结构
- 协作图显示了一系列对象和在这些对象之间的联系以及对象间发送和接受的消息
- 时序图主要侧重与对象间消息传递在时间上的先后关系，而协作图则侧重与对象间以及对象和角色交互的静态关系

![](img/12.png)

#### 4.3.3 状态图

略~

#### 4.3.4 活动图

- 在UML里，活动图本质上就是流程图，
- 它描述系统的活动，判断系统的活动，判断点和分支等。

![](img/13.png)

#### 4.3.5 组件图

- 组件图用例建立系统的各个组件之间的关系，它们是通过软件或者文件组织在一起，使用组件图可以帮助读者了解某个功能位于软件包中的哪一个位置，以及各个版本的软件包含那些功能。
- 组件图可以用来帮助设计系统的整体架构

![](img/14.png)

#### 4.3.6 配置图（部署图）

- 部署图是来帮助读者了解软件中的各个组件运行硬件什么位置，以及这些硬件之间的交互关系
- 节点： 用来表示一种硬件，它可以是服务器，计算机等。节点的符号是一个三位盒子，在左上角包含节点的名称
- 通信关联： 节点通过通信关联建立彼此的关系，采用从节点到节点绘制实线来表示关联

![](img/15.png)

# 第2章：设计模式

## 一、面向对象

> <font color="#f00">以类和对象作为组织代码的基本单位，并实现封装、抽象、继承、多态四个特性</font>

面向对象的过程中往往会涉及到软件生命周期的三个阶段：分析、设计、编码

- 面向对象分析(OOA) Object Oriented Analysis
- 面向对象设计(OOD) Object Oriented Design
- 面向对象编程(OOP)Object Oriented Programming

### 1.1 封装

- 把数据封装起来
- 减少耦合，不该外部访问的不要让外部访问
- 利于数据的接口权限管理
- 仅暴露有限的必要接口，提高类的易用性
- 实现
  - public:公有修饰符，可以在类内或者类外使用public修饰的属性或者行为，默认修饰符
  - protected:受保护的修饰符，可以本类和子类中使用protected修饰的属性和行为
  - private : 私有修饰符，只可以在类内使用private修饰的属性和行为

```typescript
class Animal {
    public name: string;
    protected age: number;
    private weight: number;
    constructor(name: string, age: number, weight: number) {
        this.name = name;
        this.age = age;
        this.weight = weight;
    }
}
class Person extends Animal {
    private money: number;
    constructor(name: string, age: number, weight: number, money: number) {
        super(name, age, weight);
        this.money = money;
    }
    getName() {
        console.log(this.name);
    }
    getAge() {
        console.log(this.age);
    }
    getWeight() {
        console.log(this.weight);
    }
    getMoney() {
        console.log(this.money);
    }
}
let p = new Person('zfpx', 9, 100, 100);
console.log(p.name);
console.log(p.age);
console.log(p.weight);
```

### 1.2 抽象

- 抽象主要是隐藏方法的实现，让调用者只关心有哪些功能而不是关心功能的实现
- 抽象可以提高代码的可扩展性和维护性，修改实现不需要改变定义，可以减少代码的改动范围

```typescript
interface IStorage {
    save(key: any, value: any): void;
    read(key: any): void;
}
class LocalStorage implements IStorage {
    save(key: any, value: any) {
        localStorage.setItem(key, value);
    }
    read(key: any) {
        return localStorage.getItem(key);
    }
}
class User {
    constructor(public name: string, public storage: IStorage) {

    }
    save() {
        this.storage.save('userInfo', JSON.stringify(this));
    }
    read() {
        return this.storage.read('userInfo');
    }
}
let user = new User('张三', new LocalStorage());
user.save();
user.read();
```

### 1.3 继承

- 继承主要的要处是实现代码复用
- 继承可以把父类和子类的公共方法抽离出来，提高复用，减少冗余
- 是一种 `is-a` 关系

```typescript
export { };
class Animal {
    name: string;
    constructor(name: string) {
        this.name = name;
    }
    eat() {
        console.log(`${this.name} eat`)
    }
}
let animal = new Animal('动物');
animal.eat();

class Dog extends Animal {
    age: number;
    constructor(name: string, age: number) {
        super(name);
        this.age = age;
    }
    speak() {
        console.log(`${this.name} is barking!`);
    }
}
let dog = new Dog('🐶', 5);
dog.eat();
dog.speak();
```

### 1.4 多态

- 多态是指，子类可以替换父类
- 保持子类的开放性和灵活性，可以重写父类中的方法
- 实现面向接口编程

```typescript
class Animal {
    public name: string;
    protected age: number;
    private weight: number;
    constructor(name: string, age: number, weight: number) {
        this.name = name;
        this.age = age;
        this.weight = weight;
    }
    speak() {
        throw new Error('此方法必须由子类实现!');
    }
}
class Person extends Animal {
    private money: number;
    constructor(name: string, age: number, weight: number, money: number) {
        super(name, age, weight);
        this.money = money;
    }
    getName() {
        console.log(this.name);
    }
    getAge() {
        console.log(this.age);
    }
    getMoney() {
        console.log(this.money);
    }
    speak() {
        console.log('你好!');
    }

}
class Dog extends Animal {
    constructor(name: string, age: number, weight: number) {
        super(name, age, weight);
    }
    speak() {
        console.log('汪汪汪!');
    }
}
let p = new Person('zfpx', 10, 10, 10);
p.speak();
let d = new Dog('zfpx', 10, 10);
d.speak();
```

## 二、设计原则

### 2.1 什么是设计？

- 按哪一种思路或者标准来实现功能
- 功能相同，可以有不同设计的方式
- 需求如果不断变化，设计的作用才能体现出来

### 2.2 SOLID五大设计原则

| 首字母 | 指代         | 概念                                                         |
| :----- | :----------- | :----------------------------------------------------------- |
| S      | 单一职责原则 | 单一功能原则认为对象应该仅具有一种`单一功能`的概念           |
| O      | 开放封闭原则 | 开闭原则认为`软件体应该是对于扩展开放的，但是对于修改封闭的`的概念 |
| L      | 里氏替换原则 | 里氏替换原则认为程序中的对象应该是可以在不改变程序正确性的前提下`被它的子类所替换`的的概念 |
| I      | 接口隔离原则 | 接口隔离原则认为`多个特定客户端接口要好于一个宽泛用途的接口`的概念 |
| D      | 依赖反转原则 | 依赖反转原则认为一个方法应该遵从`依赖于抽象而不是一个实例`的概念,依赖注入是该原则的一种实现方式。 |

#### 2.2.1 O 开放封闭原则

- `Open Closed Principle`
- 对扩展开放，对修改关闭
- 增加需求时，扩展新代码，而非修改已有代码
- 开闭原则是设计模式中的总原则
- 对近期可能会变化并且如果有变化但改动量巨大的地方要增加扩展点,扩展点过多会降低可读性

```js
class Customer {
    constructor(public rank: string) { }
}
class Product {
    constructor(public name: string, public price: number) {

    }
    cost(customer: Customer) {
        switch (customer.rank) {
            case 'member':
                return this.price * .8;
            case 'vip':
                return this.price * .6;
            default:
                return this.price;
        }
    }
}
let p1 = new Product('笔记本电脑', 1000);
let member = new Customer('member');
let vip = new Customer('vip');
let guest = new Customer('guest');
console.log(p1.cost(member));
console.log(p1.cost(vip));
console.log(p1.cost(guest));
class Customer {
+    constructor(public rank: string, public discount: number = 1) { }
+    getDiscount() {
+        return this.discount;
+    }
}
class Product {
    constructor(public name: string, public price: number) {

    }
    cost(customer: Customer) {
-        /*  switch (customer.rank) {
-             case 'member':
-                 return this.price * .8;
-             case 'vip':
-                 return this.price * .6;
-             default:
-                 return this.price;
-         } */
+        return this.price * customer.getDiscount();
    }
}
+let p1 = new Product('笔记本电脑', 1000);
+let member = new Customer('member', .8);
+let vip = new Customer('vip', .6);
let guest = new Customer('guest');
console.log(p1.cost(member));
console.log(p1.cost(vip));
console.log(p1.cost(guest));
import axios, { AxiosInstance, AxiosRequestConfig } from 'axios';
let instance: AxiosInstance = axios.create();
instance.interceptors.request.use((config: AxiosRequestConfig) => {
    config.url = 'http://localhost:8080' + config.url;
    return config;
});

instance.interceptors.response.use(response => {
    if (response.status !== 200 || response.data.code != 0) {
        return Promise.reject(response);
    } else {
        return response.data.data;
    }
})
/**
 * {code:0,data:{id:1,name:'zhufeng'}}
 */
instance({
    url: '/api/users'
}).then(result => {
    console.log(result);
}, error => {
    console.error(error);
});
```

#### 2.2.2 S 单一职责原则

- Single responsibility principle
- 一个类或者模块只负责完成一个职责,如果功能特别复杂就进行拆分
- 单一职责可以降低类的复杂性，提高代码可读性、可维护性
- 当类代码行数过多、方法过多、功能太多、职责太杂的时候就要对类进行拆分了
- 拆分不能过度，如果拆分过度会损失内聚性和维护性
- [lodashjs](https://www.lodashjs.com/docs/latest)
- [jquery](https://api.jquery.com/)

![单一职责原则](img/16.png)

```diff
class Product {
    public name: string;
-    public categoryName: string;
-    public categoryIcon: string;
+     public category:Category;
}
+class Category {
+    public name: string;
+    public icon: string;
+}
```

#### 2.2.3 L 里氏替换原则

- Liskov Substitution Principle
- 所有引用基类的地方必须能透明地使用其子类的对象
- 子类能替换掉父类，使用者可能根本就不需要知道是父类还是子类,反之则不行
- 里氏替换原则是开闭原则的实现基础,程序设计的时候尽量使用基类定义及引用，运行时再决定使用哪个子类
- 里氏替换原则可以提高代码的复用性，提高代码的可扩展性，也增加了耦合性
- 相对于多态，这个原则是讲的是类如何设计，子类如果违反了父类的功能则表示违反了里氏替换原则

![里氏替换原则](img/17.png)

```js
abstract class AbstractDrink {
    abstract getName(): string;
}
class CocaCola extends AbstractDrink {
    getName(): string {
        return '可乐';
    }
}
class Sprite extends AbstractDrink {
    getName(): string {
        return '雪碧';
    }
}
class Fanta extends AbstractDrink {
    getName(): string {
        return '芬达';
    }
}
class Customer {
    drink(drink: AbstractDrink) {
        console.log('喝' + drink.getName());
    }
}
let customer = new Customer();
let cocaCola = new CocaCola();
let sprite = new Sprite();
let fanta = new Fanta();
customer.drink(cocaCola);
customer.drink(sprite);
customer.drink(fanta);
import React from 'react';
import ReactDOM from 'react-dom';
class App extends React.Component {
    render() {
        return (
            <div>App </div>
        )
    }
}
let element = React.createElement(App);
ReactDOM.render(element, document.getElementById('root'));
abstract class AbstractDrink {
    abstract getName(): any;
}
class CocaCola extends AbstractDrink {
    getName(): any {
        return 100;
    }
}
```

#### 2.2.4 D 依赖倒置原则

- Dependence Inversion Principle
- 面向接口编程，依赖于抽象而不依赖于具体实现
- 要求我们在程序代码中传递参数时或在关联关系中，尽量引用层次高的抽象层类
- 使用方只关注接口而不关注具体类的实现

![依赖倒置原则](img/18.png)

```js
abstract class GirlFriend {
    public age: number;
    public height: number;
    public abstract cook(): void;
}
class LinZhiLing extends GirlFriend {
    public cook(): void {

    }
}
class HanMeiMei extends GirlFriend {
    public cook(): void {

    }
}
class SingleDog {
    constructor(public girlFriend: GirlFriend) {

    }
}
let s1 = new SingleDog(new LinZhiLing());
let s2 = new SingleDog(new HanMeiMei());
import { createStore } from 'redux';
let store = createStore(state => state);
export interface Action<T = any> {
    type: T
}
export interface AnyAction extends Action {
    // Allows any extra properties to be defined in an action.
    [extraProps: string]: any
}
let action: AnyAction = { type: 'increment', payload: 5 }
store.dispatch(action);
```

#### 2.2.5 I 接口隔离原则

- Interface Segregation Principle
- 保持接口的单一独立，避免出现胖接口
- 客户端不应该依赖它不需要的接口，类间的依赖关系应该建立在最小的接口上
- 接口尽量细化，而且接口中的方法尽量的少
- 类似于单一职责原则，更关注接口

```js
interface IUserManager {
    updateUserInfo(): void;
    updatePassword(): void;
}
interface IProductManager {
    updateProduct(): void;
    updatePrice(): void;
}
```

![接口隔离原则](img/19.jpg)

```js
interface Running {
    run(): void;
}
interface Flying {
    fly(): void;
}
interface Swimming {
    swim(): void;
}
class Automobile implements Running, Flying, Swimming {
    run() { }
    fly() { }
    swim() { }
}
```

### 2.3 迪米特法则

- Law of Demeter，LOD
- 有时候也叫做最少知识原则
- 一个软件实体应当尽可能少地与其它实体发生相互作用
- 迪米特法则的初衷在于降低类之间的耦合
- 类定义时尽量要实现内聚,少使用`public`修饰符，尽量使用`private`、`protected` 等

![迪米特法则](img/20.png)

```js
class Salesman {
    constructor(public name: string) {

    }
    sale() {
        console.log(this.name + ' 销售中....');
    }
}
class SaleManager {
    private salesmen: Array<Salesman> = [new Salesman('张三'), new Salesman('李四')];
    sale() {
        this.salesmen.forEach(salesman => salesman.sale());
    }
}
class CEO {
    private saleManager: SaleManager = new SaleManager();
    sale() {
        this.saleManager.sale();
    }
}
let ceo = new CEO();
ceo.sale();
```

### 2.4 合成复用原则

#### 2.4.1 类的关系

- 类之间有三种基本关系，分别是关联(聚合和组合)、泛化和依赖

- 如果一个类单向依赖另一个类,那么它们之间就是单向关联。如果彼此依赖,则为相互依赖,即双向关联

- 关联关系包括两种特例：聚合和组合

  - 聚合，用来表示整体与部分的关系或者`拥有`关系,代表部分的对象可能会被整体拥有，但并不定定会随着整体的消亡而销毁,比如班级和学生

  - 合成或者说组合要比聚合关系强的多，部分和整体的生命周期是一致的,比如人和器官之间

    ![](img/21.png)

#### 2.4.2 合成复用原则

- 合成复用原则是通过将已有的对象纳入新对象中，作为新对象的成员对象来实现的
- 新对象可以调用已有对象的功能，从而达到复用
- 原则是尽量首先使用组合/聚合的方式，而不是使用继承
- 专业人做专业事

```js
class Cooker {
    cook() {

    }
}
class Person {
    private cooker: Cooker = new Cooker();
    cook() {
        this.cooker.cook();
    }
}
```

### 2.5 总结

- 开闭原则是核心，对修改关闭对扩展开放是软件设计的基石
- 单一职责要求我们设计接口和模块功能的时候尽量保证单一性和原子性，修改一条不影响全局和其它模块
- 里氏替换原则和依赖倒置原则要求面向接口和抽象编程,不要依赖具体实现，否则实现一改，上层调用者就要对应修改

### 2.6 如何写出好代码?

- 可维护性 BUG是否好改?
- 可读性 是否容易看懂?
- 可扩展性 是否可以添加新功能?
- 灵活性 添加新功能是否容易?老方法和接口是否容易复用?
- 简洁性 代码是否简单清晰?
- 可复用性 相同的代码不要写2遍?
- 可测试性 是否方便写单元测试和集成测试?