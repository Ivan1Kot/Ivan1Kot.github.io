---
# An instance of the Contact widget.
# Documentation: https://docs.hugoblox.com/getting-started/page-builder/
widget: contact

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 50

title: Есть вопросы?
subtitle: Напишите мне

content:
  # Automatically link email and phone or display as text?
  autolink: true

design:
  columns: '1'
---

{{ $.Scratch.Add "labelClasses" "f6 b db mb1 mt3 sans-serif mid-gray" }}
{{ $.Scratch.Add "inputClasses" "w-100 f5 pv3 ph3 bg-light-gray bn" }}

{{<form class="black-80 sans-serif" accept-charset="UTF-8" action="{{ .Get "action" }}" method="POST" role="form">

<label class="{{ $.Scratch.Get "labelClasses" }}"  for="name">{{ i18n "yourName" }}</label>
<input type="text" id="name" name="name" class="{{ $.Scratch.Get "inputClasses" }}"  required placeholder=" "  aria-labelledby="name"/>

<label class="{{ $.Scratch.Get "labelClasses" }}" for="email">{{ i18n "emailAddress" }}</label>
<input type="email" id="email" name="email" class="{{ $.Scratch.Get "inputClasses" }}"  required placeholder=" "  aria-labelledby="email"/>
   <div class="requirements f6 gray glow i ph3 overflow-hidden">
     {{ i18n "emailRequiredNote" }}
   </div>

<label class="{{ $.Scratch.Get "labelClasses" }}" for="message">{{ i18n "message" }}</label>
<textarea id="message" name="message" class="{{ $.Scratch.Get "inputClasses" }} h4" aria-labelledby="message"></textarea>
   <div class="g-recaptcha" data-sitekey="6LcqZZgqAAAAAFZeDPRo1CQJ7xhuXd-DztUVisyL"></div>
   <input class="db w-100 mv2 white pa3 bn hover-shadow hover-bg-black bg-animate bg-black" type="submit" value="{{ i18n "send" }}" />

</form>}}

