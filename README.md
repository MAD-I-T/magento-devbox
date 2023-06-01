Docker infrastructure for Magento development

A magento docker devbox that takes 5min to lean and 3 min to start (tested on linux and mac)

Inspired by https://github.com/kandy/dev-docker 

# Usage
- Checkout this repository
- Copy your magento sources in src dir
- Install docker using [official guidelines](https://docs.docker.com/install/)
- Install docker compose using the same guidelines
- Install [mutagen](https://mutagen.io/documentation/introduction/installation)
- Run 
  ```
    ./mdev up
    ./mdev init
    ./mdev install
  ```
  
####To stop and (re)start existing project
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

