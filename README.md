# Captcha Server
### A simple client-server architecture example written in C
The example consists of a CLI server and a GUI client communicating over a TCP connection on the localhost. It was written for Linux and uses POSIX libraries and the GTK graphical user interface toolkit.

The example includes two types of captchas that are generated by the server and can be completed on the client. Feedback is shown whether the attempt was successful, and the server keeps track of failed attempts and overall success/fail statistics in log files.

## Building
#### The project was tested with Ubuntu 22.04 LTS
First, install the dependencies with the following command:

    $ sudo apt install build-essential git meson ninja-build libgtk-4-dev

Then you can build with the following commands:

    $ git clone https://github.com/alexb271/captcha
    $ cd captcha
    $ meson setup build
    $ cd build
    $ ninja

Once you have compiled the binaries, you can start the server first with:

    $ ./server

And then the client from a different tab:

    $ ./client

## Testing
#### Important! Make sure that the server is running before launching tests.
You can run unit tests with the following command:

    $ meson test
