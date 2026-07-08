---
layout: contact
title: Contact
permalink: /contact/
description: Leave a message using the Cusdis contact thread.
---

<p class="contact-branding">Comments powered by Cusdis</p>

<div
  id="cusdis_thread"
  data-host="https://cusdis.com"
  data-app-id="acbd279e-b809-48f9-8c9b-f0ea5ff0164e"
  data-page-id="contact"
  data-page-url="{{ page.url | absolute_url }}"
  data-page-title="{{ page.title | escape }}"
></div>
<script async defer src="https://cusdis.com/js/cusdis.es.js"></script>
<script>
  (function () {
    var thread = document.getElementById('cusdis_thread');
    if (!thread) return;

    function hideIframeScrollbars() {
      var iframe = thread.querySelector('iframe');
      if (!iframe) return false;

      iframe.setAttribute('scrolling', 'no');
      iframe.style.overflow = 'hidden';
      iframe.style.display = 'block';
      return true;
    }

    if (hideIframeScrollbars()) return;

    var observer = new MutationObserver(function () {
      if (hideIframeScrollbars()) {
        observer.disconnect();
      }
    });

    observer.observe(thread, { childList: true, subtree: true });
  })();
</script>
