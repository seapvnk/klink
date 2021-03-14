

 # klink

 A static site generator made in shell script




<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project
Klink is an experimental static site generator made in shell for small projects. The syntax is just html with block of codes where you can write bash.


### Built With

This section should list any major frameworks that you built your project using. Leave any add-ons/plugins for the acknowledgements section. Here are a few examples.
* bash script


<!-- GETTING STARTED -->
## Getting Started

This is an example of how you may give instructions on setting up your project locally.
To get a local copy up and running follow these simple example steps.

### Prerequisites
You just need your OS and terminal

* linux
* bash

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/seapvnk/klink.git
   ```
2. Remove the repo stuff
   ```sh
   rm -rf .git README.md LICENSE
   ```

<!-- USAGE EXAMPLES -->
## Usage
The usage is simple, if you have some experience in templates engine you'll be fine.
```html
<h2>Image gallery</h2>
{? for img in $(ls images); do ?}
    <img src="images/{? echo "$img" ?}"> 
{? done ?}
```

The markup is done in HTML and the script is executed between `{?` and `?}`, this syntax reminds ears. There's just shell script, 
so you can use anything you want. The output of commands written between the "ears" go to html document generated.
```shell
<pre>
{? figlet MY CODING BLOG ?}
</pre>

<h3> hello world example </h3>

<code>
<pre>
{? cat examples/hello-world.c ?}
</pre>
</code>
```

<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.
