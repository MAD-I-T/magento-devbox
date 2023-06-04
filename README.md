Docker infrastructure for Magento development

A magento docker devbox that takes 5min to lean and 3 min to start (tested on linux and mac)

Inspired by https://github.com/kandy/dev-docker 

# Usage
- Checkout this repository
- Copy your magento sources in `src/magento` dir with auth.json
- Install docker using [official guidelines](https://docs.docker.com/install/)
- Install docker compose using the same guidelines
- Install [mutagen](https://mutagen.io/documentation/introduction/installation)
- Run 
  ```
    ./mdev up
    ./mdev init
    ./mdev install
  ```

<h4>Tutorial in video </h4>
<div align="center">
  <a href=" https://youtu.be/WD4zuprVV-s"><img src="https://user-images.githubusercontent.com/3765910/243196278-082abc41-1b92-4ec6-b8df-b1718d74b7ec.png" alt="magento local devbox on docker"></a>
</div>
  
#### To stop and (re)start existing project
- Run
  ```
    ./mdev stop
    ./mdev up
  ```

#### Default credentials

  admin-user=admin \
  admin-password=123123q

#### Run command line in container
  E.g disable two factor auth modules
  ```
  ./mdev exec app bash -c ' bin/magento module:disable Magento_TwoFactorAuth Magento_AdminAdobeImsTwoFactorAuth'
  ```

