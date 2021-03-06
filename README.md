# Minimal C kernel for Jupyter

## Use with MyBinder (recommended)

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/LaGuer/jupyter-c-kernel/master)
[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/LaGuer/jupyter-c-kernel/master?urlpath=lab%2Ftree%2Fexample-notebook.ipynb)

## Use with Docker 

 * `docker pull linexus/jupyter-c-kernel`
 * `docker run -p 8888:8888 linexus/jupyter-c-kernel`
 * Copy the given URL containing the token, and browse to it. For instance:
 
 ```
 Copy/paste this URL into your browser when you connect for the first time,
 to login with a token:
    http://localhost:8888/?token=66750c80bd0788f6ba15760aadz53beb9a9fb4cf8ac15ce8
 ```

## Manual installation

Works only on Linux and OS X. Windows is not supported yet. If you want to use this project on Windows, please use Docker.


 * Make sure you have the following requirements installed:
  * gcc
  * jupyter
  * python 3
  * pip

### Step-by-step:
 * `pip install jupyter-c-kernel`
 * `install_c_kernel`
 * `jupyter-notebook`. Enjoy!

## Example of notebook

![Example of notebook](example-notebook.png?raw=true "Example of notebook")

## Custom compilation flags

You can use custom compilation flags like so:

![Custom compulation flag](custom_flags.png?raw=true "Example of notebook using custom compilation flags")

Here, the `-lm` flag is passed so you can use the math library.

## Contributing

The docker image installs the kernel in editable mode, meaning that you can
change the code in real-time in Docker. For that, just run the docker box like
that:

```bash
git clone https://github.com/brendan-rius/jupyter-c-kernel.git
cd jupyter-c-kernel
docker run -v $(pwd):/tmp/jupyter_c_kernel/ -p 8888:8888 linexus/jupyter-c-kernel
```

This clones the source, run the kernel, and binds the current folder (the one
you just cloned) to the corresponding folder in Docker.
Now, if you change the source, it will be reflected in [http://localhost:8888](http://localhost:8888)
instantly. Do not forget to click "restart" the kernel on the page as it does
not auto-restart.

## License

[MIT](LICENSE.txt)
