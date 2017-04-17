# api documentation for  [kafka-node (v1.6.0)](https://github.com/SOHU-Co/kafka-node#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-kafka-node.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-kafka-node) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-kafka-node.svg)](https://travis-ci.org/npmdoc/node-npmdoc-kafka-node)
#### Client for Apache Kafka v0.8+

[![NPM](https://nodei.co/npm/kafka-node.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/kafka-node)

- [https://npmdoc.github.io/node-npmdoc-kafka-node/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-kafka-node/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-kafka-node/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-kafka-node/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-kafka-node/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-kafka-node/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "bugs": {
        "url": "https://github.com/SOHU-co/kafka-node/issues"
    },
    "dependencies": {
        "async": ">0.9 <2.0",
        "binary": "~0.3.0",
        "buffer-crc32": "~0.2.5",
        "buffermaker": "~1.2.0",
        "debug": "^2.1.3",
        "lodash": "^4.17.4",
        "minimatch": "^3.0.2",
        "nested-error-stacks": "^2.0.0",
        "node-zookeeper-client": "~0.2.2",
        "optional": "^0.1.3",
        "retry": "^0.10.1",
        "snappy": "^5.0.5",
        "uuid": "^3.0.0"
    },
    "description": "Client for Apache Kafka v0.8+",
    "devDependencies": {
        "coveralls": "^2.11.12",
        "doctoc": "^1.2.0",
        "eslint": "^3.7.0",
        "eslint-config-semistandard": "^7.0.0",
        "eslint-config-standard": "^6.2.0",
        "eslint-plugin-dependencies": "^1.3.0",
        "eslint-plugin-promise": "^3.4.0",
        "eslint-plugin-standard": "^2.0.1",
        "istanbul": "^0.4.4",
        "mocha": "^3.1.0",
        "nsp": "^2.6.2",
        "optimist": "^0.6.1",
        "proxyquire": "^1.7.10",
        "should": "^6.0.0",
        "sinon": "^1.17.2"
    },
    "directories": {},
    "dist": {
        "shasum": "c8c4b779610a45c53b7a5d177c20f63b46d36f87",
        "tarball": "https://registry.npmjs.org/kafka-node/-/kafka-node-1.6.0.tgz"
    },
    "engines": {
        "node": ">4.4.7"
    },
    "files": [
        "kafka.js",
        "logging.js",
        "lib"
    ],
    "gitHead": "a9f22e134f78dfc8aeeac8deee6331492dd7ceed",
    "homepage": "https://github.com/SOHU-Co/kafka-node#readme",
    "keywords": [
        "kafka",
        "zookeeper",
        "consumer",
        "producer",
        "broker"
    ],
    "license": "MIT",
    "main": "kafka.js",
    "maintainers": [
        {
            "name": "estliberitas"
        },
        {
            "name": "haio"
        },
        {
            "name": "hyperlink"
        }
    ],
    "name": "kafka-node",
    "optionalDependencies": {
        "snappy": "^5.0.5"
    },
    "repository": {
        "type": "git",
        "url": "git+https://github.com/SOHU-Co/kafka-node.git"
    },
    "scripts": {
        "startDocker": "./start-docker.sh",
        "stopDocker": "docker-compose down",
        "test": "eslint . && ./run-tests.sh && nsp check",
        "updateToc": "doctoc README.md --maxlevel 2 --notitle"
    },
    "version": "1.6.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
