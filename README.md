# dynamic-page-headers

## Step 1: Create the folder that you want to connect to your pages.

This folder will contain the ID in which you give to our shortcode. 


## Step 2: Upload the images into this folder, with names correlating the page titles.

Ex: about-us.jpg

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

