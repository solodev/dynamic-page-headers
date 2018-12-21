# dynamic-page-headers

## Prerequisites
<ul>
	<li><a target="_blank" href="https://getbootstrap.com/">Boostrap 4</a></li>
</ul>


## Step 1: Create the folder in which you want to connect it's images to your pages.

This folder will contain the ID in which you give to the shortcode. 


## Step 2: Upload the images into this folder, with names correlating the page titles.

Ex: about-us.jpg

It is also recommended to add a default.jpg, as that will be the fallback on any page names without correlated images.

## Step 3: Create a hero.tpl file with the shortcode.

Your markup should look similar to this:

```
<header class="position-relative py-5 d-flex align-items-center text-center text-md-left" style='background: url([get_asset_from_folder path_id="64"]) center/cover no-repeat'>

  <div class="w-100 py-5">
    <div class="container">
      <div class="row">
        <div class="col-md-8">
          <h1 class="text-uppercase text-white mb-0">[page_title]</h1>
          <p class="mb-0">[page_description]</p>
        </div>
      </div>
    </div>
  </div>
</header> 
```
## Step 4: Use this hero.tpl file in any page with a correlated image.

The shortode will dynamically grab any image with the name correlated. If there is no image, it will look for an image from its parent page.

Example: /about-us/team.stml will first look for team.jpg, then for about-us.jpg. If neither of these are found, it will default to the default.jpg
