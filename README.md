你好！
很冒昧用这样的方式来和你沟通，如有打扰请忽略我的提交哈。我是光年实验室（gnlab.com）的HR，在招Golang开发工程师，我们是一个技术型团队，技术氛围非常好。全职和兼职都可以，不过最好是全职，工作地点杭州。
我们公司是做流量增长的，Golang负责开发SAAS平台的应用，我们做的很多应用是全新的，工作非常有挑战也很有意思，是国内很多大厂的顾问。
如果有兴趣的话加我微信：13515810775  ，也可以访问 https://gnlab.com/，联系客服转发给HR。
[![Go Report Card](https://goreportcard.com/badge/github.com/zupzup/calories)](https://goreportcard.com/report/github.com/zupzup/calories)

# blog-generator

A static blog generator using a configurable GitHub repository as a data-source. The posts are written in markdown with yml metadata attached to them. [This](https://github.com/zupzup/blog) is an example repo for the blog at [https://zupzup.org/](https://zupzup.org/).

## Features

* Listing
* Sitemap Generator
* RSS Feed
* Code Highlighting
* Archive 
* Configurable Static Pages 
* Tags 

## Installation

```bash
go get github.com/zupzup/blog-generator
```

## Usage

Just execute

```bash
blog-generator
```

in this repository's root directory.

## Customization

### Configure the CLI

Set the following constants in `cli/cli.go`:

```go
// data source for the blog
const RepoURL string = "git@github.com:username/repo.git"
// folder to download the repo into
const TmpFolder string = "./tmp"
// output folder
const DestFolder string = "./www"
```

### Configure the Generator

Set the following constants in `generator/generator.go`
```go
// url of the blog
const blogURL = "https://www.someblog.com"
// blog language
const blogLanguage = "en-us"
// blog description
const blogDescription = "some description..."
// date format
const dateFormat string = "02.01.2006"
// main Template
const templatePath string = "static/template.html"
// blog title
const blogTitle string = "my Blog's Title"
// displayed posts on landing page
const numPostsFrontPage int = 10
```

You can define and configure the different generators in the `runTasks` function within `generator/generator.go`.

### Templates

Edit templates in `static` folder to your needs.

## Example Blog Repository

[Blog](https://github.com/zupzup/blog)
