# 设计模式
## 单例模式
#### 模式动机
对于系统中的某些类来说，只有一个实例很重要。
#### 模式定义
确保某一个类只有一个实例，而且自行实例化并向整个系统提供这个实例。
#### 模式要点
1. 某个类只能有一个实例；
2. 必须自行创建这个实例；
3. 必须自行向整个系统提供这个实例。
#### 模式优点
1. 提供了对唯一实例的受控访问；
2. 可以节约系统资源；
3. 允许可变数目的实例。
#### 模式缺点
1. 单例类的扩展性不好；
2. 单例类的职责过重。
#### 适用环境
1. 系统只需要一个实例对象；
2. 只允许使用一个公共访问点；
3. 单例也可根据需要改进成多例模式。
## 桥接模式
#### 模式动机
对于有两个变化维度的系统，桥接模式将继承关系转化成关联关系，从而降低了类与类之间的耦合，减少代码的编写量。
#### 模式定义
将抽象部分与它的实现部分分离，使它们都可以独立地变化。
#### 模式优点
1. 分离抽象接口及其实现部分；
2. 提高了系统的可扩展性；
3. 实现细节对客户透明。
#### 模式缺点
1. 增加了系统的理解和设计难度；
2. 使用范围具有一定的局限性。
#### 适用环境
1. 在构件的抽象化角色和具体化角色之间增加更多的灵活性，避免在两个层次之间建立静态的继承联系时；
2. 抽象化角色和实现化角色可以以继承的方式独立扩展而互不影响时；
3. 一个类中存在两个独立变化的维度时；
4. 不希望使用继承或因为多层次继承导致系统类的个数急剧增加时。
## 适配器模式
#### 模式动机
因为现有类中方法名与目标类中定义的方法名不一致等原因导致服务器提供的接口不是客户所期望的。
#### 模式定义
将一个接口转换成客户希望的另一个接口，使接口不兼容的类可以一起工作。
## 职责链模式
#### 模式动机
可以是一条直线、一个环或者一个树形结构，链上的每一个对象都是请求处理者；将请求的处理者组织成一条链，客户端只需将请求发送到链上即可，从而实现请求的发送者和处理者解耦。
#### 模式定义
避免请求发送者与接收者耦合在一起，让多个对象都有可能接收请求，将这些对象连接成一条链，并且沿着这条链传递请求，直到有对象处理它为止。
#### 模式优点
1. 降低耦合度；
2. 可简化对象的相互连接；
3. 增强给对象指派职责的灵活性；
4. 增加新的请求处理类很方便。
#### 模式缺点
1. 不能保证请求一定被接收；
2. 系统性能会受到一定的影响。
#### 适用环境
1. 有多个对象可以处理同一个请求，具体哪个对象处理该请求由运行时刻自动确定；
2. 在不明确指定接收者的情况下，向多个对象中的一个提交一个请求；
3. 需要动态指定一组对象处理请求时。
## 中介者模式
#### 模式动机
根据“单一”原则，应该尽量将对象细化，使其只负责或呈现单一的职责；为了减少对象两两之间复杂的引用关系，使之成为一个松耦合的系统。
#### 模式定义
用一个中介对象来封装一系列的对象交互，中介者使各对象不需要显式地相互引用，从而使其耦合松散，而且可以独立地改变它们之间的交互。
#### 模式职责
1. 中转作用（结构性）；
2. 协调作用（行为性）。
#### 模式优点
1. 简化对象之间的交互；
2. 将各同事之间解耦；
3. 减少子类的生成；
4. 可简化各个同事类的设计与实现。
#### 模式缺点
1. 可能会导致中介类非常复杂，系统难以维护。
#### 适用环境
1. 系统对象间存在复杂的引用关系时；
2. 某个对象难以复用时；
3. 希望通过一个中间类来封装多个类中的行为，而又不希望生成太多的子类时。
## 观察者模式
#### 模式定义
意图是定义对象间的一种一对多的依赖关系，当一个对象的状态发生改变时，所有依赖于它的对象都得到通知并被自动更新；一个目标可以有任意数目的依赖它的观察者，一旦目标的状态发生改变，所有的观察者都得到通知，作为对这个通知的响应，每个观察者都将查询目标以使其状态与目标的状态同步。
#### 适用环境
1. 当一个抽象模型有两个方面，其中一个方面依赖于另一方面。将这二者封装在独立的对象中可以使他们各自独立地改变和复用；
2. 当对一个对象的改变需要同时改变其它对象，而不知道具体有多少对象有待改变；
3. 当一个对象必须通知其他对象，而它又不能确定其他对象是谁；
