[![Latest Stable Version](https://poser.pugx.org/carbon/primarycontent/v/stable)](https://packagist.org/packages/carbon/primarycontent)
[![Total Downloads](https://poser.pugx.org/carbon/primarycontent/downloads)](https://packagist.org/packages/carbon/primarycontent)
[![License](https://poser.pugx.org/carbon/primarycontent/license)](LICENSE)
[![GitHub forks](https://img.shields.io/github/forks/CarbonPackages/Carbon.PrimaryContent.svg?style=social&label=Fork)](https://github.com/CarbonPackages/Carbon.PrimaryContent/fork)
[![GitHub stars](https://img.shields.io/github/stars/CarbonPackages/Carbon.PrimaryContent.svg?style=social&label=Stars)](https://github.com/CarbonPackages/Carbon.PrimaryContent/stargazers)
[![GitHub watchers](https://img.shields.io/github/watchers/CarbonPackages/Carbon.PrimaryContent.svg?style=social&label=Watch)](https://github.com/CarbonPackages/Carbon.PrimaryContent/subscription)

# Carbon.PrimaryContent Package for Neos CMS

## [`Carbon.PrimaryContent:PrimaryContent`](Resources/Private/Fusion/Helper/PrimaryContent.fusion)

This is an own implementation from PrimaryContent. If a document node has a prototype with a `.MainContent` or a `.PlainContent` suffix this prototype will be used as content. Otherwise, the ContentCollection will be rendered. It is also possible to pass your own content.

## [`Carbon.PrimaryContent:ClassArray`](Resources/Private/Fusion/Helper/ClassArray.fusion)

Raw Array of the css classes for the `Carbon.PrimaryContent:PrimaryContent`.
Can be used also for the `body` tag.

## [`Carbon.PrimaryContent:NodeTypeName`](Resources/Private/Fusion/Helper/NodeTypeName.fusion)

Convert a name from a nodetype to a `hyphen-case-string`. Make use of `Carbon.PrimaryContent:RemoveVendors`.

## [`Carbon.PrimaryContent:RemoveVendors`](Resources/Private/Fusion/Helper/RemoveVendors.fusion)

If you want to remove some of the vendor names from the NodeTypeName, this helper is for you. Per default it will read the setting `Carbon.PrimaryContent.removeVendors`

Example:

```elm
prototype(Carbon.PrimaryContent:NodeTypeName) {
    @process.removeVendorName = Carbon.PrimaryContent:RemoveVendors {
        vendors = ${['Vendor', 'Foo', 'Bar']}
    }
}
```

## License

Licensed under MIT, see [LICENSE](LICENSE)
