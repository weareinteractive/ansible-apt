<a name="2.7.0"></a>
## 2.7.0 (2019-09-16)


#### Features

*   extend unattended update config Merge branch 'pbessonies-feature/update_unattended_template' ([7b2c0e4f](https://github.com/weareinteractive/ansible-apt/commit/7b2c0e4fadf07feb8ef3a97425a282b38315a44b))



<a name="2.6.1"></a>
### 2.6.1 (2019-09-16)


#### Bug Fixes

*   ensure unattended-upgrades package installation ([03740eea](https://github.com/weareinteractive/ansible-apt/commit/03740eea70fdf744256e708798ea048be22a2a9e))

#### Features

*   add bool check ([1f9f71d3](https://github.com/weareinteractive/ansible-apt/commit/1f9f71d32df59563ebb2fb40b82ddc2e916e9de8))



<a name="2.5.1"></a>
### 2.5.1 (2019-06-17)


#### Features

*   update syntax to ansible 2.8 ([fa5f8740](https://github.com/weareinteractive/ansible-apt/commit/fa5f87400d1d1db233bffcf8ced0b82c6460fd4d))



<a name="2.5.0"></a>
## 2.5.0 (2018-12-12)


#### Features

*   add apt pinning ([349d5b09](https://github.com/weareinteractive/ansible-apt/commit/349d5b09a9b90513da4b66829eca1172da692e96))
*   added apt pinning ([d66994de](https://github.com/weareinteractive/ansible-apt/commit/d66994de87a291cb5a2ebfe2ed4867e290ad68fb))



<a name="2.4.2"></a>
### 2.4.2 (2018-11-01)


#### Features

*   add options to apt_keys and apt_repositories ([f2ce4e0e](https://github.com/weareinteractive/ansible-apt/commit/f2ce4e0e6d41f539610adb34e0ac1093e482677c))
*   added options ([bb80fe88](https://github.com/weareinteractive/ansible-apt/commit/bb80fe8804ee2bac18065b89a8abcadc14f0ed9b))



<a name="2.4.1"></a>
### 2.4.1 (2018-11-01)


#### Bug Fixes

*   fix deprication warning for ansible 2.7 and apt package loops ([556b6445](https://github.com/weareinteractive/ansible-apt/commit/556b6445e748004846c6e16248d9d92b69afd0c3))



<a name="2.5.0"></a>
## 2.5.0 (2018-10-08)




<a name="2.3.1"></a>
### 2.3.1 (2017-12-18)


#### Bug Fixes

*   rename missing include to include_tasks ([da051d29](https://github.com/weareinteractive/ansible-apt/commit/da051d29e279e48061e7e6b41f504a00f1508b16))



<a name="2.3.0"></a>
## 2.3.0 (2017-12-18)


#### Features

*   upgrade tasks for ansible 2.4 ([6e5a1ca4](https://github.com/weareinteractive/ansible-apt/commit/6e5a1ca49a855e7c183446cb4a2d817d58bab59f))



<a name="2.2.0"></a>
## 2.2.0 (2017-08-24)


#### Features

*   add option to alter solution cost ([cfaf694c](https://github.com/weareinteractive/ansible-apt/commit/cfaf694c6ea921e6d6209db0e851c84dd35c8fe2))
*   allow multiple file systems to be remounted ([5cb5a96c](https://github.com/weareinteractive/ansible-apt/commit/5cb5a96cfbdce66f7b5f4d2f7716e1e30279ac98))



<a name="2.1.0"></a>
## 2.1.0 (2017-01-27)


#### Features

*   use builtin autoremove option ([87a34935](https://github.com/weareinteractive/ansible-apt/commit/87a34935874f78d4752f2557c9094496eb51a391))



<a name="2.0.3"></a>
### 2.0.3 (2016-08-18)


#### Bug Fixes

*   fix proxy config conditions ([27787e80](https://github.com/weareinteractive/ansible-apt/commit/27787e80dc805a828af35b7206aae835e9d8b0aa))



<a name="2.0.2"></a>
### 2.0.2 (2016-04-25)


#### Features

*   always get latest unattended-upgrades instead of just present ([a927d6af](https://github.com/weareinteractive/ansible-apt/commit/a927d6afbc0b35481c5eea3623cd5eebf7a3d415))



<a name="2.0.1"></a>
### 2.0.1 (2016-03-22)


#### Features

*   escape bare variables ([96525b39](https://github.com/weareinteractive/ansible-apt/commit/96525b393671352973d81abfcb942272f70dc6bd))



<a name="2.0.0"></a>
## 2.0.0 (2016-03-15)


#### Features

*   update to ansible 2.0 ([052bc675](https://github.com/weareinteractive/ansible-apt/commit/052bc675f01ded71c7bd9bd7e8154ecb2f600c4a))



<a name="1.8.0"></a>
## 1.8.0 (2016-01-11)


#### Features

*   add support for proxy servers ([91ae92f5](https://github.com/weareinteractive/ansible-apt/commit/91ae92f56e7f3fa2f9851adc03235d3985dd7b7e))



<a name="1.7.1"></a>
### 1.7.1 (2015-12-03)


#### Features

*   adds variables to configure apt ([3ec652be](https://github.com/weareinteractive/ansible-apt/commit/3ec652be9513b0d8b9b1bb7f317aa6a4c30256ff))
*   only adds 50unattended-upgrades config if enabled ([14742e5e](https://github.com/weareinteractive/ansible-apt/commit/14742e5ee87bf135edf8756ce9cd197ca65b346d))
*   updates travis tests ([2d1873da](https://github.com/weareinteractive/ansible-apt/commit/2d1873daec0e1b76e4bcafbb898ac63c4b12e91f))
*   using ansible-role to generate README ([3abe7246](https://github.com/weareinteractive/ansible-apt/commit/3abe72463af5d4d101570e233d497a96e910e4ea))
*   adds CHANGELOG ([5f4c6673](https://github.com/weareinteractive/ansible-apt/commit/5f4c66734445e239fb96faec557a6c5e708cd5b3))

#### Bug Fixes

*   fixes quotation marks on 'APT::Periodic::Enable' value ([bf19c900](https://github.com/weareinteractive/ansible-apt/commit/bf19c90034badb1173ad9b204d815d17cd33ba9d))
*   fixes the usage of unattended upgrades ([04f25734](https://github.com/weareinteractive/ansible-apt/commit/04f25734fa29aba48ec3f9461c9488785bfe8ae3))



<a name="1.7.0"></a>
## 1.7.0 (2015-11-30)


#### Features

*   adds variables to configure apt ([3ec652be](https://github.com/weareinteractive/ansible-apt/commit/3ec652be9513b0d8b9b1bb7f317aa6a4c30256ff))
*   only adds 50unattended-upgrades config if enabled ([14742e5e](https://github.com/weareinteractive/ansible-apt/commit/14742e5ee87bf135edf8756ce9cd197ca65b346d))
*   updates travis tests ([2d1873da](https://github.com/weareinteractive/ansible-apt/commit/2d1873daec0e1b76e4bcafbb898ac63c4b12e91f))
*   using ansible-role to generate README ([3abe7246](https://github.com/weareinteractive/ansible-apt/commit/3abe72463af5d4d101570e233d497a96e910e4ea))
*   adds CHANGELOG ([5f4c6673](https://github.com/weareinteractive/ansible-apt/commit/5f4c66734445e239fb96faec557a6c5e708cd5b3))

#### Bug Fixes

*   fixes the usage of unattended upgrades ([04f25734](https://github.com/weareinteractive/ansible-apt/commit/04f25734fa29aba48ec3f9461c9488785bfe8ae3))



