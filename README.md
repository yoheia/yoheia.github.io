# About Me
This is my portfolio site

## Environment

* This site is Made by Hugo 
* GitHub Pages
	* yoheia.github.io - Settings - GitHub Pages - Source 
		* Branch: gh-pages
		* /(root)
* GitHub Branches
	* gh-pages: Web site contents built by hugo
	* develop: Hugo Themes "Academic" (https://themes.gohugo.io/academic/)

## Install

### Go

```
# for macOS
$ brew install go
```

### Hugo 0.53

* Dwonload hugo_extended_0.53_macOS-64bit.tar.gz
 from https://github.com/gohugoio/hugo/releases/tag/v0.53

```
# for macOS
$ tar xfvz hugo_extended_0.53_macOS-64bit.tar.gz
$ mkdir -p /usr/local/Cellar/hugo/0.53/
$ cd hugo_extended_0.53_macOS-64bit
$ cp -pr * /usr/local/Cellar/hugo/0.53/
```

* Add following lines to ~/.bash_profile

```
# go
export PATH=$PATH:/usr/local/go/bin

# hugo
export PATH=$PATH:/usr/local/Cellar/hugo/0.53
```

* ~/.bash_profile

```
$ source ~/.bash_profile
```

## How to build

* Download web site contents

```
$ git clone -b develop https://github.com/yoheia/yoheia.github.io.git
$ cd yoheia.github.io
$ git submodule update --init --recursive
```

* Build

```
$ cd yoheia.github.io
$ hugo
```

* View at local environment (http://localhost:1313/)

```
$ hugo server
```

* Update contents, build, deploy

```
$ cd yoheia.github.io
$ git add .
$ git commit -m ''
$ git push origin develop
$ hugo
$ cd public
$ git add .
$ git commit -m ''
$ git push origin gh-pages
```
