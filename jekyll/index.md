---
layout: archive
url: /
title: "Latest Posts"
image: JeepSilverton2015.jpg # test
---
# Big Ol' Words Right Here!

``` c++
// test
#define YASS 2
#include<iostream.h>

int main() {
	return 0;
}

```

Did it do a thing?  
It didn't do a thing in the generated html but this...
{% highlight c++ linenos %}
#define ATHING 8
#include<string>
using std::cout;

volatile unsigned int num;

int main() {
	//do a thing
	return 0;
}
{% endhighlight %}

should?

<div class="tiles">
{% for post in site.posts.playthings %}
	{% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles -->
