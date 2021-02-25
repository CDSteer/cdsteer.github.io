---
layout: page
permalink: /newsletter/
title: newsletter
description: Join my newsletter.
nav: true
---

<!-- For now, this page is assumed to be a static description of your courses. You can convert it to a collection similar to `_projects/` so that you can have a dedicated page for each course. -->

<div id="revue-embed" class="form-group">
  <form action="https://www.getrevue.co/profile/cdsteer/add_subscriber" method="post" id="revue-form" name="revue-form"  target="_blank">
  <div class="revue-form-group">
    <label for="member_email">Email address</label>
    <input class="revue-form-field form-control" placeholder="Your email address..." type="email" name="member[email]" id="member_email">
  </div>

  <div class="revue-form-group">
    <label for="member_first_name">First name <span class="optional">(Optional)</span></label>
    <input class="revue-form-field form-control" placeholder="First name" type="text" name="member[first_name]" id="member_first_name">
  </div>

  <div class="revue-form-group">
    <label for="member_last_name">Last name <span class="optional">(Optional)</span></label>
    <input class="revue-form-field form-control" placeholder="Last name" type="text" name="member[last_name]" id="member_last_name">
  </div>

  <div class="revue-form-actions">
    <input type="submit" value="Subscribe" name="member[subscribe]" id="member_submit" class="btn btn-primary">
  </div>
