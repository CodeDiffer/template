# cdff template


每个 project 都至少有两个 branch (master 和 travis)


#### .travis.yml

``` yaml
language: python3.5
branches:
  only:
  - travis
before_install:
- openssl aes-256-cbc -K $encrypted_6ee1cee3745d_key -iv $encrypted_6ee1cee3745d_iv
  -in id_rsa.enc -out ~/.ssh/id_rsa -d
- chmod 600 ~/.ssh/id_rsa
- eval $(ssh-agent)
- ssh-add ~/.ssh/id_rsa
- cp ssh_config ~/.ssh/config
- git config --global user.name "fate0"
- git config --global user.email "fate0@fatezero.org"
install:
- id
script:
- id

notifications:
  webhooks: https://webhooks.gitter.im/e/e77a55bd8dd56a15fe6b
```
