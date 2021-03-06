# PWA Studio Release 12.3.0

**NOTE:**  
_This changelog only contains release notes for PWA Studio and Venia 12.3.0_  
_For older release notes, see_ [PWA Studio releases][].


## Highlights  
  
-   Add shimmer loader on dynamic blocks to avoid layout shift. Shimmer loaders will only be rendered if minHeight is specified on the row containing a dynamic block. This gives flexibility to users to display a shimmer or not (let's say a dynamic block wouldn't render most of the time, we probably don't want to display a shimmer) — [3713][]  
-   Added the new \`PersonalizedContentSampleDataVenia\` module that contains customer segments, dynamic blocks and cart rule promotion sample data for personalized content. — [19.,2.,3670][]  
-   You can now use ReCaptcha V3 on the Braintree payment form and the Place Order form. — [3691,24][]  
-   reCAPTCHA V3 validation is now available on the following customer forms:
    \- Customer Login
    \- Customer account creation
    \- Customer information change (password) — [3702][]  
-   reCaptcha has been enabled for the Forgot Password form. — [3604,12,20][]  
-   MISSING RELEASE NOTE— [PWA-2453][]  
-   MISSING RELEASE NOTE— [PWA-2653][]  
-   In the Link component, \`prefetchType\` property has been renamed to \`shouldPrefetch\`. This helps to clarify that it is a boolean, rather a property that returns a type. \`prefetchType\` is deprecated but not removed. — [3646][]  
-   Store-view specific label and localization support has been added for product attributes. — [17][]  
-   MISSING RELEASE NOTE— [PWA-2610][]  
-   Refactored the reCaptcha to ensure it is backwards compatible with 12.2.0. — [3696][]  
-   The "Sign In" link has been removed from from the 2nd stage of checkout. This will ensure the cart configuration (guest or account holder) does not change in the middle of checkout. — [3672][]  
-   MISSING RELEASE NOTE— [PWA-2296][]  
-   Images from PageBuilder content now include height and width dimensions. This will help with initial layout rendering. — [files][]  
-   Shopping cart promotions are now properly displayed depending on customer segment. For instance, an incorrect promotion could be displayed when merging a guest cart with a customer cart. — [3609][]  
-   You can now make GraphQL queries for dynamic blocks. — [3587,2][]  
-   Configurable images are now shown in the Edit Cart Item menu. Previously, the parent image would be shown, without configured options. — [3695][]  
-   PWA Studio can now retrieve image metadata from PageBuilder. — [16,17][]  
-   PWA Studio now supports PHP 8.1. — [14,11,7,17][]  
-   Dependency packages have been updated. See https&#x3A;//github.com/magento/pwa-studio/pull/3611 for more details about specific package versions. — [3611][]  
-   MISSING RELEASE NOTE— [PWA-2220][]  
-   Adobe Commerce users can now set gift options on the Order level. — [3540][]  
-   The correct product-specific image is now displayed in the mini-cart. Previously, the default product image was shown. — [3690][]  
-   Long wish list names no longer break the layout or force scrolling to close modal dialogs. — [3706][]  
-   We now use "Best Match" as the default sort order on the Search Results page. Previously "Position" was the default order. — [3698][]  
-   Products with configurable product variants are now properly added to Wish Lists. Previously, adding a configurable product threw an error. — [files][]  
-   MISSING RELEASE NOTE— [PWA-2617][]  
-   MISSING RELEASE NOTE— [PWA-2616][]  
-   GraphQL now properly returns only qualified blocks to PWA Studio. Previously, unqualified blocks were mistakenly sent in the query. — [3678,3][]  
-   The virtual products extension has been removed. — [3612][]  
-   Changed instances of the \`useMemo\` type to \`const\` in the \`productUrlSuffix\` talon to improve performance. — [3660][]  
-   PWA Studio now properly hides the "Create a list" button when reaching the maximum number of wishlists in the users "Favorite lists". Previously, the button was displayed when the max number was reached. — [3668][]  
-   CSS has been adjusted so that the header logo no longer overlaps the main navigation. — [3659][]  
-   Fix the click target accuracy when clicking tab in a long list of tabs from the pagebuilder. — [3676][]  


| Type  | Description                                                                                                                                       | GitHub PR                       |
| :---- | :------------------------------------------------------------------------------------------------------------------------------------------------ | :------------------------------ |
| Story | Shimmer Loader for Dynamic Blocks                                                                                                                 | [3713][]                        |
| Story | Update the Sample Data with Personalized content                                                                                                  | [19.][], [2.][], [3670][],      |
| Story | Add reCaptcha to the Checkout  Forms                                                                                                              | [3691][], [24][],               |
| Story | Add reCaptcha to the Account Information Forms                                                                                                    | [3702][]                        |
| Story | Add reCaptcha to the Forgot Password  Form                                                                                                        | [3604][], [12][], [20][],       |
| Story | Add cypress status reporting while running headless                                                                                               | [3613][]                        |
| Story | Remove PHP 8.1 Support                                                                                                                            | [25][], [4][], [22][], [3][],   |
| Story | \[Issue] Rename Link's prefetchType prop                                                                                                          | [3646][]                        |
| Story | Store view specific label/localization support for product attributes                                                                             | [17][]                          |
| Story | Update magento capability table                                                                                                                   | [3724][]                        |
| Story | reFACTA reCAPTCHA                                                                                                                                 | [3696][]                        |
| Story | Remove Sign In link on 2nd step of checkout                                                                                                       | [3672][]                        |
| Story | CMS Page Shimmer Loader                                                                                                                           | [3711][]                        |
| Story | Images to include dimensions                                                                                                                      | [files][]                       |
| Story | Validate Shopping Cart Promotions are displayed correctly                                                                                         | [3609][]                        |
| Story | Query for available Dynamic Blocks                                                                                                                | [3587][], [2][],                |
| Story | Configurable images are not shown in Edit Cart Item menu                                                                                          | [3695][]                        |
| Story | Backend pagebuilder image metadata support                                                                                                        | [16][], [17][],                 |
| Story | Support PHP 8.1.0 for all PWA related repo's                                                                                                      | [14][], [11][], [7][], [17][],  |
| Story | Update packages and dependencies                                                                                                                  | [3611][]                        |
| Story | \[Doc] Best Practice of developing for the customer segmentation                                                                                  | [][]                            |
| Bug   | Gift options on Order Level (Commerce only)                                                                                                       | [3540][]                        |
| Bug   | Parent product image thumbnail has been showns in mini cart instead of product itself                                                             | [3690][]                        |
| Bug   | Long wishlist name length breaks layout                                                                                                           | [3706][]                        |
| Bug   | Change sort on Search page to relevance                                                                                                           | [3698][]                        |
| Bug   | Wishlist page error when configured variant added                                                                                                 | [files][]                       |
| Bug   | Venia sample data personalised content not updating                                                                                               | [20][]                          |
| Bug   | Fix Cypress Page Builder tests                                                                                                                    | [3715][]                        |
| Bug   | \[bug]: Dynamic Blocks GraphQL returns non-qualified blocks                                                                                       | [3678][], [3][],                |
| Bug   | Remove virtual products extension                                                                                                                 | [3612][]                        |
| Bug   | \[feature]: Possible wrong usage of useMemo                                                                                                       | [3660][]                        |
| Bug   | \[bug]: PWA multiple wishlist:  storefront still showing create whishlist button when reach max number of allowed wishlists configured in magento | [3668][]                        |
| Bug   | Header - Logo dimensions overlap with main content                                                                                                | [3659][]                        |
| Bug   | \[PB] Click target for long spanning tabs is inconsistent                                                                                         | [3676][]                        |


[PWA-2228]: https://jira.corp.magento.com/browse/PWA-2228  
[PWA-2227]: https://jira.corp.magento.com/browse/PWA-2227  
[PWA-2065]: https://jira.corp.magento.com/browse/PWA-2065  
[PWA-2064]: https://jira.corp.magento.com/browse/PWA-2064  
[PWA-2063]: https://jira.corp.magento.com/browse/PWA-2063  
[PWA-2453]: https://jira.corp.magento.com/browse/PWA-2453  
[PWA-2653]: https://jira.corp.magento.com/browse/PWA-2653  
[PWA-2498]: https://jira.corp.magento.com/browse/PWA-2498  
[PWA-2509]: https://jira.corp.magento.com/browse/PWA-2509  
[PWA-2610]: https://jira.corp.magento.com/browse/PWA-2610  
[PWA-2570]: https://jira.corp.magento.com/browse/PWA-2570  
[PWA-1199]: https://jira.corp.magento.com/browse/PWA-1199  
[PWA-2296]: https://jira.corp.magento.com/browse/PWA-2296  
[PWA-2295]: https://jira.corp.magento.com/browse/PWA-2295  
[PWA-2172]: https://jira.corp.magento.com/browse/PWA-2172  
[PWA-2169]: https://jira.corp.magento.com/browse/PWA-2169  
[PWA-2415]: https://jira.corp.magento.com/browse/PWA-2415  
[PWA-2418]: https://jira.corp.magento.com/browse/PWA-2418  
[PWA-2401]: https://jira.corp.magento.com/browse/PWA-2401  
[PWA-2400]: https://jira.corp.magento.com/browse/PWA-2400  
[PWA-2220]: https://jira.corp.magento.com/browse/PWA-2220  
[PWA-1947]: https://jira.corp.magento.com/browse/PWA-1947  
[PWA-2543]: https://jira.corp.magento.com/browse/PWA-2543  
[PWA-2554]: https://jira.corp.magento.com/browse/PWA-2554  
[PWA-2552]: https://jira.corp.magento.com/browse/PWA-2552  
[PWA-2575]: https://jira.corp.magento.com/browse/PWA-2575  
[PWA-2617]: https://jira.corp.magento.com/browse/PWA-2617  
[PWA-2616]: https://jira.corp.magento.com/browse/PWA-2616  
[PWA-2174]: https://jira.corp.magento.com/browse/PWA-2174  
[PWA-2432]: https://jira.corp.magento.com/browse/PWA-2432  
[PWA-2413]: https://jira.corp.magento.com/browse/PWA-2413  
[PWA-2479]: https://jira.corp.magento.com/browse/PWA-2479  
[PWA-2463]: https://jira.corp.magento.com/browse/PWA-2463  
[PWA-1950]: https://jira.corp.magento.com/browse/PWA-1950  


[3713]: https://github.com/magento/pwa-studio/pull/3713
[19.]: https://github.com/magento-commerce/venia-sample-data-modules/pull/19.
[2.]: https://github.com/magento-commerce/venia-sample-data-modules-ee/pull/2.
[3670]: https://github.com/magento/pwa-studio/pull/3670
[3691]: https://github.com/magento/pwa-studio/pull/3691
[24]: https://github.com/magento-commerce/magento2-pwa/pull/24
[3702]: https://github.com/magento/pwa-studio/pull/3702
[3604]: https://github.com/magento/pwa-studio/pull/3604
[12]: https://github.com/magento-commerce/magento2-pwa/pull/12
[20]: https://github.com/magento-commerce/magento2-pwa/pull/20
[3613]: https://github.com/magento/pwa-studio/pull/3613
[25]: https://github.com/magento-commerce/magento2-pwa/pull/25
[4]: https://github.com/magento-commerce/magento2-pwa-commerce/pull/4
[22]: github.com/magento-commerce/venia-sample-data-modules/pull/22
[3]: github.com/magento-commerce/venia-sample-data-modules-ee/pull/3
[3646]: https://github.com/magento/pwa-studio/pull/3646
[17]: https://github.com/magento-commerce/magento2-pwa/pull/17
[3724]: https://github.com/magento/pwa-studio/pull/3724
[3696]: https://github.com/magento/pwa-studio/pull/3696
[3672]: https://github.com/magento/pwa-studio/pull/3672
[3711]: https://github.com/magento/pwa-studio/pull/3711
[files]: https://github.com/magento/pwa-studio/pull/3712/files
[3609]: https://github.com/magento/pwa-studio/pull/3609
[3587]: https://github.com/magento/pwa-studio/pull/3587
[2]: https://github.com/magento-commerce/magento2-pwa-commerce/pull/2
[3695]: https://github.com/magento/pwa-studio/pull/3695
[16]: https://github.com/magento-commerce/magento2-pwa/pull/16
[17]: https://github.com/magento-commerce/venia-sample-data-modules/pull/17
[14]: https://github.com/magento-commerce/venia-sample-data-modules/pull/14
[11]: https://github.com/magento-commerce/magento2-pwa/pull/11
[7]: https://github.com/magento-commerce/upward-php/pull/7
[17]: https://github.com/magento-commerce/magento2-upward-connector/pull/17
[3611]: https://github.com/magento/pwa-studio/pull/3611

[3540]: https://github.com/magento/pwa-studio/pull/3540
[3690]: https://github.com/magento/pwa-studio/pull/3690
[3706]: https://github.com/magento/pwa-studio/pull/3706
[3698]: https://github.com/magento/pwa-studio/pull/3698
[files]: https://github.com/magento/pwa-studio/pull/3703/files
[20]: https://github.com/magento-commerce/venia-sample-data-modules/pull/20
[3715]: https://github.com/magento/pwa-studio/pull/3715
[3678]: https://github.com/magento/pwa-studio/pull/3678
[3]: https://github.com/magento-commerce/magento2-pwa-commerce/pull/3
[3612]: https://github.com/magento/pwa-studio/pull/3612
[3660]: https://github.com/magento/pwa-studio/pull/3660
[3668]: https://github.com/magento/pwa-studio/pull/3668
[3659]: https://github.com/magento/pwa-studio/pull/3659
[3676]: https://github.com/magento/pwa-studio/pull/3676


[PWA Studio releases]: https://github.com/magento/pwa-studio/releases

