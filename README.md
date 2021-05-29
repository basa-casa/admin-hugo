# /nc-admin
An admin for Netlify CMS, built in itself, with the help of Hugo, theNewDynamic, and Basa Casa. 

1. Import this module in your Hugo config.
    ```
    [module]
        [[module.imports]]
            path = "github.com/basa-casa/hugo-module-bc-nc-admin"
    ```
1. run `npx netlify-cms-proxy-server` and `hugo server` from the base of your site repository.
1. Navigate to localhost:1313/nc-admin at your site.
1. Create the CMS, with at least one collection, `type import`, to `collection config`. 
1. Add import collections to `collection files_collections` and `collection folder_collections` for the ability to create importable collections of your own.