---
page-title: "快速入门Spring第一天(共四天) - 知乎"
url: https://zhuanlan.zhihu.com/p/98967126
date: "2024-10-14 20:23:41"
---
**Spring第一天讲义**

## **1.** **说在前面**

什么样的架构，我们认为是一个优秀的架构？

判断准则：**可维护性好，可扩展性好**，性能。

**什么叫可扩展性好？**

答：在不断添加新的代码的同时，可以不修改原有代码，即符合[开闭原则](https://zhida.zhihu.com/search?content_id=110123719&content_type=Article&match_order=1&q=%E5%BC%80%E9%97%AD%E5%8E%9F%E5%88%99&zhida_source=entity)。

**如何让程序的可维护性好，可扩展性好呢？**

业界有一个公认的标准：[高内聚](https://zhida.zhihu.com/search?content_id=110123719&content_type=Article&match_order=1&q=%E9%AB%98%E5%86%85%E8%81%9A&zhida_source=entity)，低耦合。

**高内聚：**就是尽量将代码写在与之功能描述一致的模块中。如User表的操作写在UserDAO里面，不要写在非UserDAO的类里面。

**[低耦合](https://zhida.zhihu.com/search?content_id=110123719&content_type=Article&match_order=2&q=%E4%BD%8E%E8%80%A6%E5%90%88&zhida_source=entity)：**就是尽量减少类与类之间的**直接关系**。（重点）

直接关系：Controller层依赖Service层，在Controller层直接new Service层的类的对象。

Service层依赖Dao层，在Service层直接new Dao层的对象。

Spring框架就是通过**IoC/DI**（控制反转/依赖注入）实现程序的**解耦**。从而提高程序的维护性和扩展性。

## **2.** **Spring概述**

## **2.1.** **Spring是什么**

Spring是一个JavaEE轻量级的一站式开发框架。

**JavaEE：** 就是用于开发企业级（B/S）应用的技术。

**轻量级：**使用最少代码启动框架，然后根据需求选择需要使用的模块。

**重量级：**早期的EJB，开发一个HelloWorld程序都需要引入EJB的全部模块。

**一站式：**提供了表示层，服务层，[持久层](https://zhida.zhihu.com/search?content_id=110123719&content_type=Article&match_order=1&q=%E6%8C%81%E4%B9%85%E5%B1%82&zhida_source=entity)的所有支持。

## **2.2.** **Spring框架出现的背景**

世界上第一套由Java官方Sun公司推出的企业级开发框架EJB瞬间风靡全球，被各大公司所应用。

Spring之父，Rod Jonhson是一个音乐博士，在Sun公司的大力推广下，也成为EJB框架的使用者。

在深入研究完EJB框架（由Sun主导开发的一个JavaEE开发框架），无法接受这么一个框架被吹成世界第一，具体查看他吐槽EJB的书《Expert one on one J2EE design and development》。

其中突出被他吐槽最厉害的一个点就EJB的重量级，就是只要使用EJB里面任何一个组件。都要导入EJB所有的jar包。于是他就提供了一个解决方案：轻量级的一站式企业级开发框架。

**那么什么是轻量级呢？**

就是除内核模块，其他模块由开发者自由选择使用，同时支持整合其他框架。也可以称为可插拔式开发框架，像插头和插座一样，插上就用，不用就拔下来。这就是Spring框架核心理念。

**那么什么是一站式呢？**

就是Spring框架提供涵盖了JavaEE开发的表示层，服务层，持久层的所有组件功能。也就是说，原则上，学完一套Spring框架，不用其他框架就可以完成网站一条流程的开发。

如图：

![](https://pic2.zhimg.com/v2-26c7023026716aab52bb269fbd70f493_b.jpg)

## **2.3.** **Spring框架的作用**

根据以上章节的描述。Spring是一个JavaEE轻量级一站式开发框架。它提供的功能涵盖了JavaEE程序中的表示层，服务层，持久层功能组件。这意味着，单单Spring框架就可以满足整个JavaEE程序的开发。

但Spring框架，更加强调的是它的**轻量级**（模块的可插拔）。也就是说，除了内核模块，其他功能模块如果你想使用可以不用，并且Spring框架能够整合任何第三方的框架。在现实开发中，Spring主要**用于整合其他框架**。

## **2.4.** **总结**

1\. Spring是一个一站式的企业级（JavaEE）开发框架，意味着，仅仅使用一个Spring框架就可以满足JavaEE开发的表示层，服务层，持久层的开发。

2\. Spring强调的理念是：轻量级。意味着Spring提供的功能模块，除了内核模块以外，其他功能模块开发人员可以选择性使用。

3\. Spring框架在现实开发中，主要的功能是整合第三方框架。

## **2.5.** **Spring框架包**

Spring官方网站

[https://spring.io/](https://link.zhihu.com/?target=https%3A//spring.io/)

### **2.5.1.** **框架包的下载**

Spring官方提供的Maven方式的项目下载。

[https://start.spring.io/](https://link.zhihu.com/?target=https%3A//start.spring.io/)

但是基于简单入门的原则，我们要通过导入包的方式来学习。需要下载框架的zip包

路径为：[http://repo.springsource.org/libs-release-local/org/springframework/spring/](https://link.zhihu.com/?target=http%3A//repo.springsource.org/libs-release-local/org/springframework/spring/)

### **2.5.2.** **目录说明**

\--[根目录](https://zhida.zhihu.com/search?content_id=110123719&content_type=Article&match_order=1&q=%E6%A0%B9%E7%9B%AE%E5%BD%95&zhida_source=entity)

![](https://pic4.zhimg.com/v2-8d95557846ca585d88b98ff5618bd1e3_b.jpg)

\--类库规则

![](https://pic4.zhimg.com/v2-9fc8029b64eb5c263a1da61b3851bf81_b.png)

\--包说明

![](https://pic1.zhimg.com/v2-11c76ac179d15b350b13357621e71796_b.jpg)

## **3.** **入门示例（IDEA）**

Spring之所以可以实现模块的可插拔是支持依赖注入，所谓的依赖注入就是不用new就可以创建对象。

**需求：使用Spring框架不用new创建一个对象。**

## **3.1.** **配置[流程图](https://zhida.zhihu.com/search?content_id=110123719&content_type=Article&match_order=1&q=%E6%B5%81%E7%A8%8B%E5%9B%BE&zhida_source=entity)**

![](https://pic2.zhimg.com/v2-e19b7149af3c1dc153aa282b1860730f_b.jpg)

1\. 创建一个普通类。

2\. 创建一个Spring配置文件，用于描述类与类之间的关系。

3\. 创建ApplicationContext容器对象，根据Spring配置文件的描述，创建对象并放在Spring容器里面。

4\. 使用ApplicationContext容器对象的getBean方法，获取Spring容器里面的对象。

## **3.2.** **配置步骤说明**

1\. 导入包。

2\. 创建一个普通类。

3\. 创建一个Spring主配置文件（去官方文档上拷贝约束）。

4\. 编写一个测试类，使用ApplicationContext的子类对象根据配置文件创建Spring容器对象ApplicationContext。并且在容器里面获得创建的对象。

## **3.3.** **配置步骤**

### **3.3.1.** **第一步：搭建环境**

1.创建一个Java项目

![](https://pic2.zhimg.com/v2-4a611aaece405ba4604d4c9b16e1fe7f_b.jpg)

2.导包，String的基础支撑包和依赖的日志包复制到lib文件下，并且加入项目中。

\---导入Spring基础支撑包。

![](https://pic1.zhimg.com/v2-8502ced2efa0af4dc2bdc42f949cc072_b.jpg)

\--导入Spring依赖的日志包

![](https://pic4.zhimg.com/v2-49d2ce9bba9a1d76e4d693d63e1e87a9_b.png)

### **3.3.2.** **第二步：创建配置文件**

1\. 在项目的src下面创建配置文件applicationContext.xml，配置文件模块查看位置：spring框架/docs/spring-framework-reference/html/beans.html。

```
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
        http://www.springframework.org/schema/beans/spring-beans.xsd">

</beans>
```

### **3.3.3.** **第三步：创建对象到容器里面**

1\. 创建一个类

```
package org.cjw.service;

public class HelloWorldService {

    public void say() {
        System.out.println("--你好世界！--");
    }
}
```

2\. applicationContext.xml配置文件加入配置

```
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
        http://www.springframework.org/schema/beans/spring-beans.xsd">

    <!--
        <bean name="" class="" />标签：用于声明一个类，在启动Spring框架的时候根据该配置的类创建对象到spring容器里面去
           name属性：bean的唯一标识
           class属性：bean的全限定名，用于反射创建对象到spring容器里面去
    -->
    <bean id="helloWorldService" class="org.cjw.service.HelloWorldService" />
</beans>
```

3\. 测试使用getBean获得容器中的对象

```
package org.cjw.service.test;

import org.cjw.service.HelloWorldService;
import org.junit.Test;
import org.springframework.context.support.ClassPathXmlApplicationContext;

public class HelloWorldServiceTest {

    @Test
    public void testSay() {
        // 创建一个ApplicationContext对象，根据xml配置创建对象到spring容器里面去
        // 直接读取src目录下的配置文件的子类是ClassPathXmlApplicationContext
        ClassPathXmlApplicationContext context = new ClassPathXmlApplicationContext("applicationContext.xml");
        // 通过getBean方法获取spring容器里面的对象
        HelloWorldService helloWorldService = context.getBean(HelloWorldService.class);
        // 对象调用方法
        helloWorldService.say();
    }
}
```

4\. 测试结果

通过代码可以得出：Spring框架果然不用new就可以创建对象。

## **3.4.** **Spring容器的两个实现**

![](https://pic4.zhimg.com/v2-caa06751bb184824cea1d2ba5af2dd6b_b.jpg)

ClassPathXmlApplicationContext:通过[classpath路径](https://zhida.zhihu.com/search?content_id=110123719&content_type=Article&match_order=1&q=classpath%E8%B7%AF%E5%BE%84&zhida_source=entity)（相对路径）直接获得加载的xml文件（推荐使用）

FileSystemXmlApplicationContext：通过文件路径（绝对路径）来获得加载的xml文件。

```
@Test
public void testSay() {
    // 创建一个ApplicationContext对象，根据xml配置创建对象到spring容器里面去
    // 直接读取src目录下的配置文件的子类是ClassPathXmlApplicationContext
    // ClassPathXmlApplicationContext context = new ClassPathXmlApplicationContext("applicationContext.xml");
    FileSystemXmlApplicationContext context = new FileSystemXmlApplicationContext("C:\\Users\\JackMi\\IdeaProjects\\spring-demo-starat\\src\\applicationContext.xml");
    // 通过getBean方法获取spring容器里面的对象
    HelloWorldService helloWorldService = context.getBean(HelloWorldService.class);
    // 对象调用方法
    helloWorldService.say();
}
```

## **3.5.** **ApplicationContext类图结构图**

Spring框架容器对象的继承体系

![](https://pic3.zhimg.com/v2-70a8c85de5df1811c2dedf3eef4f9e36_b.jpg)

通过结构图可以看到，Spring使用了工厂[设计模式](https://zhida.zhihu.com/search?content_id=110123719&content_type=Article&match_order=1&q=%E8%AE%BE%E8%AE%A1%E6%A8%A1%E5%BC%8F&zhida_source=entity)，Spring容器顶级接口是BeanFactory，ApplicationContext是它的子接口。在开发中，使用ApplicationContext即可。

## **4.** **Spring的控制反转和依赖注入（重点-spring核心之一）**

**IoC：Inversion of Control（控制反转）:**

读作“反转控制”，更好理解，不是什么技术，而是一种设计思想，好比于MVC。就是将原本在程序中手动创建对象的控制权，交由[Spring框架](https://zhida.zhihu.com/search?content_id=110123719&content_type=Article&match_order=17&q=Spring%E6%A1%86%E6%9E%B6&zhida_source=entity)来管理。

**正控：若开发者需要使用某个对象，那么就必须通过new关键字来创建该对象。**

**反控：开发者只管从Spring容器中获取需要使用的对象，无需关心对象的创建过程，这也就是把对象的创建控制权反转给了Spring框架。**（Don’t call me ,I’ll call you）

**DI：Dependency Injection（依赖注入）**

从字面上分析：

IoC：指将对象的创建权，反转给了[Spring容器](https://zhida.zhihu.com/search?content_id=110123719&content_type=Article&match_order=7&q=Spring%E5%AE%B9%E5%99%A8&zhida_source=entity)；

DI：指Spring创建对象的过程中，将对象依赖的属性（简单值、对象、集合）通过配置信息设置给该对象。

IoC和DI其实是同一个概念的不同角度描述，DI相对IoC而言，明确描述了“被注入对象依赖IoC容器配置依赖对象”。

Container：容器，在生活中容器就是一种盛放东西的器皿，**从程序设计角度看作是装对象的对象**，因为存在对对象的存入、取出等操作，所以容器还要管理对象的生命周期。

![](https://pic1.zhimg.com/v2-31a5c3b9601bb50d9a5be4d5da1ca0e0_b.jpg)

## **4.1.** **IoC（控制反转）的概述**

Spring号称是一个可以实现模块可插拔的JavaEE开发框架。那么它是如何实现程序的可插拔的呢？

实现程序可插拔的核心理念就是，控制反转（Inversion of Control，英文缩写为IoC）

**所谓的[控制反转](https://zhida.zhihu.com/search?content_id=110123719&content_type=Article&match_order=6&q=%E6%8E%A7%E5%88%B6%E5%8F%8D%E8%BD%AC&zhida_source=entity)，就是将代码的调用权从调用方转移给被调用方（服务提供方）。**

如图所示：

1\. 强耦合调用方式

将A类调用B类对象修改调用C类对象，修改的是调用方的代码，所以我们认为代码的调用权在调用方。

![](https://pica.zhimg.com/v2-f7519727dc95227d71b3d98d600e58be_b.jpg)

2\. 基于IoC（控制反转）的调用方式

将上图的需求，修改为Ioc方式。就是将代码的控制权从调用方修改为被调用方，意味着，代码的调用权转移给被调用方（我们也称为服务方），不用修改调用方的代码。

Ioc方式下只需修改配置文件就实现对象的切换。

如下图：将A类调用B类对象修改为C类对象，修改的是被调用方的配置文件的代码，所以代码的调用权转移到了被调用方。通过控制反转，我们可以实现增加模块或者移除模块统一由配置文件关联，增加或者移除模块，配置XML配置文件即可。

我们将代码的**调用权（控制权）**从**调用方**转移给**被调用方**（服务提供方）的设计模式称为控制反转（IoC）。

![](https://pic4.zhimg.com/v2-e9e24489bdb67c7193cff5cefac5fee3_b.jpg)

根据上图可以得出，实现一个IoC的框架，必须要解决两个问题：

1\. 被调用方（服务方），在程序启动时就要创建好对象，放在一个容器里面。

2\. 调用方使用一个接口或类的引用（不用使用new），在程序运行过程中调用方就可以获取对象。

我们将这种不用new，而是根据接口或者类的引用就可以从容器里获得创建的对象的方式称为依赖注入DI。

所以，控制反转（Ioc），就是依赖注入加上面向接口的编程思想的实现。

**在这里，我们首先抓住一个重点：Spring之所以可以实现可插拔程序，是实现了不用new，使用类或接口就可以获得对象！**

## **4.2.** **Spring的个人思考**

Spring框架本质上作为一个容器的角色存在，我们程序中对象的创建，以及对象间的依赖关系都交由Spring来完成，当我们需要使用对象时，只需向[spring容器](https://zhida.zhihu.com/search?content_id=110123719&content_type=Article&match_order=7&q=spring%E5%AE%B9%E5%99%A8&zhida_source=entity)获取即可，实现了模块间、对象间的解耦，所有对象信息都配置在applicationContext.xml配置文件中，当Spring框架启动时，创建spring容器，读取applicationContext.xml配置文件对象对象到spring容器中去。程序后续使用对象时都从spring容器中获取（getBean方法）。

## **4.3.** **项目[目录结构](https://zhida.zhihu.com/search?content_id=110123719&content_type=Article&match_order=1&q=%E7%9B%AE%E5%BD%95%E7%BB%93%E6%9E%84&zhida_source=entity)**

![](https://pica.zhimg.com/v2-15cf7ab292bee76ebdfef20c655c8716_b.jpg)

## **4.4.** **示例代码**

### **4.4.1.** **CustomerService接口代码**

```
package org.cjw.service;

public interface CustomerService {

    /**
     * 保存方法
     */
    void save();
}
```

### **4.4.2.** **CustomerServiceImpl子类**

```
package org.cjw.service.impl;

import org.cjw.service.CustomerService;

public class CustomerServiceImpl implements CustomerService {

    @Override
    public void save() {
        System.out.println("-保存客户-CustomerServiceImpl");
    }
}
```

### **4.4.3.** **CustomerServiceImpl2子类**

```
package org.cjw.service.impl;

import org.cjw.service.CustomerService;

public class CustomerServiceImpl2 implements CustomerService {

    @Override
    public void save() {
        System.out.println("-保存客户-CustomerServiceImpl2");
    }
}
```

### **4.4.4.** **CustomerClient类（调用方）**

```
package org.cjw.controller;

import org.cjw.service.CustomerService;

public class CustomerController {

    // 1.声明一个父接口的引用
    private CustomerService customerService;

    // 2.使用set方法注入对象，我们将通过方法注入对象的方式称为依赖注入
    public void setCustomerService(CustomerService customerService) {
        this.customerService = customerService;
    }

    public void save() {
        // 调用服务方的方法
        customerService.save();
    }
}
```

### **4.4.5.** **配置文件applicationContext.xml**

```
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
        http://www.springframework.org/schema/beans/spring-beans.xsd">

    <!--
        <bean>标签：用于声明一个类，在启动Spring框架的时候根据配置信息创建对象到容器里面去
    -->
    <!--
        <bean id="customerServiceImpl" class="org.cjw.service.impl.CustomerServiceImpl" />
        可以根据需求，将CustomerServiceImpl修改为CustomerServiceImpl2
    -->
    <bean id="customerServiceImpl" class="org.cjw.service.impl.CustomerServiceImpl2" />

    <bean id="customerController" class="org.cjw.controller.CustomerController">
        <!--
            <property name="" ref="" />标签对应set方法关联对象customerService
                name属性：关联对应的set方法，关联规则：xxx对应setXxx();
                          如：customerService对应setCustomerService()
                ref属性：指向容器中的对象，即set方法的参数
        -->
        <property name="customerService" ref="customerServiceImpl"/>
    </bean>
</beans>
```

### **4.4.6.** **测试代码**

```
package org.cjw.controller.test;

import org.cjw.controller.CustomerController;
import org.junit.Test;
import org.springframework.context.support.ClassPathXmlApplicationContext;

public class CustomerControllerTest {

    @Test
    public void testSave() {
        ClassPathXmlApplicationContext context = new ClassPathXmlApplicationContext("applicationContext.xml");
        CustomerController customerController = context.getBean("customerController", CustomerController.class);
        customerController.save();
    }
}
```

### **4.4.7.** **测试结果**

![](https://pic2.zhimg.com/v2-1246a6eb58a4bca1882606dc19e2894b_b.jpg)

## **5.** **标签说明**

## **5.1.** **alias标签**

作用：为已配置的bean设置别名

\--applicationContext.xml配置文件

```
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
        http://www.springframework.org/schema/beans/spring-beans.xsd">

    <bean id="user" class="org.cjw.pojo.User" />

    <!--
        标签alias：为已配置的bean设置别名
            name属性：必要属性，代表为哪一个bena配置别名
                此属性的值为其他bean标签的id或name属性值
            alias属性：必要属性，代表新命名的别名是什么
    -->
    <alias name="user" alias="user1" />
</beans>
```

\--测试代码

```
package org.cjw.pojo.test;

import org.cjw.pojo.User;
import org.junit.Test;
import org.springframework.context.support.ClassPathXmlApplicationContext;

public class UserTest {

    @Test
    public void testAlias() {
        ClassPathXmlApplicationContext context = new ClassPathXmlApplicationContext("applicationContext.xml");
        // 通过id获取User对象
        User user = context.getBean("user", User.class);
        System.out.println(user);
        System.out.println("-----------------");
        // 通过别名获取User对象
        User user2 = context.getBean("user1", User.class);
        System.out.println(user2);
    }
}
```

\--测试结果

![](https://pic1.zhimg.com/v2-b3e1d7d3c63b4e72fa2d2961c4a35d6c_b.jpg)

## **5.2.** **bean标签的配置**

### **5.2.1.** **bean标签作用**

用于声明一个类，在启动Spring框架的时候根据配置信息创建对象到Spring容器里面。

### **5.2.2.** **属性说明**

```
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
        http://www.springframework.org/schema/beans/spring-beans.xsd">

    <!--
        <bean>标签：用于声明一个类，在启动Spring框架的时候配置信息创建对象到spring容器里面去
            name属性：设置对象名(唯一标识符)，可以有多个名称，每一个名称用逗号隔开，如name1，name2
            id属性：设置对象名(唯一标识符)，功能和name一样，但是id只能有一个
            class属性：用于指定对象对应的类名，用于反射创建对象
            scope属性：用于设置对象的作用范围，可选参数如下：
                *singleton：单例（默认）
                    对象出生：当程序加载配置文件创建容器时，创建
                    对象活着：只要容器还在，一直活着
                    对象死亡：应用停止，容器销毁，对象死亡
                *propertype：多例（原型对象）
                    对象出生：当程序加载配置文件创建容器时，创建
                    对象活着：只要对象被使用，一直活着
                    对象死亡：对象长时间不用，会被java立即回收机制回收
                *request：web项目中，Spring将创建的对象放在request作用域中
                *session：web项目中，Spring将创建的对象放在session作用域中
    -->
    <bean id="customerServiceImpl" class="org.cjw.service.impl.CustomerServiceImpl" scope="singleton" />
</beans>
```

### **5.2.3.** **Bean作用范围**

作用范围也可以说生命周期（bean能存活多久）

<bean id="" class="" **scope="作用域"**/>

![](https://picx.zhimg.com/v2-633e121ae728df1ec635ecff216dcf8b_b.jpg)

**在开发中主要使用 scope="singleton"、 scope="prototype"**

**对于MVC中的Action/Controller使用[prototype](https://zhida.zhihu.com/search?content_id=110123719&content_type=Article&match_order=2&q=prototype&zhida_source=entity)类型，其他使用singleton**

```
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
        http://www.springframework.org/schema/beans/spring-beans.xsd">

    <!--
      <bean id="" class="" scope="作用域"/>
      scope : 配置当前bean的范围大小

      singleton: 单例 ，在Spring IoC容器中仅存在一个Bean实例 （默认的scope）
      prototype: 多例 ，每次从容器中调用Bean时，都返回一个新的实例，即每次调用getBean()时 ，相当于执行new XxxBean()
    -->

    <bean id="customerServiceImpl" class="org.cjw.service.impl.CustomerServiceImpl" scope="prototype" />
</beans>
```

在Web开发的[三层架构](https://zhida.zhihu.com/search?content_id=110123719&content_type=Article&match_order=1&q=%E4%B8%89%E5%B1%82%E6%9E%B6%E6%9E%84&zhida_source=entity)中

Web：一般都是多例

Service：单例

DAO：单例

如果使用struct，那么会在表示层使用成员变量来接受前端发送过来的参数，此时如果表示层使用的是单例，那么会造成数据的错乱，所以表示层需要使用多例。

而现在springMVC已经不再使用成员变量来接受前端参数了，而是直接对应方法的参数，所以表示层可以使用单例，因为方法的参数是在程序运行过程中才会被赋值，所以不存在数据错乱的问题，因此可以使用单例。

单例和多例的使用判断准则：是否存在共享数据情况，如果有，使用多例，没有则单例。如果使用了单例还存在共享数据的情况，那么就需要使用锁来保证数据的正确性。

## **5.3.** **实例化Bean的四种方式**

Spring创建对象的四种方式

### **5.3.1.** **构造器实例化（无参数构造器），最标准，使用最多。**

```
package org.cjw.pojo;

public class SomeBean1 {
    public SomeBean1() {
        System.out.println("SomeBean.SomeBean1()");
    }
}
```

\--配置文件

```
<!-- ①构造器实例化（无参构造器），最标准、使用最多 -->
<bean id="someBean1"  class="org.cjw.pojo.SomeBean1"/>
```

### **5.3.2.** **通过[静态方法](https://zhida.zhihu.com/search?content_id=110123719&content_type=Article&match_order=1&q=%E9%9D%99%E6%80%81%E6%96%B9%E6%B3%95&zhida_source=entity)工厂创建（了解）**

\--bean、静态工厂类

```
SomeBean2、SomeBean2Factory 
public class SomeBean2 {
    public SomeBean2() {
        System.out.println("SomeBean.SomeBean2()");
    }
}
public class SomeBean2Factory {

    public static SomeBean2 getSomeBean2() {
        System.out.println("执行静态工厂方法");
        return new SomeBean2();
    }
}
```

\--静态工厂配置

```
<!-- ②.静态工厂方法实例化：解决系统遗留问题 -->
<bean id="someBean2" class="org.cjw.factory.SomeBean2Factory" factory-method="getSomeBean2" />
```

### **5.3.3.** **通过实体工厂创建（了解）**

\--实体工厂

```
public class SomeBean3 {
    public SomeBean3() {
        System.out.println("SomeBean.SomeBean3()");
    }
}
public class SomeBean3Facotry {
    //实例工厂方法
    public SomeBean3 getSomeBean3() {
        System.out.println("执行实例工厂方法");
        return new SomeBean3();
    }
}
```

\--配置方式

```
<!-- 1.配置工厂bean -->
<bean id="someBean3Factory" class="org.cjw.factory.SomeBean3Facotry"></bean>
<!-- 2.配置bena
    factory-bean : 创建bean的工厂对象对应的 id
    factory-method : 工厂bean中返回 bean对象的方法
 -->
<bean id="someBean3" factory-bean="someBean3Factory" factory-method="getSomeBean3"/>
```

### **5.3.4.** **实现FactoryBean接口实例化：实例工厂变种（了解）**

实现FactoryBean接口，MyBatis和Spring集成就是使用的这种方式。

此种方式，如果没有使用Bean对应的对象，Spring就不会自动创建，只有在使用的时候Spring才会创建对应的对象。

```
public class SomeBean4 {
    public SomeBean4() {
        System.out.println("SomeBean4.SomeBean4()");
    }
}
public class SomeBean4ObjectFactory implements FactoryBean<SomeBean4> {

    @Override
    public SomeBean4 getObject() throws Exception {
        SomeBean4 bean4 = new SomeBean4();
        return bean4;
    }

    @Override
    public Class<?> getObjectType() {
        return null;
    }

    @Override
    public boolean isSingleton() {
        return false;
    }
}
```

\--配置方式

```
<!-- ④.实现FactoryBean接口实例化：实例工厂变种：集成其他框架使用：LocalSessionFactoryBean -->
<bean id="someBean4" class="org.cjw.factory.SomeBean4ObjectFactory" />
```

## **5.4.** **初始化和销毁方法**

比如DataSource,SessionFactory最终都需要关闭资源:在Bean销毁之前,都要调用close方法.

```
<bean id="someBean" class="......" 
   		init-method="该类中初始化方法名" destroy-method="该类中销毁方法名">
</bean>
```

init-method：bean生命周期初始化方法,对象创建后就进行调用

destroy-method:容器被销毁的时候，如果bean被容器管理，会调用该方法。

default-init-method：指定默认的初始化方法

分析原理:

如果bean的scope="prototype",那么容器只负责创建和初始化，它并不会被spring容器管理。交给用户自己调用。

```
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
        http://www.springframework.org/schema/beans/spring-beans.xsd"
        default-init-method="init">
        <!--
            配置全局初始化方法,如果有100个bean中都有init方法,那么只要Spring容器一启动,bean对象一创建
            默认对象中只要有 init方法,都全部会执行:一般不建议使用
        -->

     <!--
       init-method : 配置初始化方法名
       destroy-method : 配置销毁方法名
    -->
    <bean id="someBean" class="org.cjw.pojo.SomeBean1" init-method="init" destroy-method="destory" />
</beans>
```

## **6.** **Spring[依赖注入](https://zhida.zhihu.com/search?content_id=110123719&content_type=Article&match_order=9&q=%E4%BE%9D%E8%B5%96%E6%B3%A8%E5%85%A5&zhida_source=entity) DI**

**DI：Dependency Injection（依赖注入）**

从字面上分析：

IoC：指将对象的创建权，反转给了Spring容器；

DI ：指Spring创建对象的过程中，将对象[依赖属性](https://zhida.zhihu.com/search?content_id=110123719&content_type=Article&match_order=1&q=%E4%BE%9D%E8%B5%96%E5%B1%9E%E6%80%A7&zhida_source=entity)（简单值，集合，对象）通过配置设值给该对象。

IoC和DI其实是同一个概念的不同角度描述，DI相对IoC而言，明确描述了“被注入对象依赖IoC容器配置依赖对象”。

所谓的依赖注入，就是属性不创建对象，通过配置文件的配置将Spring容器里面的对象注入给对应的属性。

依赖注入有四种方式

## **6.1.** **setter注入（属性注入）**

1.setter注入,(也可以称之为属性注入)

使用setter注入：

1，使用bean元素的**<property>**子元素设置；

①简单类型值，直接使用value赋值；

②引用类型，使用ref赋值；

③集合类型，直接使用对应的集合类型元素即可。

2，spring通过属性的setter方法注入值；

3，在配置文件中配置的值都是string，spring可以自动的完成类型转换

```
 package org.cjw.pojo;

public class Employee {

    private String name;
    private Integer age;
    private Department dept;
    // get、set、toString、无参构造、有参构造方法
}
package org.cjw.pojo;

public class Department {

    private Integer id;
    private String name;

    // get、set方法
}
```

\--配置文件

```
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
        http://www.springframework.org/schema/beans/spring-beans.xsd">

    <!-- 员工 -->
    <bean id="employee" class="org.cjw.pojo.Employee">
        <!-- setter方法注入，属性注入
            <property name="" value/ref="">
            name：属性名称
            value：基本类型+String+包装类型值注入
            ref：除了value以外的引用类型(对象)注入
            注意：value和ref只能二选一
         -->
        <property name="name" value="cjw" />
        <property name="age" value="18" />
        <property name="dept" ref="dept" />
    </bean>

    <!-- 部门 -->
    <bean id="dept" class="org.cjw.pojo.Department">
        <property name="id" value="1" />
        <property name="name" value="研发部" />
    </bean>
</beans>
```

## **6.2.** **[构造器注入](https://zhida.zhihu.com/search?content_id=110123719&content_type=Article&match_order=1&q=%E6%9E%84%E9%80%A0%E5%99%A8%E6%B3%A8%E5%85%A5&zhida_source=entity)**

```
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
        http://www.springframework.org/schema/beans/spring-beans.xsd">

    <!--
        <constructor-arg name/index=""  value/ref=""/>
            默认情况下，constructor-arg的顺序就是构造器参数的顺序
            name: 在构造器中按照构造器的参数名字设置值
            index：在构造器中的参数索引(从0开始)，index有默认值，就是当前constructor-arg出现的序号
            value/ref：在构造器中的实参值，value用于简单值、ref用于对象(引用值)
            注意：要么name和value/ref搭配(常用，直观明了)、要么index和value/ref搭配
              ====================
            使用哪种注入方式比较好（setter？构造器？）？
            1，如果一个类必须依赖另一个类才能正常运行，用构造器；
            2，但是构造器的参数如果过多，构造器很难看；
            3，更多的还是使用setter注入；
            4，可以使用@Required标签来要求一个属性必须注入
             [1] 将@Required注解放置在需要必须注入的属性的setter方法上
             [2] 在Spring容器中注册RequiredAnnotationBeanPostProcessor类，用于检测@Required注解下的方法是否以被执行过。
             <bean class="org.springframework.beans.factory.annotation.RequiredAnnotationBeanPostProcessor"/>
             @Required注解只针对setter注入方式的DI，用于确认某些属性是否已被初始化，而构造器注入则是根据提供的有参构造来进行的，
             换句话说，有参构造的形式决定了构造器注入的形式。
    -->

    <bean id="employee" class="org.cjw.pojo.Employee">
        <constructor-arg name="name" value="cjw"/>
        <constructor-arg name="age" value="18" />
        <constructor-arg name="dept" ref="dept" />
    </bean>

    <bean id="dept" class="org.cjw.pojo.Department"/>
</beans>
```

## **6.3.** **p命名空间注入**

使用p命名空间注入，需要先在约束上面引入 p标签

```
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xmlns:p="http://www.springframework.org/schema/p"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
        http://www.springframework.org/schema/beans/spring-beans.xsd">

    <!--
        属性类型是简单类型：p:属性名=属性值
        属性类型是引用类型：p:属性名-ref=对象引用
    -->
    <bean id="employee" class="org.cjw.pojo.Employee" p:name="cjw" p:age="18" p:dept-ref="dept"/>

    <bean id="dept" class="org.cjw.pojo.Department"/>
</beans>
```

## **6.4.** **集合类型值注入**

在处理的数据中，

有标量类型（基础数据类型以及包装类+String）-- value属性

也有引用类型 --ref属性

还要很多数据JDK内置的数据结构：

1\. 键值对 Map、Properties

2\. 数组

3\. 集合Set、List

对于集合类型的属性使用集合类型值注入。

```
package org.cjw.pojo;

import java.util.*;

public class CollectionBean {
    private Set<String> set;
    private List<String> list;
    private String[] array;
    private Map<String, String> map;
    private Properties prop; //读取本地 xxx.properties文件(本质就是一个Map集合)
    // get、set、toString方法
}
```

\-- 配置文件

```
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
        http://www.springframework.org/schema/beans/spring-beans.xsd">

    <bean id="collectionBean" class="org.cjw.pojo.CollectionBean">
        <property name="set">
            <set>
                <value>set1</value>
                <value>set2</value>
                <value>set3</value>
            </set>
        </property>
        <property name="list">
            <list>
                <value>list1</value>
                <value>list2</value>
                <value>list3</value>
            </list>
        </property>
        <property name="array">
            <array>
                <value>array1</value>
                <value>array2</value>
                <value>array3</value>
            </array>
        </property>
        <property name="map">
            <map>
                <entry key="key1" value="value1" />
                <entry key="key2" value="value2" />
                <entry key="key3" value="value3" />
            </map>
        </property>
        <property name="prop">
            <props>
                <prop key="prop1">proValue1</prop>
                <prop key="prop2">proValue2</prop>
                <prop key="prop3">proValue3</prop>
            </props>
        </property>
    </bean>
</beans>
```

## **7.** **获得[properties](https://zhida.zhihu.com/search?content_id=110123719&content_type=Article&match_order=2&q=properties&zhida_source=entity)文件的值**

Spring配置文件支持通过xxx.properties文件的Key获得对应的值。实现该功能是通过

通过${Key}来获得Properties文件指定Key的Value值。

使用[Spring](https://zhida.zhihu.com/search?content_id=110123719&content_type=Article&match_order=71&q=Spring&zhida_source=entity)读取配置文件必须导入新的命名空间（context）。

导入命名空间方法：将命名空间和约束重新拷贝一份，将对应的全部替换成 context，然后关联context本地schema约束。

```
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xmlns:context="http://www.springframework.org/schema/context"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
        http://www.springframework.org/schema/beans/spring-beans.xsd 
        http://www.springframework.org/schema/context
        http://www.springframework.org/schema/context/spring-context.xsd">
```

## **7.1.** **使用Spring创建[阿里巴巴](https://zhida.zhihu.com/search?content_id=110123719&content_type=Article&match_order=1&q=%E9%98%BF%E9%87%8C%E5%B7%B4%E5%B7%B4&zhida_source=entity) Druid连接池（读取配置文件）**

### **7.1.1.** **拷贝Mysql驱动包和druid连接池jar包到项目中**

![](https://pic1.zhimg.com/v2-47a6a14921b636673d12f4b479528902_b.png)

### **7.1.2.** **创建 db.properites**

```
jdbc.driverClassName=com.mysql.jdbc.Driver
jdbc.url=jdbc:mysql://localhost:3306/users
jdbc.username=root
jdbc.password=root
jdbc.maxActive=10
```

### **7.1.3.** **applicationContext.xml配置**

```
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xmlns:context="http://www.springframework.org/schema/context"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
        http://www.springframework.org/schema/beans/spring-beans.xsd
        http://www.springframework.org/schema/context
        http://www.springframework.org/schema/context/spring-context.xsd">

    <!-- 读取classpath下的db.properties配置文件 -->
    <context:property-placeholder location="classpath:db.properties" />

    <!-- 配置数据源 -->
    <bean id="dataSource" class="com.alibaba.druid.pool.DruidDataSource">
        <property name="driverClassName" value="${jdbc.driverClassName}" />
        <property name="url" value="${jdbc.url}" />
        <property name="username" value="${jdbc.username}" />
        <property name="password" value="${jdbc.password}" />
        <property name="maxActive" value="${jdbc.maxActive}" />
    </bean>
</beans>
```

### **7.1.4.** **测试代码**

```
@Test
public void testAlias() {
    try {
        ClassPathXmlApplicationContext context = new ClassPathXmlApplicationContext("applicationContext.xml");
        DataSource dataSource = context.getBean("dataSource", DataSource.class);
        Connection connection = dataSource.getConnection();
        System.out.println(connection);
    } catch (SQLException e) {
        e.printStackTrace();
    }
}
```

### **7.1.5.** **效果**

![](https://pic3.zhimg.com/v2-3053b8684d4a24c2c5b5a6e514ee1c80_b.jpg)

## **8.** **模拟注册功能**

此功能重点在于将每一层对象的创建交给Spring管理，对象之间的依赖关系交给Spring来维护。

## **8.1.** **Dao层接口以及实现代码**

```
public interface UserDao {

    public void insert(User user);
}
public class UserDaoImpl implements UserDao {
    @Override
    public void insert(User user) {
        System.out.println("注册功能Dao层方法执行了");
    }
}
```

## **8.2.** **Service层接口以及实现代码**

```
public interface UserService {

    void insert(User user);

}
public class UserServiceImpl implements UserService {

    private UserDao userDao;

    public void setUserDao(UserDao userDao) {
        this.userDao = userDao;
    }

    @Override
    public void insert(User user) {
        System.out.println("注册功能Service层方法执行了");
        userDao.insert(user);
    }
}
```

## **8.3.** **Web表现层实现代码**

```
package org.cjw.controller;

import org.cjw.pojo.User;
import org.cjw.service.UserService;

public class UserController {

    private UserService userService;

    public void setUserService(UserService userService) {
        this.userService = userService;
    }

    public void insert() {
        System.out.println("注册功能Controller层方法执行了");
        User user = new User();
        userService.insert(user);
    }

}
```

## **8.4.** **applicationContext.xml文件配置代码(重点),一定要掌握每层的配置,和每层之间对象的依赖关系的维护**

```
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
        http://www.springframework.org/schema/beans/spring-beans.xsd">

    <bean id="userController" class="org.cjw.controller.UserController">
        <property name="userService" ref="userService" />
    </bean>

    <bean id="userService" class="org.cjw.service.impl.UserServiceImpl">
        <property name="userDao" ref="userDao" />
    </bean>

    <bean id="userDao" class="org.cjw.dao.impl.UserDaoImpl" />

</beans>
```

## **8.5.** **测试代码**

```
@Test
public void testAlias() {
    ClassPathXmlApplicationContext context = new ClassPathXmlApplicationContext("applicationContext.xml");
    UserController userController = context.getBean("userController", UserController.class);
    userController.insert();
}
```

## **8.6.** **测试结果**

![](https://pica.zhimg.com/v2-7e0a0efe66d08ca342299ecc59f36256_b.jpg)

## **9.** **小结**

1\. 优秀的项目架构的特点

(1) 高内聚

① 项目分层开发（每层处理各自的任务，职责分明）

(2) 低耦合

① 对象与对象之间有不直接产生依赖（不直接new对象）

2\. 低耦合的解决方案

(1) 开发者自己底层使用反射进行封装相关代码

(2) 使用优秀的框架 Spring

3\. 什么是Spring？

(1) 轻量级一站式框架

(2) 轻量级

① Spring有20个模块，只需要四个模块即可启动Spring框架，其他模块按需引入即可

(3) 一站式

① Web开发的三层架构 ，Web层、Service层，Dao层，全部使用Spring框架完成

4\. Spring如何实现解耦

(1) IOC ：控制反转

① 将对象创建权交给Spring管理

② 负责管理对象生命周期（有效期）

③ 执行对象的初始化方法，销毁方法

④ IOC创建对象实例有四种方式

**1)** **直接使用无参数构造函数-推荐**

a. <bean id = ‘’’ class =””>

2) 使用静态工厂创建bean

3) 使用实例工厂创建bean

4) 使用变种实例工厂，工厂类实现 FactoryBean接口

(2) DI ：依赖注入（将对象的属性通过Spring赋值）

**①** **Setter方法（属性）注入**

**②** **构造器注入**

**③** **P[命名空间](https://zhida.zhihu.com/search?content_id=110123719&content_type=Article&match_order=6&q=%E5%91%BD%E5%90%8D%E7%A9%BA%E9%97%B4&zhida_source=entity)注入**

**④** **集合类型值类型，引用类型和支持各种集合数据类型的注入**

**5.** **Spring读取 .Properteis配置文件**

**6.** **综合案例-模拟注册功能-使用Spring管理对象**