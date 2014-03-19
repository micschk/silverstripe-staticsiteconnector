# ToDo

This is non-priority (i.e. random) and inexhaustive list of tasks that we'd like to see completed to really polish this module.
Some are already registered as issues on Github, others are more in the "would like to have" basket, others may not make it at all:

## StaticSiteConnector Module Issues

* BUG: Bug when using no "www." prefix in basic setup, URLs appear as t.nz for example in "urls" cache file (see simplifyUrl() ??)
* BUG: Show only a partial tree under each "Connector" in the crawl tab, as larger lists from large crawls, slow down the CMS considerably (Firefox OS/X, likely others also)
* BUG: Hide the "Schema" field on each import rule CMS UI, it is not needed.
* BUG: MimeType Processing is buggy when a zero-length mime-type is encountered.
* TASK: Is StaticSiteCrawlURLsTask needed anymore?
* TASK: Replace relevant StaticSiteMimeTypeProcessor logic with logic found in Zend_Validate_File_ExcludeMimeType.
.* ENHANCEMENT: Add a "Description" field to each schema. Allows users to outline/describe what content from the external site's page-content, each rule refers to.
* ENHANCEMENT: Add user help-text or hint explaining what the "Show content in menus" checkbox does.
* ENHANCEMENT: In addition to the "Number of URLs" total under the "Crawl" tab, modify to show a list of totals for each mime-type or SS type (e.g. SiteTree)
* ENHANCEMENT: After selecting "Crawl site", its label should switch to read "Crawling site..". Maybe show the CMS default "timer" icon too.
* ENHANCEMENT: Make the selection in the "Folder to import into" dropdown (FileMigrationTarget) used as the assets-target instead of the hard-coded "Import" value
* ENHANCEMENT: Add a schema export function for use in between similar sites hosted on multi/subsite CMS systems like SilverStripe and eZPublish for example.
* ENHANCEMENT: Add an onAfterImport() (see external-content module) to StaticSiteImporter and run StaticSiteRewriteLinksTask from it, based on CMS UI user-selection (default is 'yes')
* ENHANCEMENT: Add CMS UI to allow fine-grained control of the sleep time between server hits. See usleep() in StaticSite#Transformer#transform()

## External Content Module Issues:

* BUG: Fix the UI under the "Import" tab to store saved values. Currently you will lose your changes if you move away from the "Import" tab and then go back to it.
* [PR#17] ENHANCEMENT: Add a default to "Select how duplicate items should be handled" radio buttons field
* ENHANCEMENT: Change the externalContentSource` in the external-content module for displaying in the "Create" dropdown instead of the classname
 * Add a 'label' static on ExternalContentSource and subclasses, to show in this menu
 * Make that text disappear onfocus if it equals the default text