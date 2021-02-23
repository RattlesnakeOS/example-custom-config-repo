This is an example custom config repo that does the following:
* adds Seedvault
  * remote and project added in `local_manifests/custom.xml`
  * product_packages added in `vendor/config/main.mk`
  * backup transport enabled and set in `vendor/overlay/common/frameworks/base/packages/SettingsProvider/res/values/default.xml`
* adds microG 
  * sigspoof patch in `hooks/aosp_build_pre.sh`
  * project added in `local_manifests/custom.xml`
  * product_packages added in `vendor/config/main.mk`
* applies community patch for network toggle in `hooks/aosp_build_pre.sh`
* adds a custom hosts file in `hooks/aosp_build_pre.sh`
* commented out example that applies vanadium patches to chromium in `build_chromium_pre.sh`
* adds a fix to make newer versions of google camera to work
  * google_experience.xml added in `prebuilt`
  * prodcut_copy_files in `vendor/config/main.mk`