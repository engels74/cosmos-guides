# 01) The Node shows up as offline

## Help! My Pterodactyl Node shows up as Offline in the Panel! :angry:

If the Pterodactyl Node appears to be offline (with a red heart symbol instead of a green heart), you can try the following. However, keep in mind that it may not work for you.

Before proceeding with any of these steps, ensure that you have completed all of the steps in the guide and have not missed any.

### Disable the Smart Shield Protection

* Disable the **Smart Shield Protection** for the `pt-wings` URL. It somtimes doesn't play well with the `pt-wings`. It might change in the future. If you don't want to Disable it entirely, you can try setting the setting to Lenient instead of Default.

<figure><img src="https://i.imgur.com/dcfr4NV.gif" alt=""><figcaption></figcaption></figure>

### Setup CORS with a wildcard

* If the step above didn't do anything, you could try and use the \* for the CORS option. This is covered in [this section](../../pterodactyl-setup/02-creating-urls/02c-setting-up-cors/02cb-cors-option-2-failsafe.md) of the how-to guide.
