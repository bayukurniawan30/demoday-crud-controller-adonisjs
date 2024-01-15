---
theme: purplin
class: text-center
highlighter: prism
lineNumbers: true
info: |
  ## Taksu Demo Day 72
drawings:
  persist: false
title: CRUD Controller in AdonisJS
---

<div class="w-full flex items-center justify-center">
  <img src="/img/adonisjs-logo.png" class="h-20 mb-8" />
</div>

## CRUD Controller in AdonisJS

Taksu Demo Day #72

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Next <carbon:arrow-right class="inline"/>
  </span>
</div>

<BarBottom  title="Taksu Demo Day #72">
  <Item text="Bayu Kurniawan">
    <carbon:user-avatar />
  </Item>
</BarBottom>


---

# What is AdonisJS?

<style>
  .general-desc {
    line-height: 2rem !important;
  }
</style>

<div v-click class="text-2xl text-white mt-10">
<p class="general-desc">
AdonisJS is a fully featured web framework for Node.js. It has everything you need to create a fully functional web app or an API server.</p>

<p class="general-desc">
It also has built-in authentication, validator, template engine, ORM, and CLI command.
</p>

</div>

<BarBottom  title="Taksu Demo Day #72">
  <Item text="Bayu Kurniawan">
    <carbon:user-avatar />
  </Item>
</BarBottom>

<!-- 
Put comment here
-->

---

# What is CRUD?

<style>
  .general-desc {
    line-height: 2rem !important;
  }
</style>

<div v-click class="text-2xl text-white mt-10">
<p class="general-desc">
CRUD stands for Create, Read, Update and Delete. We make all this process in one controller to make REST API.</p>

<p class="general-desc">
In a controller, Create use <strong>store()</strong> function, Read use <strong>index()</strong> and <strong>show()</strong> function, Update use <strong>update()</strong> function, and Delete use <strong>destroy()</strong> function.
</p>

</div>

<BarBottom  title="Taksu Demo Day #72">
  <Item text="Bayu Kurniawan">
    <carbon:user-avatar />
  </Item>
</BarBottom>

<!-- 
Put comment here
-->

---


# Why Use CRUD Controller?

<style>
  .general-desc {
    line-height: 2rem !important;
  }
</style>

<div v-click class="text-2xl text-white mt-10">
<p class="general-desc">
The goals of using CRUD controller is to simplify and minimize code writing, make your code maintainable, and in the same time, save your time of writing the same code in different file.</p>

<p class="general-desc">
We can create a parent class for CRUD controller, then the child class just extend it, to have the same functions. It really same hundred lines of code.
</p>

</div>

<BarBottom  title="Taksu Demo Day #72">
  <Item text="Bayu Kurniawan">
    <carbon:user-avatar />
  </Item>
</BarBottom>

<!--  
Put comment here
-->

---

# Routing


<div class="text-2xl text-white mt-10">
Below is the code of CRUD Controller written in AdonisJS
</div>

```ts {1|2|3|5|6|7|8|9|all}
export default abstract class CrudController {
  protected abstract model: typeof BaseModel
  protected relationships

  public async index({ request, response }: HttpContextContract) { }
  public async show({ request, response }: HttpContextContract) { }
  public async store({ request, response }: HttpContextContract) { }
  public async update({ request, response }: HttpContextContract) { }
  public async destroy({ request, response }: HttpContextContract) { }
  ...
}

```

<div class="text-2xl text-white">In child controller, example use <strong>UsersController</strong></div>

```ts {1|2|3}
export default class UsersController extends CrudController {
  protected model = User
  protected relationships = ['profile']
}

```

<BarBottom  title="Taksu Demo Day #72">
  <Item text="Bayu Kurniawan">
    <carbon:user-avatar />
  </Item>
</BarBottom>

<!--
Put comment here
-->

---

# Code Session

<div class="text-2xl text-white mt-10">
Ok now we continue to code session
</div>

<BarBottom  title="Taksu Demo Day #72">
  <Item text="Bayu Kurniawan">
    <carbon:user-avatar />
  </Item>
</BarBottom>

---

# Real Life Example

<div class="text-2xl text-white mt-10">
To see it in real life example, you can see my repo at <a href="https://github.com/bayukurniawan30/adonisjs-headless-api" target="_blank">https://github.com/bayukurniawan30/adonisjs-headless-api</a>. It's a simple project that use CRUD controller with AdonisJS.
</div>

<BarBottom  title="Taksu Demo Day #72">
  <Item text="Bayu Kurniawan">
    <carbon:user-avatar />
  </Item>
</BarBottom>

---


# What's Next?

<div v-click class="text-2xl text-white mt-10">
Next demo day, will be Authentication in AdonisJS, so don't miss it!
</div>
