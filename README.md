# IGExperimentsHooksUpdates
Repository for updating class hooks used by the [IGExperiments Xposed module](https://github.com/xHookman/IGexperiments), which enables developer options in Instagram. By hosting the hook updates separately, we ensure that the main module remains clean and focused on its primary functionality.

### Objectives:
- **Centralized Hook Management:** Provides a single, centralized JSON file (`hooks.json`) that lists all necessary class hooks, simplifying the process of updating and maintaining these entries.
- **Community-Driven Updates:** Encourages community contributions to keep the hooks up-to-date with the latest Instagram app changes, enhancing the module's reliability and functionality.
- **Automated Fetching:** Integrates with the main IGExperiments module to automatically fetch the latest hook configurations, ensuring seamless updates and compatibility.

### How to Contribute:
1. **Fork the Repository:** Create a fork of the repository on your GitHub account.
2. **Update the JSON File:** Modify the `hooks.json` file by adding new entries or updating existing ones as needed based on new versions of Instagram or functionality changes.
3. **Pull Request:** Submit a pull request to merge your changes. Ensure your updates are well-documented and tested.

### How to Support new versions:
First you will need to use [Jadx](https://github.com/skylot/jadx)
 to decompile an [Instagram apk](https://www.apkmirror.com/apk/instagram/).

- Open Jadx and select your apk.
- Click on the text search button at top, wait for decompiling (it can takes several times)
- Search for "```"is_employee", Boolean.valueOf```" and find a line similar to:

```
c0at.A0J("is_employee", Boolean.valueOf(AnonymousClass196.A00(userSession)));
```
<img src="https://github.com/xHookman/IGexperiments/blob/master/readme/1.png?raw=true">

Double click on the method name, A00:

<img src="https://github.com/xHookman/IGexperiments/blob/master/readme/2.png?raw=true">

Now go at top, you will see a line like this: 
```
/* renamed from: X.196 reason: invalid class name */
```
<img src="https://github.com/xHookman/IGexperiments/blob/master/readme/3.png?raw=true">


You now know the class to hook: X.196

Method to hook: A00

Second class to hook: com.instagram.common.session.UserSession

You can now try if it works by enabling HECKER mode and completing the class name and method name field, click on hook and kill Instagram - Root devices ONLY!

Contributors of all experience levels are welcome! Whether you're making your first contribution to open source or you're a seasoned developer, your input is valuable in keeping the IGExperiments module functional and current.

### Usage:
The main IGExperiments Xposed module will periodically check this repository for updates to the `hooks.json` file. This setup ensures that the module uses the most recent data without manual intervention, thus reducing errors and maintaining module effectiveness.

### Getting Involved:
If you find any issues or if you have suggestions for improvements, please submit an issue on this repository. For broader discussions or proposals, the repository's discussions section is a great place to collaborate with other developers.

Together, we can ensure that the IGExperiments module continues to offer great utility to Instagram developers by providing timely and effective updates.

## Authors

- [@xHookman](https://github.com/xHookman)
- [@ReSo7200](https://github.com/ReSo7200)

### Contributors
 - [@Vasilis](https://github.com/down-bad)
 - [@rmnscnce](https://github.com/rmnscnce)
