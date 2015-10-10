
[![](https://i.imgur.com/8I289mA.png)](http://bladejava.com)

[![@biezhi on weibo](https://img.shields.io/badge/weibo-%40biezhi-red.svg)](http://weibo.com/u/5238733773)
[![Hex.pm](https://img.shields.io/hexpm/l/plug.svg)](http://www.apache.org/licenses/LICENSE-2.0.html)
[![Build Status](https://api.travis-ci.org/biezhi/blade.svg?branch=master)](https://travis-ci.org/biezhi/blade)
[![release](https://img.shields.io/maven-central/v/com.bladejava/blade-core.svg)](http://search.maven.org/#search%7Cga%7C1%7Cg%3A%22com.bladejava%22)

[中文](https://github.com/biezhi/blade/blob/master/README_CN.md)

# What Is Blade?
`blade` is a lightweight MVC framework. It is based on the principles of simplicity, relevance and elegance. 
If you like it, can be [Star and Fork](https://github.com/biezhi/blade), thanks!

# Features
* [x] Lightweight. The code is simple and structure is clear
* [x] Modular (you can choose which components to use)
* [x] Support plug-in extension mechanism
* [x] Restful style routing interface
* [x] Multiple configuration files support (currently properties, json and coding)
* [x] Eembed jetty server and template engine support
* [x] Support jdk1.6 or higher version

# Overview

* Simplicity. The design is simple, easy to understand and doesn't introduce many layers between you and the standard library. It is a goal of the project that users should be able to understand the whole framework in a single day.

* Relevance. `blade` doesn't assume anything. We focus on things that matter, this way we are able to ensure easy maintenance and keep the system well-organized, well-planned and sweet.

* Elegance. `blade` uses golang best practises. We are not afraid of heights, it's just that we need a parachute in our backpack. The source code is heavily documented, any functionality should be well explained and well tested.

# Getting started
To get started, first [include the Blade library](http://bladejava.com) and then create a class with a main method like this:
```java
public class App extends Bootstrap {
	
	@Override
	public void init() {}
	
	public static void main(String[] args) throws Exception {
		Blade blade = Blade.me();
		blade.get("/").run(request, response) -> {
			response.html("<h1>Hello blade!</h1>");
			return null;
		});
		blade.app(App.class).listen(9001).start();
	}
}
```
Run it and point your browser to http://localhost:9001. There you go, you've just created your first Blade app!

OK, all this may seem simple, refer to the guidelines for use more ready-made examples for your reference:

+ [hello project](https://github.com/bladejava/hello)
+ [api docs](http://bladejava.com/apidocs/)
+ [user guide](https://github.com/biezhi/blade/wiki)
+ [some examples](https://github.com/bladejava)

## Plan

	1. Improve the document
	2. Add configurable log
	3. Complete the Java China BBS
	4. Maintain and optimize the code
	
## Update

[update log](https://github.com/biezhi/blade/blob/master/UPDATE_LOG.md)

## licenses

Blade Framework based on the [Apache2 License](http://www.apache.org/licenses/LICENSE-2.0.html)

## Contact

Blog:[https://biezhi.me](https://biezhi.me)

Mail: biezhi.me#gmail.com

QQ Group: [1013565](http://shang.qq.com/wpa/qunwpa?idkey=932642920a5c0ef5f1ae902723c4f168c58ea63f3cef1139e30d68145d3b5b2f)
