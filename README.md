# Google Summer Of Code 2022 for Casbin

Note: There are some significant changes in GSoC 2022 like expanding eligibility and multiple sizes of projects, see details at GSoC official site: https://opensource.googleblog.com/2021/11/expanding-google-summer-of-code-in-2022.html

## What is Google Summer Of Code?

Google Summer of Code (GSoC) is a global program held by Google to bring students into open source software development. Students work with an open source organization on a 3 month programming project during their break from school. See more details at: https://summerofcode.withgoogle.com/

## How we select students:

The student will be more likely selected if he/she:

1. Contribute to Casbin related project before.
2. Familiar with the techniques required by the idea he selected.
3. Show the previous code related to the idea on personal website or GitHub.
4. Provide a personal website and descriptions for previous work/projects.
5. Provide demo sites for the previous projects if possible.
6. Provide a resume/CV.

## Get started

1. Choose an idea from our list: https://github.com/casbin/SummerOfCode2022
2. Send your resume/CV in PDF to: admin@casbin.org
3. Do a self-introduction in: https://gitter.im/casbin/gsoc
4. Get familiar with the existing code, try to solve opened issues for your chosen idea's repo before & after application deadline.
5. If you have questions, you can ask the mentor of the idea via GitHub or Gitter.
6. Submit your proposal in [GSoC official site](https://summerofcode.withgoogle.com/). The deadline is TBD.

## Ideas

- [Casbin Core Engine (Golang)](#casbin-core-engine-golang)
- [Casdoor](#casdoor)
- [Casnode](#casnode)
- [Casbin for C/C++](#casbin-for-cc)
- [Casbin for Java](#casbin-for-java)
- [Casbin for .NET](#casbin-for-net)
- [Casbin Sam](#casbin-sam)
- [Casbin for Rust](#casbin-for-rust)
- [Casbin for Node.js](#casbin-for-nodejs)
- [Casbin Hub](#casbin-hub)
- [Casbin for PHP](#casbin-for-php)
- [Casbin for Python](#casbin-for-python)
- [Casbin.js](#casbinjs)
- [Casbin for Lua](#casbin-for-lua)
- [Casbin for Dart](#casbin-for-dart)
- [Casbin for Swift](#casbin-for-swift)



### Casbin Core Engine (Golang)

#### Description

Support more features and tune the performance in Casbin core engine. This will first be done in Golang Casbin. Possibly applied to other language implementations.

#### Expected outcomes

Some issues to work on:

1. Resolve policy conflicts: https://github.com/casbin/casbin/issues/338
2. Improve the performance of the new BatchEnforce() API: https://github.com/casbin/casbin/issues/710
3. Make an authorization plugin/middleware for kubernetes (k8s): https://github.com/casbin/k8s-authz/issues/2
4. Help solve issues for the 1st-party and 3rd-party middlewares

#### Skills required/preferred

1. Golang
2. Other languages that Casbin is written with

#### Mentors

[Yang Luo](https://github.com/hsluoyz), Casbin founder

#### Expected size of project (175 hour or 350 hour)

350 hour

#### Rating (Easy, Medium or Hard)

Medium



### Casdoor

#### Description

Build a UI-first centralized authentication / Single-Sign-On (SSO) platform based on OAuth 2.0 / OIDC. It can:

1. Use OAuth 2.0 + OIDC as the authentication protocols.
2. Support popular 3rd-party identity providers like Google, GitHub, Facebook, etc.
3. Has a web portal to manage users, roles and permissions.
4. Use Casbin as authorization method.
5. Support user register, login, password reset, 2FA like Email and SMS.

The current progress is: https://door.casdoor.com/. Source code: https://github.com/casdoor/casdoor. We want the student to continue the work.

#### Expected outcomes

#### Skills required/preferred

1. Golang (backend)
2. Javascript + React + Ant Design (frontend)
3. Casbin

#### Mentors

[Yang Luo](https://github.com/hsluoyz), Casbin founder

#### Expected size of project (175 hour or 350 hour)

350 hour

#### Rating (Easy, Medium or Hard)

Medium



### Casnode

#### Description

Casnode is a light-weight forum software. It is used by Casbin community as the official developer forum (https://forum.casbin.com/). We hope to fix its bugs and add more features like mailing list to replace the traditional open-source community mailing list.

The current progress is: https://github.com/casbin/casnode

#### Expected outcomes

Some issues to work on:

1. Integrate open-source mailing list functionality to Casnode: https://github.com/casbin/casnode/issues/112
2. Make it SEO friendly via SSR: https://github.com/casbin/casnode/issues/122
3. The text area is at risk of XSS injection: https://github.com/casbin/casnode/issues/131
4. The ranking pages do not display correctly: https://github.com/casbin/casnode/issues/132
5. Use Casdoor as the authentication system: https://github.com/casbin/casnode/issues/145

#### Skills required/preferred

1. Golang (backend)
2. Javascript + React (frontend)
3. Casbin

#### Mentors

[Junjie Zhang](https://github.com/kocoler), Casbin member, [Yang Luo](https://github.com/hsluoyz), Casbin founder

#### Expected size of project (175 hour or 350 hour)

175 hour

#### Rating (Easy, Medium or Hard)

Easy



### Casbin for C/C++

#### Description

We already have a C/C++ version Casbin called [Casbin-CPP](https://github.com/casbin/casbin-cpp). It already works on all primary OSs, like Windows, Linux, macOS. Most of Casbin's functionalities (for example 90%) should work. There are still many bugs and missing features in Casbin-CPP. Moreover, we also need to make authz middlewares for other C++ projects like [Mosquitto](https://github.com/casbin/casbin-cpp/issues/79 ) and adapters for DB. We also have plan to make Casbin-CPP as a base layer to build the next-generation PyCasbin and PHP-Casbin on top of it (see [PyCasbin on CPP](https://github.com/casbin/pycasbin-on-cpp )) for better performance (a lot of Python packages like numpy and tensorflow rely on the underlying C++ code). So Casbin-CPP needs to provide necessary help if needed for PyCasbin and PHP-Casbin developers.

The current progress is: https://github.com/casbin/casbin-cpp

#### Expected outcomes

#### Skills required/preferred

1. C/C++
2. Golang (only need to read code)

#### Mentors

[Joey Xie](https://github.com/xcaptain), Casbin member, [Yang Luo](https://github.com/hsluoyz), Casbin founder

#### Expected size of project (175 hour or 350 hour)

175 hour

#### Rating (Easy, Medium or Hard)

Hard



### Casbin for Java

#### Description

In Java world, Apache Shiro and Spring Security are very popular security frameworks. We need to find ways to improve the Casbin middlewares for both of them, so Shiro and Spring Security users can use jCasbin without many migrating efforts.

Another work is to develop jCasbin' middleware for the popular Java web frameworks except Spring such as Play and Vert.x, like how we did it for Golang: https://casbin.org/docs/en/middlewares

Some issues to work on:

1. Make a Play Framework middleware: https://github.com/casbin/jcasbin/issues/104
2. Make a Vert.x middleware: https://github.com/casbin/jcasbin/issues/105
3. Fix the bug about "ABAC with policy rule" doesn't work: https://github.com/casbin/jcasbin/issues/145
4. Improve the user experience of the SpringBoot middleware: https://github.com/jcasbin/casbin-spring-boot-starter
5. Make an example project that uses our Shiro middleware: https://github.com/jcasbin/shiro-casbin

#### Skills required/preferred

1. Java
2. Other languages that Casbin is written with

#### Mentors

[Zhengjin Fang](https://github.com/fangzhengjin), Casbin member, [Yang Luo](https://github.com/hsluoyz), Casbin founder

#### Expected size of project (175 hour or 350 hour)

175 hour

#### Rating (Easy, Medium or Hard)

Medium



### Casbin for .NET

#### Description

The feature and ecosystem of Casbin.NET are gradually improving. We hope to provide complete features with a goal to Golang Casbin, excellent performance, and suitable for user experience in .NET.

#### Expected outcomes

There are some important features that need to be implemented:

1. Rule Indexing feature : https://github.com/casbin/Casbin.NET/issues/132
2. Parallel enforcing feature : https://github.com/casbin/Casbin.NET/issues/133
2. Multiple request, policy, effect, matcher type support : https://github.com/casbin/Casbin.NET/issues/134

#### Skills required/preferred

1. .NET/C#
2. Other languages that Casbin is written with

#### Mentors

[Joey Xie](https://github.com/xcaptain), Casbin member, [Zhikui Hua](https://github.com/huazhikui), Casbin member

#### Expected size of project (175 hour or 350 hour)

175 hour

#### Rating (Easy, Medium or Hard)

Medium



### Casbin Sam

#### Description

A authorization service based on OAuth 2.x and support centralized authentication / Single-Sign-On (SSO) integration.

#### Expected outcomes

Some issues to work on:

1. Use [Casbin.NET](https://github.com/casbin/Casbin.NET) and [Casbin.AspNetCore](https://github.com/casbin-net/casbin-aspnetcore) to authorizate.
2. Provide Web APIs to manage users, roles and permissions.
3. Support integrate OIDC authentication provider ([Identity Server 4](https://github.com/IdentityServer/IdentityServer4)) and [ASP.NET Identity](http://docs.identityserver.io/en/latest/quickstarts/6_aspnet_identity.html) to manage user and sgin in/out.
4. Support be integrated to [Dapr](https://github.com/dapr/dapr) or [Steeltoe](https://github.com/SteeltoeOSS/Steeltoe) as authentication/authorization provider.

The current progress is: https://github.com/casbin-net/casbin-sam. We want the student to continue the work.

#### Skills required/preferred

1. .NET/C#
2. [Casbin.NET](https://github.com/casbin/Casbin.NET) and [Casbin.AspNetCore](https://github.com/casbin-net/casbin-aspnetcore)
3. [Dapr](https://github.com/dapr/dapr) or [Steeltoe](https://github.com/SteeltoeOSS/Steeltoe)

#### Mentors

[Joey](https://github.com/xcaptain), Casbin member, [Zhikui Hua](https://github.com/huazhikui), Casbin member, [Yang Luo](https://github.com/hsluoyz), Casbin founder

#### Expected size of project (175 hour or 350 hour)

175 hour

#### Rating (Easy, Medium or Hard)

Medium

### Casbin for Rust

#### Description

With Casbin community's effort, the Rust version of Casbin is now mature and ready for production. [Casbin-RS](https://github.com/casbin/casbin-rs) can provide access control with blazing fast speed.

#### Expected outcomes

There are something need to be implemented，from easy to hard:

1. Embrace Rust 2021 edition [Easy]

- Complete the migration from edition 2018 to edition 2021.
- Clean up stale and meaningless dependencies and make clippy happy.

**Note** This work will help you get familiar with the Rust toolchain and the existing work of Casbin-RS, so please complete it for at least two repos.

2. Continuous maintenance of the surrounding ecology [Medium]

- Implement a middleware for [Poem](https://github.com/poem-web/poem) with examples.
- An article introducing how to use casbin-rs with poem.
- Participate in the maintenance of at least one other repo, such as [sqlx-adapter](https://github.com/casbin-rs/sqlx-adapter) or [casbin-grpc](https://github.com/casbin-rs/casbin-grpc/).

**Note** This work will help you understand the mechanics of casbin's operation. In addition, we hope you can present your works, which will become an important milestone for you in the casbin community.

3. Explore casbin-rs in real-world/distributed applications [Hard]

- You can choose to:
  - Implement a real-world application with casbin-rs, Or
  - Implementing [openraft](https://github.com/datafuselabs/openraft)-based distributed casbin clusters/plugins.
- An article that describes your current work.

**Note** Go beyond the existing casbin-rs projects, this is a job that is completely led by you. [casbin-grpc](https://github.com/casbin-rs/casbin-grpc/) and [casbin-raft](https://github.com/casbin-rs/casbin-raft/) are the results of some previous explorations.


#### Skills required/preferred

1. Rust
2. Other languages that Casbin is written with

#### Mentors

[Chojan Shang](https://github.com/PsiACE), Casbin member, [Yisheng Chai](https://github.com/hackerchai), Casbin member, [Cheng JIANG](https://github.com/GopherJ), Casbin member, [Yang Luo](https://github.com/hsluoyz), Casbin founder

#### Expected size of project (175 hour or 350 hour)

175 hour

#### Rating (Easy, Medium or Hard)

Hard



### Casbin for Node.js

#### Description

Improving the user experience of Node-Casbin will be our focus. Currently, Node-Casbin provides a set of asynchronous API, if we can provide a set of synchronous API, it will be a great experience.

#### Expected outcomes

Some issues to work on:

- Support a full set of Sync API like enforcer.enforce()(https://github.com/casbin/node-casbin/issues/224)

- Scaling Access Control Lists for multi-million users(https://github.com/casbin/node-casbin/issues/147)

- Sequelize v6 compatibility: addPolicies & removePolicies problem(https://github.com/casbin/node-casbin/issues/207)

#### Skills required/preferred

1. JavaScript (Node.js/TypeScript)
2. Other languages that Casbin is written with

#### Mentors

[Zixuan Liu](https://github.com/nodece), Casbin member

#### Expected size of project (175 hour or 350 hour)

175 hour

#### Rating (Easy, Medium or Hard)

Medium



### Casbin Hub

Casbin Hub is similar to [Docker Hub](https://hub.docker.com/search?q=&type=edition&offering=community) website, which is mainly used to share and discuss the model and policy of Casbin.

#### Expected outcomes

We need to implement the following features:

1. Support anyone to share the model and policy of Casbin. Sharers must describe the scenario that this model applies, and mark the classification, like so: Frontend, Backend, Cloud, Message System, and so on. Users can discuss shared content.

2. Integrate the [Casbin-Online-Editor](https://casbin.org/en/editor) is used to test or debug the model and policy shared by users.

#### Skills required/preferred

1. Golang (Backend)
2. React (Frontend)
3. Casbin

#### Mentors

[Zixuan Liu](https://github.com/nodece), Casbin member, [Yang Luo](https://github.com/hsluoyz), Casbin founder

#### Expected size of project (175 hour or 350 hour)

175 hour

#### Rating (Easy, Medium or Hard)

Medium



### Casbin for PHP

#### Description

#### Expected outcomes

1. Full implementation of Casbin(go) by PHP, then fix [issues](https://github.com/php-casbin/php-casbin/issues).
2. Improve some [extensions](https://github.com/php-casbin).

#### Skills required/preferred

1. PHP
2. Casbin

#### Mentors

[Jon Lee](https://github.com/techoner), Casbin member

#### Expected size of project (175 hour or 350 hour)

175 hour

#### Rating (Easy, Medium or Hard)

Medium



### Casbin for Python

#### Description

1. At present, compared to Casbin for Golang, `Pycasbin` is not very perfect, especially the lack of RBAC API, so we hope that `Pycasbin` can fully implement the function of Casbin (Go).
2. `PyCasbin`'s adaptation to various frameworks, such as `Django`, `Tornado`, etc.

Pycasbin organization: https://github.com/pycasbin

#### Expected outcomes

Some issues to work on: https://github.com/casbin/pycasbin/issues

#### Skills required/preferred

1. Python
2. Other languages that Casbin is written with

#### Mentors

[Jon Lee](https://github.com/techoner), Casbin member

#### Expected size of project (175 hour or 350 hour)

175 hour

#### Rating (Easy, Medium or Hard)

Medium



### Casbin.js

#### Description

Quite a lot of users want to use Casbin to control web frontend UI elements, like:

1. Some tabs are only visible to admin users.
2. Some buttons should be grayed-out for users with no permission to click them.
3. A list can only show filtered items based on a user's permission rights.

Currently, Node-Casbin already supports to run in browser. But the API like `enforce()` is still not friendly to frontend developers to control the visibility of a button. So we need:

1. A frontend developer friendly API for authorization based on Casbin, e.g., `isVisible(button_id)`
2. A mechanism to load model and policy data from backend. Of course we assume the backend also uses a Casbin implementation.

The current progress is: https://github.com/casbin/casbin.js

Currently, we still lack the middlewares for Angular, React and Vue. These new JS frameworks are very popular and making middlewares for them will boost our usage from their population.

#### Expected outcomes

Some issues to work on:

1. Make a React authz middleware for Casbin.js: https://github.com/casbin/casbin.js/issues/26
2. Make a Vue authz middleware for Casbin.js: https://github.com/casbin/casbin.js/issues/27
3. Support Key Matching: https://github.com/casbin/casbin.js/issues/15
4. Support domains in model: https://github.com/casbin/casbin.js/issues/25
5. Resolve Casbin.js 0.1.0 with react-scripts 4.0.2 conflict: https://github.com/casbin/casbin.js/issues/28

#### Skills required/preferred

1. Javascript
2. Node-Casbin
3. At least one backend language like Golang

#### Mentors

[Zihui Liu](https://github.com/kingiw), Casbin member, [Yang Luo](https://github.com/hsluoyz), Casbin founder

#### Expected size of project (175 hour or 350 hour)

175 hour

#### Rating (Easy, Medium or Hard)

Hard



### Casbin for Lua

#### Description

Port Golang Casbin into Lua. We call it `lua-casbin`. It should work on the Nginx + OpenResty stack. Most of Casbin's functionalities (for example 90%) should work.

Nginx is now the most popular HTTP server in the world. OpenResty is a web platform based on Nginx which can run Lua scripts using its LuaJIT engine. Nginx + OpenResty are usually used in edge computing and authorization is a real need for its scenario. Lua-Casbin will help Nginx and OpenResty users on checking permissions of the coming HTTP request.

The current progress is: https://github.com/casbin/lua-casbin

#### Expected outcomes

#### Skills required/preferred

1. Nginx
2. OpenResty
1. Lua
2. Golang (only need to read code)

#### Mentors

[Yang Luo](https://github.com/hsluoyz), Casbin founder

#### Expected size of project (175 hour or 350 hour)

175 hour

#### Rating (Easy, Medium or Hard)

Medium



### Casbin for Dart

#### Description

Port Casbin to Dart, little progress has been made in the project so it's excellent for jumping in early.

The current progress is: https://github.com/casbin/dart-casbin

#### Expected outcomes

You will be responsible for the design and making of the Dart port with the help of the mentor, most of Casbin's functionalities should work.

#### Skills required/preferred

1. Dart
2. Other languages that Casbin is written with.

#### Mentors

[Tomás Arias](https://github.com/KNawm), Casbin member

#### Expected size of project (175 hour or 350 hour)

175 hour

#### Rating (Easy, Medium or Hard)

Medium



### Casbin for Swift

#### Description

We already have a Swift version Casbin called [SwiftCasbin](https://github.com/casbin/SwiftCasbin.git). It already works on all primary OSs, like Windows, Linux, macOS,iOS,tvOS,watchOS. Most of Casbin's functionalities (for example 90%) should work.

The current progress is: https://github.com/casbin/SwiftCasbin

#### Expected outcomes

There are still many bugs and missing features in SwiftCasbin. Moreover, we also need to make authz middlewares for any  Swift projects:

1. Server-Side like Vapor and adapters for DB.
2. A frontend developer friendly API for UI frameworks like UIKit,SwiftUI.

#### Skills required/preferred

1. Swift
2. Golang (only need to read code)
3. ios UIkit SwiftUI

#### Mentors

[Xiaobei](https://github.com/xiaobeiswift), Casbin member, [Yang Luo](https://github.com/hsluoyz), Casbin founder

#### Expected size of project (175 hour or 350 hour)

175 hour

#### Rating (Easy, Medium or Hard)

Medium
