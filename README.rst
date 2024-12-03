Electrum Digital Cash (Dash) Wallet
=====================================


**Electrum Dash** is a lightweight and secure wallet for the Dash cryptocurrency.
It is designed to provide fast transactions, enhanced security, and cross-platform compatibility.  


Features  
=============

- **Secure and Reliable**: Protects your funds with advanced encryption.  
- **Lightweight**: Quick to download and sync, saving you time and resources.  
- **Multi-platform**: Available on Windows, macOS, and Linux.  
- **Hardware Wallet Integration**: Supports devices like Ledger and Trezor.  
- **Instant Transactions**: Optimized for Dash's InstantSend functionality. 


This project is licensed under the MIT License. See the `LICENSE`_ for details.

.. _LICENSE: https://github.com/Electrum-Digital-Cash/electrum-dash/blob/master/LICENCE


1. GETTING STARTED
------------------

To run Electrum from this directory, just do::

    ./electrum

If you install Electrum on your system, you can run it from any
directory.

If you have pip, you can do::

    python setup.py sdist
    sudo pip install --pre dist/Electrum-2.0.tar.gz


If you don't have pip, install with::

    python setup.py sdist
    sudo python setup.py install



To start Electrum from your web browser, see
http://electrum.org/bitcoin_URIs.html



2. HOW OFFICIAL PACKAGES ARE CREATED
------------------------------------

On Linux/Windows::

    pyrcc4 icons.qrc -o gui/qt/icons_rc.py
    python setup.py sdist --format=zip,gztar

On Mac OS X::

    # On port based installs
    sudo python setup-release.py py2app

    # On brew installs
    ARCHFLAGS="-arch i386 -arch x86_64" sudo python setup-release.py py2app --includes sip

    sudo hdiutil create -fs HFS+ -volname "Electrum" -srcfolder dist/Electrum.app dist/electrum-VERSION-macosx.dmg
