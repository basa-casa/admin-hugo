# /admin
A [NetlifyCMS](https://netlifycms.org) generator, made with love, [Hugo](https://gohugo.io), NetlifyCMS, and [theNewDynamic's](https://www.thenewdynamic.com) [hugo-module-tnd-netlifycms](https://github.com/theNewDynamic/hugo-module-tnd-netlifycms). 

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
            path = "github.com/basa-casa/hugo-module-bc-nc-admin"
    ```

## Usage
### Getting Started
1. Run `npx netlify-cms-proxy-server` and your `hugo server` commands from the root directory of your site repository.
2. Open [/nc-admin](http://localhost:1313/admin).

Your site now has four pages, at`/admin`, `/admin/content`, `/admin/structure`, and `/admin/configuration`. 

### /admin

Manages the setup of each /admin/{{cms}} with `collection admin-pages`
This branch bundle cascades common netlify-CMS configuration settings down to each page below it. Override the module default at /admin/configuration/admin

### /admin/content
### /admin/data/netlifycms/collections
### /admin/data/netlifycms/fields
### /admin/configuration
Hugo Configs
Hugo Environments
### /admin/layouts
Hugo Layouts
Hugo config.modules?
### /admin/archetypes
import collection set for admin/content, point each at `/archetypes`?
### People

Manages users, roles, and permissions.

### Reports

Contains links to logs, update information, search information, and other information about the site’s status.


### Help

Lists help topics for installed modules that provide them.


