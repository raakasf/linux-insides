linux-insides
===============

A book-in-progress about the linux kernel and its insides.

**The goal is simple** - to share my modest knowledge about the insides of the linux kernel and help people who are interested in linux kernel insides, and other low-level subject matter. Feel free to go through the book [Start here](https://github.com/raakasf/linux-insides/blob/master/SUMMARY.md)

**Questions/Suggestions**: Feel free about any questions or suggestions by pinging me at twitter [@0xAX](https://twitter.com/0xAX), adding an [issue](https://github.com/0xAX/linux-insides/issues/new) or just drop me an [email](mailto:anotherworldofworld@gmail.com).

# Mailing List

We have a Google Group mailing list for learning the kernel source code. Here are some instructions about how to use it.

#### Join

Send an email with any subject/content to `kernelhacking+subscribe@googlegroups.com`. Then you will receive a confirmation email. Reply it with any content and then you are done.

> If you have Google account, you can also open the [archive page](https://groups.google.com/forum/#!forum/kernelhacking) and click **Apply to join group**. You will be approved automatically.

#### Send emails to mailing list

Just send emails to `kernelhacking@googlegroups.com`. The basic usage is the same as other mailing lists powered by mailman.

#### Archives

https://groups.google.com/forum/#!forum/kernelhacking

Support
-------

**Support** If you like `linux-insides` you can support me with: 

[![Support with bitcoin](https://img.shields.io/badge/donate-bitcoin-green.svg)](https://www.coinbase.com/checkouts/0bfa452a41cf52c0b3f99500b4f31685) [![Join the chat at https://gitter.im/0xAX/linux-insides](https://badges.gitter.im/0xAX/linux-insides.svg)](https://gitter.im/0xAX/linux-insides?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

On other languages
-------------------

  * [Brazilian Portuguese](https://github.com/mauri870/linux-insides)
  * [Chinese](https://github.com/MintCN/linux-insides-zh)
  * [Japanese](https://github.com/tkmru/linux-insides-ja)
  * [Korean](https://github.com/junsooo/linux-insides-ko)
  * [Russian](https://github.com/proninyaroslav/linux-insides-ru)
  * [Spanish](https://github.com/leolas95/linux-insides)
  * [Turkish](https://github.com/ayyucedemirbas/linux-insides_Turkish)

Docker
------

In order to run your own copy of the book with gitbook within a local container:

1. Enable Docker experimental features with vim or another text editor
   ```bash
    sudo vim /usr/lib/systemd/system/docker.service
   ```

   Then add --experimental=true to the end of the ExecStart=/usr/bin/dockerd -H fd:// line and save.

   Eg: *ExecStart=/usr/bin/dockerd -H fd:// --experimental=true*

   Then, you need to reload and restart the Docker daemon:
   ```bash
    systemctl daemon-reload
    systemctl restart docker.service
   ```

2. Build container image
   ```bash
   docker image build \
       --rm --squash \
       --label linux-insides \
       --tag linux-insides-book:latest \
       -f Dockerfile .
   ```

3. Create and run book in local container
   ```bash
   docker run \
       --detach \
       --rm \
       -p 4000:4000 \
       --name linux-insides-book \
       --hostname linux-insides-book \
       linux-insides-book
   ```

4. Open your local copy of linux insides book under this url
   http://localhost:4000

Contributions 
--------------

Feel free to create issues or pull-requests if you have any problems.

**Please read [CONTRIBUTING.md](https://github.com/0xAX/linux-insides/blob/master/CONTRIBUTING.md) before pushing any changes.**

![linux-kernel](Assets/linux-kernel.png)

Author
---------------

[@0xAX](https://twitter.com/0xAX)

LICENSE
-------------

Licensed [BY-NC-SA Creative Commons](http://creativecommons.org/licenses/by-nc-sa/4.0/).
