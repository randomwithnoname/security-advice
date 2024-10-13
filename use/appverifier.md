[🔗](https://github.com/randomwithnoname/security-advice/tree/main/use/appverifier.md)

[AppVerifier](https://github.com/soupslurpr/AppVerifier) is not an app store or a way to obtain apps. It's simply an app signing certificate hash viewer and verifier, which can be useful when obtaining apps without using an app store that has robust validity guarantees for installed apps. 

[Obtainium](https://github.com/ImranR98/Obtainium/blob/main/README.md#-obtainium) will automatically open the share menu to share a newly installed app with AppVerifier if you have it installed and haven't disabled that feature in Obtainium. You only need to verify the initial installation, as Android prevents installing updates that aren't signed by the same key or a key authorized by it, as well as versions older than the one currently installed.
