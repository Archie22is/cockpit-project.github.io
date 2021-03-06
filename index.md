---
title: Cockpit Project
layout: essential
class: front-page
---

{% include page_header.html %}

{% comment %}
##### Content #####
First we set up & capture the content, then we render it in the scaffolding below.
{% endcomment %}


{% capture intro-left %}
## ![Cockpit](/images/site/cockpit-logo.svg)
{:.logo}

<span aria-hidden="true" role="presentation">Cockpit</span> is a server manager that makes it easy to administer your GNU/Linux servers via a web browser.

{% endcapture %}

{% capture intro-right %}
[![Docker screenshot]({{ site.baseurl }}/images/site/screenshot-docker.png)]({{ site.baseurl }}/images/site/screenshot-docker.png){:.screenshot.zoom}
{% endcapture %}


{% capture blurb_easy %}
[![Storage screenshot]({{ site.baseurl }}/images/site/screenshot-storage.png)]({{ site.baseurl}}/images/site/screenshot-storage.png){:.screenshot.zoom}
### Easy to use
Cockpit makes Linux discoverable, allowing sysadmins to easily perform tasks such as starting containers, storage administration, network configuration, inspecting logs and so on.
{% endcapture %}


{% capture blurb_interactive %}
[![Network screenshot]({{ site.baseurl }}/images/site/screenshot-network.png)]({{ site.baseurl }}/images/site/screenshot-network.png){:.screenshot.zoom}
### No interference
Jumping between the terminal and the web tool is no problem. A service started via Cockpit can be stopped via the terminal. Likewise, if an error occurs in the terminal, it can be seen in the Cockpit journal interface.
{% endcapture %}


{% capture blurb_multiserver %}
[![Dashboard screenshot]({{ site.baseurl }}/images/site/screenshot-dashboard.png)]({{ site.baseurl }}/images/site/screenshot-dashboard.png){:.screenshot.zoom}
### Multi-server
You can monitor and administer several servers at the same time. Just add it easily and your server will look after its buddies.
{% endcapture %}


{% capture footer_links_1 %}
About Cockpit
: [Project Ideals and Goals](ideals.html)
: [Cockpit Blog](blog)
: [Search this site](search.html)
{% endcapture %}

{% capture footer_links_2 %}
[Running Cockpit](running.html)
: [Deployment guide](guide/latest/guide.html)
: [Feature internals](guide/latest/features.html)
: [Release Notes and Videos](blog/category/release.html)
: [File a bug in the issue tracker](https://github.com/cockpit-project/cockpit/issues)
{% endcapture %}

{% capture footer_links_3 %}
[Contributing](https://github.com/cockpit-project/cockpit/wiki/Contributing)
: [Get the source](https://github.com/cockpit-project/cockpit)
: [Join the mailing list](https://lists.fedorahosted.org/archives/list/cockpit-devel@lists.fedorahosted.org/)
: [IRC #cockpit on Freenode.net](irc://irc.freenode.net:6667/cockpit)
: [Developer tutorials](blog/category/tutorial.html)
: [Developer API reference](guide/latest/development.html)
{% endcapture %}


{% comment %}
##### Scaffolding #####
{% endcomment %}

<div id="page-wrap" role="main">
  <section class="intro">
    <div class="wrapper"><div class="grid-center-noBottom">
      <div class="side-left col-7_md-11">{{ intro-left  | markdownify }}</div>
      <div class="side-right col-5_md-11-bottom"><div class="intro-image">{{ intro-right | markdownify }}</div></div>
    </div></div>
  </section>

  <section class="wrapper">
    <section class="grid-center_md-2_sm-1 blurbs">
      <div class="col">{{ blurb_easy        | markdownify }}</div>
      <div class="col">{{ blurb_interactive | markdownify }}</div>
      <div class="col">{{ blurb_multiserver | markdownify }}</div>
    </section>
  </section>
</div>

<footer class="footerlinks">
  <div class="wrapper"><div class="grid-wrap-3_md-2_xs-1">
    <div class="col">
      {{ footer_links_1 | markdownify }}
    </div>
    <div class="col">
      {{ footer_links_2 | markdownify }}
    </div>
    <div class="col">
      {{ footer_links_3 | markdownify }}
    </div>
  </div></div>
</footer>
{% include page_footer.html %}

<script>
<!--
$(function(){
  $(document).on('click', 'a.screenshot.zoom', function(ev){
    desc = $('img', this).attr('alt');
    code = $('<div id="imagePreview" class="image-container zoom-out"><img src="' + this.href + '" alt="' + desc + '"><p>' + desc + "<\/p><\/div>");
    $('body').append(code);
    ev.preventDefault();
  }).on('click', '#imagePreview', function(ev){
    $(this).fadeOut(200, function(){
      $(this).remove();
    });
  });
});
//-->
</script>
