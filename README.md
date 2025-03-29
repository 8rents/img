# img `GH Image Share`

> *This is a repo that's designed to allow public hotlinking of images from GitHub. I don't believe that this is against their TOS so I'm going to keep using it until they tell me to knock it off.*
>
> *Note that this is the [images (`i`) branch](https://github.com/8rents/_/tree/i) of an older [repo (`_`) that was named with an underscore](https://github.com/8rents/_). It was used to share all different file types, with each different file type being stored on a separate branch. The image branch of the `_` repo was called `i`. Since this repo is only going to be used to share images, we'll name the main branch `share`. Conversely we will also have a branch named `private`.*
---

## Documentation Table of Contents:

- [**`1.1` Branches**](#)    
  *An overview of the branches that this repository uses*
- [**`2.1` How to Hot Link an image**](#)     
  *A quick tutorial on how to upload and hot link an image using this repository*
- [**`2.2` Making a snippet**](#)    
  *Understanding how image URLs are constructed and how to make a snippet to quickly embed images from this repo*
- [**`3.1` File Guidelines**](#)    
  *A couple of simple rules for consistancy & simplicity when using this repo*
- [**`3.2` Preffered File Types**](#)    
  *Which image file types to use and not use and which to preffer and when*
- [**`4.1` Directory Structure**](#)   
  *The base set of folders that I use for this repo for keeping track of things*
- [**`5.1` Tracking an images lineage and history**](#)    
  *A system for keeping track of an image and all of the edits made to it from creation or download to each of the versions and from which they came from*

## Branches

This repo has one primary branch (`s` branch, short for "share") that is used to host and share all image media. 


### Primary Branch

- **`s` (share) [primary]** - The main branch used to share & host images publicly so they can be hot linked.

### Other Branches

The other two branches which will be much less used than `share` are:

- **`e` (edit)** - A branch that is used to host host all edit filetypes like `.psd` files or `.ai` files
- **`b` (blank)** - A tempalte branch that is used to create new blank branches. Contains only a `README.md` template.

## Alternate Branch Name Idea

- **`0` - blank branch**
- **`1` [primary] - sharing branch**
- **`2` - edit branch**

## How to: Hot Link an Image

Steps to embed an image named `jimi.png` on a website:

1. Open the Repository either in the GitHub client or on the GitHub website.
2. Add the image to the repo then commit and push it.
3. Go to the repo on GitHub & switch to the `i` branch
4. Click the name of the image & copy the image link
5. On the target page, insert the link the appropriate way and save the file. The Full link is:
   ```bash
   https://raw.githubusercontent.com/8rents/img/1/jimi.png
   ```
   Which is easy to remember!
   
   `https://raw.githubusercontent.com/`[`username`/`repo`/`branch`/`filename`]

   - All you have to do is memorize: `https://raw.githubusercontent.com/`

   **After that add:** `username`/`repo`/`branch`/`folder (blank if on root)`/`file name`

   - **So the complete URL for the uploaded image would be:**
     ```bash
     https://raw.githubusercontent.com/8rents/img/1/jimi.png
     ```

   - **To embed this with markdown:**
     ![Jimi](https://raw.githubusercontent.com/8rents/img/1/jimi.png)
   - **Embed with HTML:**
     `<img src="https://raw.githubusercontent.com/8rents/img/1/jimi.png" alt="Jimi">`

     ![Jimi](https://raw.githubusercontent.com/8rents/img/1/jimi.png)

## Making a snippet for the URL of the Repo

To save your self a lot of time, you can make a snippet for ease of linking uploaded images.

A markdown snippet would look something like this: `![alt](https://raw.githubusercontent.com/8rents/img/1/)` It's up to you to decide how to trigger it, or if you just wan to copy paste it whenever you need it. If you copy / pasted the above snippet you would need to edit it. Here's a good example of how it's done.

`![alt](https://raw.githubusercontent.com/8rents/img/1/)`


First you'd want to edit the `alt` text. This is the text that is displayed if the image isn't displayed. It's also the text served to the visually disabled who can't see images. You should make it descriptive of what the image actualy it. The image in this example is a silkscreen picture of Jimi Hendrix that I use as my account icon. In this case I would make the `alt` text something like `8rent's GitHub account icon`. In a different context I would probably mention that it's a picture of Jimi Hendrix but since it's just my account icon, it makes the most sense to simply say that.

`![`***`8rent's GitHub account icon`***`](https://raw.githubusercontent.com/8rents/img/1/)`


Next I'll want to add the path and the name of the file

The image is an `account` `icon` of `jimi` hendrix, the size I want is `256` px by 256px and naturally it is a `png` file type.


`![8rent's GitHub account icon](https://raw.githubusercontent.com/8rents/img/1/`***`account/icons/jimi/256.png`***`)`

## File Guidelines

- File names must consist of lowercase letters, numbers & hyphens only
- Use only open formats whenever possible avoid proprietary formats like Google's `webm`. 
  **Note:** *the exception to these rules is for editing mode for formats like `PSD` (Photoshop) or `ALS` (Ableton Live)


## Preferred File Types

File types can be in whatever type I need to share. I tend to prefer:

- Open Formats
- Easy to mutate

Here is a brief list of my order of preference of file formats:

#### Text Documents

- **Markdown (Good)**
- Microsoft Word
- PDF (Not Good)

> Markdown is the winner here because it's completely open source, works better, is cleaner and is not completely stupid in the way that a `docx` or `pdf` file is.

#### Images

Prefer image formats in the following order for the following types of styles

##### Photographic style Images

The following formats are ideal for photographic style images that do not have a set amount of colors.

- **PNG**
- JPG

> PNG is the preffered image type because it is lossless, meaning that the compressed information is not discarded and irretrivable. While it has a much larger file size than a well compressed jpeg, it looks a lot better in > 90% of circumstances.

##### Limited Color Images (like a cartoon)

The following formats are ideal for images that have a limited color pallet. Think of how a cartoon still looks.

- **SVG**
- GIF

> SVG wins this because:
>
> 1. It's a completely open format
> 2. It is a resolution independent vector

> **NOTE: SVG's can not be animated in the same abusive way that GIFs can, so if you need your limited color pallet image yo be animate gif is going to be the way to go until x264 or 65 embeds are standard and common place.**

## Tracking an images lineage and history

The following is a system that I am devising to track an images lineage through a series of edits. 

### Tracking changes directly within the directory structure

Using a set of nested folders in the `share` branch. We can set up a nested structure to link for various purposes or for different situations.

### Tracking changes using branches and git commits

Instead of using nested directories on the public share branch it may make more sense to use a specific `dev` or `edits` branch to make changes on.

#### Example #1: 8rents accounts jimi icon and variations
---

**🤍 2024 [Brenton Holiday](https://8rents.github.io)**
