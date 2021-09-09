---
layout: home
---

<div class="w-full bg-white p-12 py-24 md:py-28 ">
  <div class="header flex items-end justify-between mb-12">
    <div class="title">
      <p class="text-4xl font-bold text-gray-800 mb-4">
          Success Stories
      </p>
      <p class="font-light text-gray-400">
          Do you have a success story to share?
          <br />
          Built a cool app while at Hacker Hours, met a co-founder, or knocked out a pesky bug?
          <br />
          <a class="text-indigo-500 text-md font-medium"
            href="https://github.com/afeld/hackerhours.org/issues/new">Let us know!</a>
      </p>
    </div>
  </div>

  <div class="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-3 gap-12 my-5">
    {%- for post in site.posts -%}
    <div class="overflow-hidden shadow-lg rounded-lg h-90 w-60 md:w-80 cursor-pointer m-auto">
      <div class="text-center mb-4 opacity-90">
        {%- if post.img -%}
        <img alt="avatar" src="/images/success/{{ post.img }}"
          class="mx-auto object-cover rounded-full h-40 w-40 "/>
        {%- endif -%}
      </div>
      <div class="bg-white dark:bg-gray-800 w-full p-4">
        <p class="text-gray-800 dark:text-white text-xl font-medium mb-2">
          {{ post.title | escape }}
        </p>
        <p class="text-gray-400 dark:text-gray-300 font-light text-md">
          <div class="mt-6 post-content">{{ post.excerpt }}</div>
          <!-- <div class="mt-10">
            <a class="text-blue-500 uppercase text-sm tracking-wide font-black content-link" 
            href="{{ post.url | relative_url }}">Read More</a>
          </div> -->
        </p>
        <div class="flex items-center mt-4">
          <div class="flex flex-col justify-between ml-4 text-sm">
            <p class="text-gray-400 dark:text-gray-300">
              {{ post.date | date: "%b %-d, %Y" }}
            </p>
          </div>
        </div>
      </div>
    </div>
    {%- endfor -%}
  </div>
</div>
