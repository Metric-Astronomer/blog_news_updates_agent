Install the gcloud CLI 

bookmark_border
This page contains instructions for choosing and maintaining a Google Cloud CLI installation. The Google Cloud CLI includes the gcloud, gsutil and bq command-line tools. For a list of gcloud CLI features, see All features.

To access the Google Cloud APIs using a supported programming language, you can download the Cloud Client Libraries.

Installation instructions
These instructions are for installing the Google Cloud CLI. For information about installing additional components, such as gcloud CLI commands at the alpha or beta release level, see Managing gcloud CLI components.

Note: If you are behind a proxy or firewall, see the proxy settings page for more information on installation.
Linux
Debian/Ubuntu
Red Hat/Fedora/CentOS
macOS
Windows
Confirm that you have a supported version of Python:
To check your current Python version, run python3 -V or python -V. Supported versions are Python 3.8 to 3.13.
The main install script offers to install CPython's Python 3.12.
Xcode command line tool is required to install Python.
Verify that Xcode is installed by running: xcode-select -p.
If Xcode is not installed, install it by running: sudo xcode-select --install.
Otherwise, to install a supported Python version, please visit the Python.org Python Releases for macOS.
If you have multiple Python interpreters installed on your machine, set the CLOUDSDK_PYTHON environment variable within your shell to point to the path of your preferred interpreter.
For more information on how to choose and configure your Python interpreter, see gcloud topic startup.
Download one of the following:
Note: To determine your machine hardware name, run uname -m from a command line.
Platform	Package	Size	SHA256 Checksum
macOS 64-bit
(x86_64)

google-cloud-cli-darwin-x86_64.tar.gz	55.5 MB	580e483669fb94d296473a01ae3092ddd25c929bdda1e5c76ace9de28fe1524c
macOS 64-bit
(ARM64, Apple silicon)

google-cloud-cli-darwin-arm.tar.gz	55.5 MB	cccbc9d59ed9fa519e0672457c69e60e2363c7253b540a0cda28060adb425d14
macOS 32-bit
(x86)

google-cloud-cli-darwin-x86.tar.gz	54.0 MB	93c75d84612a1fb9ba10559157ad515c7103d4b26733db70d36aec49bd90cb15
Extract the archive to any location on your file system (preferably your Home directory). On macOS, this can be achieved by opening the downloaded .tar.gz archive file in the preferred location. Or run the following command:


tar -xf google-cloud-cli-darwin-arm.tar.gz
Optional: To replace an existing installation, remove the existing google-cloud-sdk directory and then extract the archive to the same location.

Run the installation script (from the root of the folder you extracted in the last step) using the following command:


./google-cloud-sdk/install.sh
The script will prompt to install Python 3.12 and certain recommended modules.

The install can also be done non-interactively (for example, using a script) by providing preferences as flags. To describe the available flags, run:


./google-cloud-sdk/install.sh --help
To run the install script with screen reader mode on:


./google-cloud-sdk/install.sh --screen-reader=true
Optional:
To send anonymous usage statistics to help improve the gcloud CLI, answer Y when prompted.
To add the gcloud CLI to your PATH and enable command completion, answer Y when prompted.
If you updated your PATH in the previous step, open a new terminal so that the changes take effect.
To initialize the gcloud CLI, run gcloud init:


./google-cloud-sdk/bin/gcloud init
Optional. Install additional components using the component manager.
Other installation options
Depending on your development needs, instead of the recommended installation, you can use an alternative method of installing the gcloud CLI:

Using the gcloud CLI with scripts or Continuous Integration/Deployment? Download a versioned archive for a non-interactive installation of a specific version of the gcloud CLI.
Need to run the gcloud CLI as a Docker image? Use the gcloud CLI Docker image for the latest release (or a specific version) of the gcloud CLI.
Running Ubuntu and prefer automatic updates? Use a snap package to install the gcloud CLI.
For Windows and macOS interactive installations, and all other use cases, run the interactive installer to install the latest release of the gcloud CLI.
Manage an installation
After you have installed the gcloud CLI, you can use commands in the gcloud components command group to manage your installation. This includes viewing installed components, adding and removing components, and upgrading to a new version or downgrading to a specific version of the gcloud CLI.

Note: If you used apt-get or yum to install the gcloud CLI, you must use use apt-get or yum to update or remove components, not gcloud components.
Earlier versions of the gcloud CLI
If you need a different version of the gcloud CLI, install the current version using the instructions that appear earlier on this page and then log in. After you are logged in, you can download earlier releases. To see the versions sorted by date, be sure to enable Sort and filter and click the Created column.

Supported Python versions
The Google Cloud CLI requires Python 3.8 to 3.13. For information on how to choose and configure your Python interpreter, see gcloud topic startup.

