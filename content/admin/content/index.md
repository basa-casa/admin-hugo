---
title: Content
draft: false
menu:
  admin:
    weight: 40
collections:
  - import: collection hugo-content-default
    collection_type: import
---
 
Content writers and editors can use the CMS at [`admin/content`](/admin/content) to create and edit files in the  `content` directory.  

## Creating Content
Replace with instructions including links for your users to create content

## Editing Content
Replace with instructions for your users to edit content

## Manage Content Creation Collections

### Create Collections for Import 

Open [`admin/collections`](/admin/collections) to create and edit the forms they will fill out to add content files to your site. 

## Create Content Admin Override File

Copy the Content admin page into your project at the same location. Your version of the file will now control the cms above and this help page.

`content/admin/collections/index.md`

```
{{< readfile file="/content/admin/content/index.md" >}}
```

## Add Collections to admin/content

Edit the file now recognized in [`/admin`](/admin/#/collections/admin-pages/entries/content/index).
Import collections by clicking add new collection, selecting the import type, and entering `collection {filename}` with your collection's filename as located in `data/scms/collections`.  Publish the change and visit [`admin/content`](/admin/content) to create content with the form.

