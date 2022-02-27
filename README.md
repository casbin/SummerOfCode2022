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
- [Casdoor for .NET](#casdoor-for-net)
- [Casbin for Cloud Native](#casbin-for-cloud-native)
- [Casbin for Rust](#casbin-for-rust)
- [Casbin for Node.js](#casbin-for-nodejs)
- [Casbin Hub](#casbin-hub)
- [Casbin for PHP](#casbin-for-php)
- [Casbin for Python](#casbin-for-python)
- [Casbin.js](#casbinjs)
- [Casbin for Lua](#casbin-for-lua)
- [Casbin for Dart](#casbin-for-dart)
- [Casbin for Swift](#casbin-for-swift)
- [Casbin Mesh](#casbin-mesh)



### Casbin Core Engine (Golang)

#### Description

Support more features and tune the performance in Casbin core engine. This will first be done in Golang Casbin. Possibly applied to other language implementations.

#### Expected outcomes

Some issues to work on:

1. Make a Casbin middleware for go-zero: https://github.com/casbin/casbin/issues/957
2. Improve the performance of the new BatchEnforce() API: https://github.com/casbin/casbin/issues/710
3. Make a default implementation of WatcherEx: https://github.com/casbin/casbin/issues/943
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

Some issues to work on:

1. Support SAML as IdP: https://github.com/casdoor/casdoor/issues/405
2. Support password hashing in LDAP: https://github.com/casdoor/casdoor/issues/499
3. Add Telegram provider: https://github.com/casdoor/casdoor/issues/341
4. Add Casbin model and policy management: https://github.com/casdoor/casdoor/issues/95
5. Design and develop a more beautiful frontend portal: https://github.com/casdoor/casdoor/issues/69

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

Some features to add/improve:

1. Further optimized the project UI: https://github.com/casbin/casnode/issues/400
  Now casnode UI may break on some models, mainly mobile phones, we need to further optimize our project UI to fix it.
2. Anonymous-Post
  Note: we may change whether to enable the node's anonymous function via the admin console.
3. Improve the part of https://forum.casbin.com/api and https://forum.casbin.com/swagger/#/ that provides API externally.
4. Implement [notes](https://forum.casbin.com/notes), so users could create and publish notes: https://github.com/casbin/casnode/issues/341.
4. Implement [timeline](https://forum.casbin.com/timeline), so users could post their thoughts and reply to others' thoughts there: https://github.com/casbin/casnode/issues/341
5. Add RSS feed.
6. Add some metrics, for Prometheus or others.
7. Backup and recovery data from backup files.

Code quality maintenance:

1. Add configurable logs.
  Notes: this may add a completion log system for casnode using [zap](https://github.com/uber-go/zap).
2. More friendly error handling instead of panic.
  Notes: this may be built on a well-established logging system
3. Add some commits for code.
  Notes: This could be finished when you read the code.
4. Improve performance, such as SQL query, cache, etc.

And other [issues](https://github.com/casbin/casnode/issues) that may arise during the time.

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

Another work is to develop jCasbin' middleware for the popular Java web frameworks except Spring such as Play, like how we did it for Golang: https://casbin.org/docs/en/middlewares

#### Expected outcomes

Some issues to work on:

1. Make a Play Framework middleware: https://github.com/casbin/jcasbin/issues/104
2. Sync more features about "in" special grammar from Go-Casbin: https://casbin.org/docs/en/syntax-for-models#special-grammer
3. Make a default implementation of WatcherEx and migrate Watcher to WatcherEx : https://github.com/casbin/casbin/issues/943
4. Provide more offical  adapter/watcher like Golang: https://casbin.org/docs/en/watchers.
5. Fix the bug about ClassCastException for Strings within grouping fucntions: https://github.com/casbin/jcasbin/issues/254
6. Help solve issues for the 1st-party and 3rd-party middlewares

#### Skills required/preferred

1. Java
2. Other languages that Casbin is written with

#### Mentors

[Yang Tang](https://github.com/tangyang9464), Casbin member, [Zhengjin Fang](https://github.com/fangzhengjin), Casbin member, [Yang Luo](https://github.com/hsluoyz), Casbin founder

#### Expected size of project (175 hour or 350 hour)

175 hour

#### Rating (Easy, Medium or Hard)

Medium



### Casbin for .NET

#### Description

Casbin.NET v2 will release quickly. The new architecture provides excellent performance and flexible scalability and prepares for the addition of more imaginative and exciting features.

#### Expected outcomes

1. Support more features:
- a. Feature Request: subjectPriority(https://
github.com/casbin/Casbin.NET/issues/238)
- b. Support "in" special grammar(https://github.com/casbin/Casbin.NET/issues/198)
- c. Validate and compile matcher when loading model(https://github.com/casbin/Casbin.NET/issues/228)
- d. Improve the unit test coverage(https://github.com/casbin/Casbin.NET/issues/151)
2. Enhance ecosystem:
- a. Support ASP.NET Core and Blazor (Enhance [Casbin.AspNetCore](https://github.com/casbin-net/casbin-aspnetcore))
- b. Provide Offical Redis adaptor/watcher.

#### Requirements

1. .NET/C#
2. ASP.NET Core

#### Mentor

[Sagilio](https://github.com/sagilio), Casbin member

#### Expected size of project (175 hour or 350 hour)

175 hour

#### Rating (Easy, Medium or Hard)

Medium



### Casdoor for .NET

#### Description

Casdoor is a UI-first centralized authentication / Single-Sign-On (SSO) platform based on OAuth 2.0 / OIDC. We hope to provide a comprehensive and powerful SDK to make .NET application integrate with it easily.

#### Expected outcomes

1. Implement SDK:
- a. Implement Casdoor.Client to call Casdoor APIs easily.
- b. Implement Casdoor.AspNetCore to integrate ASP.NET Core with Casdoor.
- c. Implement Casdoor.Native to integrate WPF or Maui with Casdoor
2. Implement Samples:
- a. Provide ASP.NET Core Web API, MVC and Blazor samples with the SDK.
- b. Provide WPF or Maui smaples with the SDK.

#### Requirements

1. .NET/C#
2. ASP.NET Core
3. WPF or Maui

#### Mentor

[Sagilio](https://github.com/sagilio), Casbin member

#### Expected size of project (175 hour or 350 hour)

175 hour

#### Rating (Easy, Medium or Hard)

Medium



### Casbin for Cloud Native

#### Description

Currently, Casbin has limited adaptability in the cloud-native field. We hope to use kubebuilder 3.x to refact the [k8s-authz](https://github.com/casbin/k8s-authz) and provide CRD based model and policy management. Enhance model parse to compatible with k8s better.

#### Expected outcomes

1. Refact k8s-authz
- a. Porvide predefined `r` or `p` tokens and custom function for k8s.
- b. Provide CRD based model and policy management.
- c. Provide Client and helm integration.
- d. Make kubesphere-athz compatible with the new k8s-authz.
2. Enhance ecosystem:
- a. Implement Casbin middleware for [Dapr](https://docs.dapr.io/reference/components-reference/supported-middleware/)
- b. Explore more usage scenarios on Cloud Native.

#### Requirements

1. Golang
2. K8s ([kubebuilder](https://book.kubebuilder.io/)) and Cloud Native
3. Service Mesh and [Dapr](https://dapr.io/)

#### Mentor

[Sagilio](https://github.com/sagilio), Casbin member, [Yang Luo](https://github.com/hsluoyz), Casbin founder

#### Expected size of project (175 hour or 350 hour)

350 hour

#### Rating (Easy, Medium or Hard)

Hard



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

Improving the user experience of Node-Casbin will be our focus.

#### Expected outcomes

Some issues to work on:

- Sync GetImplicitResourcesForUser method(https://github.com/casbin/node-casbin/issues/344)

- Sync UpdateGroupingPolicy and UpdateNamedGroupingPolicy method(https://github.com/casbin/node-casbin/issues/324)

- Improve built-in method of matcher(https://github.com/casbin/node-casbin/issues/332)

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

[PHP-Casbin](https://github.com/php-casbin/php-casbin) An authorization library that supports access control models like ACL, RBAC, ABAC in PHP .

#### Expected outcomes

1. Add `AddPermissionsForUser` API.
2. Add cache for `g` function, refer to: https://github.com/casbin/casbin/blob/master/util/builtin_operators.go#L333.
3. Integrate laravel's [Gates](https://laravel.com/docs/9.x/authorization#gates) in [Laravel-Authz](https://github.com/php-casbin/laravel-authz).
4. Implementation of [WatcherEx](https://casbin.org/docs/en/watchers#watcherex), basic Watcher: [Swoole Redis watcher](https://github.com/php-casbin/swoole-redis-watcher) [Workerman Redis watcher](https://github.com/php-casbin/workerman-redis-watcher).
5. Implement [propel-adapter](https://github.com/php-casbin/propel-adapter), [Propel](http://propelorm.org/) is a highly customizable and blazing fast ORM library for PHP.
6. Consistent with the functionality of [Casbin Core Engine (Golang)](https://github.com/casbin/casbin).
7. Bug fixes in [issues](https://github.com/php-casbin/php-casbin/issues), improve some [extensions](https://github.com/php-casbin).

#### Skills required/preferred

1. PHP
2. Casbin

#### Mentors

[Jon Lee](https://github.com/leeqvip), Casbin member

#### Expected size of project (175 hour or 350 hour)

350 hour

#### Rating (Easy, Medium or Hard)

Medium



### Casbin for Python

#### Description

1. At present, compared to Casbin for Golang, `Pycasbin` is not very perfect, especially the lack of RBAC API, so we hope that `Pycasbin` can fully implement the function of Casbin (Go).
2. `PyCasbin`'s adaptation to various frameworks, such as `Django`, `Tornado`, etc.

Pycasbin organization: https://github.com/pycasbin

#### Expected outcomes

1. Implement [redis-adapter](https://github.com/pycasbin/redis-watcher).
2. Implement [etcd-adapter](https://github.com/pycasbin/etcd-watcher).
3. Improve performance for `enforce()`.
4. Complete implementation of PyCasbin-on-CPP.
5. Reimplement the implementation of Pycasbin in `Django`, introduce Django's `Middleware`, `Caching`, `Logging`, and integrate the Django authentication system, and existing plugins: [django-casbin](https://github.com/pycasbin/django-casbin) [django-orm-adapter](https://github.com/pycasbin/django-orm-adapter).

Some issues to work on: https://github.com/casbin/pycasbin/issues

#### Skills required/preferred

1. Python
2. Other languages that Casbin is written with

#### Mentors

[Jon Lee](https://github.com/leeqvip), Casbin member

#### Expected size of project (175 hour or 350 hour)

350 hour

#### Rating (Easy, Medium or Hard)

Medium



### Casbin.js

#### Description

Quite a lot of users want to use Casbin to control web frontend UI elements, like:

1. Some tabs are only visible to admin users.
2. Some buttons should be grayed-out for users with no permission to click them.
3. A list can only show filtered items based on a user's permission rights.

Over time we have made node-casbin a cross-platform Javascript permission control library and have called the new library casbin.js. The next step is to refactor node-casbin to a casbin.js-based wrapper. Another possible idea is create a `browser-casbin` for front-end developers with front-end friendly api. 

The current progress is: https://github.com/casbin/casbin.js

Currently, we still lack the middlewares for Angular, React and Vue. These new JS frameworks are very popular and making middlewares for them will boost our usage from their population.

#### Expected outcomes

1. Sync progress with node-casbin
2. Update vue-authz and react-authz to new casbin.js.
3. Refactor node-casbin to casbin.js wrapper.

#### Skills required/preferred

1. Typescript
2. Node-Casbin
3. Vue or React development experience
3. At least one backend language like Golang

#### Mentors

[Xinyu Zhou](https://github.com/Zxilly), Casbin member, [Yang Luo](https://github.com/hsluoyz), Casbin founder

#### Expected size of project (175 hour or 350 hour)

350 hour

#### Rating (Easy, Medium or Hard)

Hard



### Casbin for Lua

#### Description

Port Golang Casbin into Lua. We call it `lua-casbin`. It should work on the Nginx + OpenResty stack. Most of Casbin's functionalities (for example 90%) should work.

Nginx is now the most popular HTTP server in the world. OpenResty is a web platform based on Nginx which can run Lua scripts using its LuaJIT engine. Nginx + OpenResty are usually used in edge computing and authorization is a real need for its scenario. Lua-Casbin will help Nginx and OpenResty users on checking permissions of the coming HTTP request.

The current progress is: https://github.com/casbin/lua-casbin

#### Expected outcomes

1. Implementation of `Watcher`, `Watcher` ensures policy consistency in multiple Casbin instances.
2. Add cache for `g` function, refer to: https://github.com/casbin/casbin/blob/master/util/builtin_operators.go#L333.
3. Add `AddPermissionsForUser` API.
4. Add LoadPolicyArray() to load policy from array
5. Improve performance for `enforce()`.
6. Implement the built-in function `keyMatch5`.
7. Fixes and refinements to lua-casbin's [extensions](https://github.com/casbin-lua).

#### Skills required/preferred

1. Nginx
2. OpenResty
1. Lua
2. Golang (only need to read code)

#### Mentors

[Jon Lee](https://github.com/leeqvip), Casbin member, [Yang Luo](https://github.com/hsluoyz), Casbin founder

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

### Casbin Mesh

#### Description

Last summer, we started a new project called Casbin-Mesh which allows us to deploy the Casbin to many nodes using the raft consensus algorithm to handle rapidly increasing data, which raises the throughout of read-only transactions.


#### Expected outcomes

However, there are still many works that need to be done.

1. The bottleneck of memory data structure
- Reconstruction the memory data model
  - We are going to use the buffer pool manager handling very large data that over then RAM
2. The overhead of full-table scanning
- Indexes
  - Create indexes for all policies
  - Use Indexes to avoid full-table scanning
- Basic query optimization
3. Transactions Implementation

#### Skills required/preferred

1. Golang
2. At least you need to be familiar with the basic concepts of the query optimization, indexing (hash index, B+ tree index), multi-version concurrency control.
2. (preferred) Had taken database lectures (Such as CMU 15-445 etc.) 



#### Mentors

[WenyXu](https://github.com/WenyXu), Casbin member, [Yang Luo](https://github.com/hsluoyz), Casbin founder

#### Expected size of project (175 hour or 350 hour)

350 hour

#### Rating (Easy, Medium or Hard)

Hard