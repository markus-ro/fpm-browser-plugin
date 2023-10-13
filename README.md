# Foundation Password Manager Browser Plugin
![License: BSD 3-Clause](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)  ![JavaScript](https://img.shields.io/badge/logo-javascript-blue?logo=javascript)

This repository contains the source code for the Foundation Password Manager Browser Plugin. The plugin is a browser extension that allows for the automatic fill of usernames and passwords. Depending on the configuration of the Foundation Password Manager, the plugin can also be used to trigger a brainwave-based authentication procedure in order to authenticate the user. The plugin is made up of two parts: a background script and a content script. The background script is responsible for the communication with the Foundation Password Manager and the content script is responsible for the communication with the website.

This repository was partially created for the paper "Overcoming Theory: Designing Brainwave Authentication for the Real World" by Markus Röse, [Emiram Kablo](https://twitter.com/emikablo), and [Patricia Arias-Cabarcos](https://twitter.com/patriAriasC). The paper was presented at the [EuroUSEC 2023](https://eurousec23.itu.dk/) conference and can be found [here](https://doi.org/10.1145/3617072.3617120).

If you use this repository, please cite the paper as follows:
```
@inproceedings{roese2023overcoming,
  title={Overcoming Theory: Designing Brainwave Authentication for the Real World},
  author={R\"ose, Markus and Kablo, Emiram and Arias-Cabarcos, Patricia},
  booktitle={The 2023 European Symposium on Usable Security (EuroUSEC 2023)},
  address={Copenhagen, Denmark},
  publisher={ACM, New York, NY, USA},
  month={October 16--17}
  doi={110.1145/3617072.3617120},
  year={2023}
}
```

## Installation
The plugin is currently only available for Mozilla Firefox. The plugin is not yet available on the Mozilla Firefox Add-ons website. The plugin can be installed by downloading the source code and loading it as a temporary add-on in Firefox. The plugin can be loaded as a temporary add-on by navigating to `about:debugging` in Firefox and clicking on the `Load Temporary Add-on` button. The plugin can then be loaded by selecting the `manifest.json` file in the `src` folder of the source code.

Once installation is complete, the plugin tries to connect to a running instance of the Foundation Password Manager. If an instance is found, it checks wether credentials for the current website are available. If credentials are available, the plugin adds a new button which triggers the selected authentication procedure. If no credentials are available, nothing happens.

## License
The source code is licensed under the BSD 3-Clause License. See the [LICENSE](LICENSE) file for more information.
