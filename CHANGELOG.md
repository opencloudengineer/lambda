## [0.6.2](https://github.com/opencloudengineer/lambda/compare/v0.6.1...v0.6.2) (2024-02-28)


### Bug Fixes

* **ci:** rm flag --charts-repo from cr ([57139be](https://github.com/opencloudengineer/lambda/commit/57139be216576a9ba753dd9021f06354f47de83a))



## [0.6.1](https://github.com/opencloudengineer/lambda/compare/v0.6.0...v0.6.1) (2024-02-28)


### Bug Fixes

* gotta manually install hub now ([c782581](https://github.com/opencloudengineer/lambda/commit/c7825818b9ebafbde2ad3c06fad59470047288f3))



# [0.6.0](https://github.com/opencloudengineer/lambda/compare/v0.5.4...v0.6.0) (2024-02-28)


### Bug Fixes

* cr install without brew in ci ([50ee379](https://github.com/opencloudengineer/lambda/commit/50ee3794676cf64eccd48f1f5664a091c58dc3b3))
* rm ./ ([4410b72](https://github.com/opencloudengineer/lambda/commit/4410b72567e74f9d31a470bc17c6e3affa75cab6))


### Features

* upgrade base image version in dockerfile ([71874a6](https://github.com/opencloudengineer/lambda/commit/71874a6efaf8a01e5800274dcc87c5a10f57185a))



## [0.5.4](https://github.com/opencloudengineer/lambda/compare/v0.5.3...v0.5.4) (2021-01-19)


### Bug Fixes

* escape `auto_database_uri` function call in `cat <<EOF` in deploy function ([d09a40f](https://github.com/opencloudengineer/lambda/commit/d09a40f55fa6d7fcedbbd283b380a2cd5b47da69))



## [0.5.3](https://github.com/opencloudengineer/lambda/compare/v0.5.2...v0.5.3) (2021-01-19)


### Bug Fixes

* `echo "${MARIADB_URI-$uri}"` for `case "${db}" in mariadb` in auto_database_uri function ([5617e9b](https://github.com/opencloudengineer/lambda/commit/5617e9b1e4d3756bb67ccc0f3c326268cafb4dfe))



## [0.5.2](https://github.com/opencloudengineer/lambda/compare/v0.5.1...v0.5.2) (2021-01-19)


### Bug Fixes

* `${1}` instead of `${i}` in install_app function ([89e622c](https://github.com/opencloudengineer/lambda/commit/89e622ca9f1a248f34b6fc5c0c2b65752477cfb8))



## [0.5.1](https://github.com/opencloudengineer/lambda/compare/v0.5.0...v0.5.1) (2021-01-18)


### Bug Fixes

* write `application.*db_uri` to `${AUTO_DEPLOY_ENVIRONMENT_VALUES_FILE}` only if `*DB_ENABLED` is true ([9c58d0d](https://github.com/opencloudengineer/lambda/commit/9c58d0dbbf82e7e9aa0b5b789af1a3119dccf650))



# [0.5.0](https://github.com/opencloudengineer/lambda/compare/v0.4.0...v0.5.0) (2021-01-18)


### Features

* setup install_app function to install DB helm charts of choice ([4a1fbc0](https://github.com/opencloudengineer/lambda/commit/4a1fbc0c206a28eb62668c025f68a297ab691fee))
* setup Redis & MongoDB specific dynamic helm values ([e620b2c](https://github.com/opencloudengineer/lambda/commit/e620b2cf72b23abe0305b244424365f374404d1a))



# [0.4.0](https://github.com/opencloudengineer/lambda/compare/v0.3.1...v0.4.0) (2021-01-15)


### Bug Fixes

* if `application.*db_uri` is null then don't create a env var `*DB_URI` for it in Pod ([2b37dfb](https://github.com/opencloudengineer/lambda/commit/2b37dfbddd71c0027be7a6517df4ff6970aa01bf))
* remove Chart.lock as dependent charts will be handled/installed separately ([dd09ec0](https://github.com/opencloudengineer/lambda/commit/dd09ec0591377bb50a611b8f61370b05922a3fdd))


### Features

* use yq to generate the dynamic values.yaml in `write_environment_values_file` function ([2f4fee1](https://github.com/opencloudengineer/lambda/commit/2f4fee1a10cac60d3580773a0ef2e171d3d0fd91))
* yq in docker image ([b05a559](https://github.com/opencloudengineer/lambda/commit/b05a5594b6002199f2c6077aed7abb2f63084e19))



## [0.3.1](https://github.com/opencloudengineer/lambda/compare/v0.3.0...v0.3.1) (2021-01-14)


### Bug Fixes

* configure auto_database_uri function to return URI for the DB passed as $1 ([54f8ae9](https://github.com/opencloudengineer/lambda/commit/54f8ae9ac0773ac65acdf9da51531c7ed12b5cd7))
* use `$CI_PROJECT_ID-$CI_COMMIT_REF_SLUG` instead of `$CI_PROJECT_PATH_SLUG` in env:url ([725d987](https://github.com/opencloudengineer/lambda/commit/725d9873d73917ae1c878f2a5667eda8d549ae32))



# [0.3.0](https://github.com/opencloudengineer/lambda/compare/v0.2.0...v0.3.0) (2021-01-13)


### Features

* add auto-deploy.gitlab-ci.yml & rm unnecessary code in auto-deploy ([c89e89d](https://github.com/opencloudengineer/lambda/commit/c89e89d88e7f58e99b56aee462f0d774ddda6749))
* add preCommit logic to change docker image version in auto-deploy.gitlab-ci.yml upon new releases ([e853201](https://github.com/opencloudengineer/lambda/commit/e8532014c9277695c629e7845f7a9aeef213ac28))
* set chart's & its app's version auto-deploy ([9d5f143](https://github.com/opencloudengineer/lambda/commit/9d5f14362c8bab7d35698c8dad3858c467329ae1))



# [0.2.0](https://github.com/opencloudengineer/lambda/compare/v0.1.0...v0.2.0) (2021-01-10)


### Features

* add gitlab related annotations when CI is gitlab ([e963154](https://github.com/opencloudengineer/lambda/commit/e96315422347cfa40977db26d093ea0ef191ccaf))
* store chart in docker image as chart version & docker image tag will be same ([cb412dd](https://github.com/opencloudengineer/lambda/commit/cb412dd86934baaebb08ea1fd2d7e827fa341bf3))



# [0.1.0](https://github.com/opencloudengineer/lambda/compare/34516f51635cafce9d9ffc83eb8f5278187cd1f9...v0.1.0) (2021-01-10)


### Bug Fixes

* always lint all charts && pass connection URI for all DBs as env var ([46fa9f7](https://github.com/opencloudengineer/lambda/commit/46fa9f793cc0d7a2bb60260e0907ce0cedb8d6e7))
* homepage link && setup custom annotations from project.* ([c26f189](https://github.com/opencloudengineer/lambda/commit/c26f1890d7fb21934f8bcd7e301818d7c2d70117))


### Features

* add action to build & push Dockerfile ([dd1f573](https://github.com/opencloudengineer/lambda/commit/dd1f5733b6f240ed7f5fbe835c22051f7b90112c))
* add lambda helm chart && github action ([34516f5](https://github.com/opencloudengineer/lambda/commit/34516f51635cafce9d9ffc83eb8f5278187cd1f9))
* docker build & push && release auto-deploy only when new tag is created by Conventional Changelog Action ([9628137](https://github.com/opencloudengineer/lambda/commit/9628137c19247dcccb17aaa3a9e65b2ad36b43df))
* improve github action workflow - lint -> package -> tag & changelog & update version -> release -> gh-pages -> docker build & push ([7cc1baf](https://github.com/opencloudengineer/lambda/commit/7cc1baf47383e330a8df3c38910802eb1fecae73))



