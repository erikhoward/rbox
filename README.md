[![MIT License](https://img.shields.io/github/license/mashape/apistatus.svg)](LICENSE.md)

![rBox](toolbox.png)

# rBox - Data Science and Machine Learning R Containers
`rBox` is a set of Docker containers for performing data science and machine learning research using R.

## Quick Start

To start an interactive **rbox** Docker container:

```sh
docker run --rm -it \
    --name rbox \
    erikhoward/rbox-base:0.5.0
    /bin/bash
```

## Contributing

For a complete guide on contributing to **rBox** see [contributing to rBox](CONTRIBUTING.md).

We welcome contributions of any kind to **rBox** including documentation, examples, bug fixes, tutorials, blog posts, feature requests, feature implementations, help answering questions, etc.

## Bugs and Feature Requests

Found a bug? Have a feature request? Found something missing in the documentation? Let me know by [creating a new issue](https://github.com/erikhoward/rbox/issues/new).

## TODO

- [ ] Add RStudio
- [ ] Add tidyverse
- [ ] Add shiny support