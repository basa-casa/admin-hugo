# /nc-admin
A D.R.Y.-er [NetlifyCMS](https://netlifycms.org) generator, made with love, [Hugo](https://gohugo.io), NetlifyCMS, and [theNewDynamic's](https://www.thenewdynamic.com) [hugo-module-tnd-netlifycms](https://github.com/theNewDynamic/hugo-module-tnd-netlifycms). 

## Prerequisites
Go 1.14
Hugo 0.61.0
Node
## Installation
1. Initialize your project as a hugo module with `hugo mod init`. 
1. Import this module in your Hugo `config.toml`.
    ```toml
    [module]
        [[module.imports]]
            path = "github.com/basa-casa/hugo-module-admin"
    ```

## Usage
### Getting Started
Because the module's `/data/netlifycms/config.yml` file has `local_repo: true`, you can get started with the following as soon as the module is in your config.
1. Run `npx netlify-cms-proxy-server` and `hugo server` from the root directory of your site repository.
1. Open [/nc-admin](http://localhost:1313/nc-admin).
1. Click "Create the CMS." Edit your backend settings, and add collections. When you are ready, click "Publish Now" and the CMS will create the `/data/netlifycms/config.yml` file that is the base of `/content/nc-admin/config.yml`

At this point, Hugo will merge the information in the site's `/data/netlifycms/config.yml` file on top of the module's version. The new CMS will include any settings in the module's file that are not in the site's. For example, if you publish the new file without specifying any `collections:`, the CMS collection from the module's config file will remain in use. 

### CMS Config
We recommend adding the following to the site's `/data/netlifycms/config.yml`, through the interface or in your text editor.

```yaml
collections:
  - import: collection site_settings
    collection_type: import
```

This file collection exists in the module, with the following configuration

```yaml
name: site_settings
label: Site Settings
collection_type: files
description: "Files collection for settings."
files:
  - import: file netlifycms_config
    type: import 
```
The file imported into the collection controls the base config file, using the fields from the CMS folder collection you used to create it.
```yaml
label: CMS Configuration
type: file
name: config
file: data/netlifycms/config.yml
fields:
  - import: collection bc-nc-cms.fields
    field_type: import
```

To add files to the Site Settings collection, you will need to create a new File Collection at `data/netlifycms/collections/site_settings.yml`. 

### Collections, Fields, Files, and Sets
To create collections in the UI for import to `config.yml`, simply add
```yaml
collections:
  - import: set cffs.collections
    collection_type: import
```
This set of collections contains folder collections for folder collections, files collections, files collection files, fields of every type, and sets of each of the above. 

### Customization
Import [`set nc_admin`](data/netlifycms/collectionSets/nc_admin.yml) to create overriding option fields or baseCollections as needed. 



