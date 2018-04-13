# Crypton Core [CRN]

![alt text](https://avatars2.githubusercontent.com/u/38019859?s=150&v=4)

## What is Crypton? 
Crypton is a cryptocurrency like Bitcoin, although it does not use SHA256 as its proof of work (POW). Taking development cues from Tenebrix, Litecoin, Dogecoin, Crypton currently employs a simplified variant of scrypt.

http://crncoin.io/

## Development and contributions
Development is ongoing, and the development team, as well as other volunteers, can freely work in their own trees and submit pull requests when features or bug fixes are ready.

### Version strategy

Version numbers are following major.minor.patch semantics.

### Branches
There are 2 types of branches in this repository:

* master: Stable, contains the latest version of the latest major.minor release.
    
* development: Unstable, contains new code for planned releases. Format: <version>-dev

Master branch is exclusively mutable by release. Planned releases will always have a development branch and pull requests should be submitted against those. Please submit new features against the development branch with the highest version.

## Frequently Asked Questions

### How much CRN can exist?

In Crypton it could be approximately 10^77 coins.

Crypton network starts with 1,000,000,000,000,000 coins. The goal is to make transactions as low cost as possible.

Each subsequent block will grant 500 coins to encourage miners to continue to secure the network and make up for lost wallets on hard drives/phones/lost encryption passwords/etc.

### How to get CRN?

Crypton uses a simplified variant of the scrypt key derivation function as its proof of work with a target time of 30 seconds per block and difficulty readjustment after every block. The block rewards are fixed. A permanent reward of 500 Crypton per block is paid.

### How to make Cryptond/Crypton-cli/Crypton-qt ?

The following are developer notes on how to build Crypton on your native platform. They are not complete guides, but include notes on the necessary libraries, compile flags, etc.

* [OSX Build Notes](https://github.com/crypton-dev/crypton/blob/master/doc/build-osx.md)

* [Unix Build Notes](https://github.com/crypton-dev/crypton/blob/master/doc/build-unix.md)

* [Windows Build Notes](https://github.com/crypton-dev/crypton/blob/master/doc/README_windows.txt)

## We use these ports 

`RPC 44777` `P2P 22556`

### Translations

Changes to translations, as well as new translations, can be submitted to Bitcoin Core's Transifex page.

Periodically the translations are pulled from Transifex and merged into the git repository. See the [translation process](https://github.com/crypton-dev/crypton/blob/master/doc/translation_process.md) for details on how this works.

If the changes are Crypton specific, they can be submitted as pull requests against this repository. If it is a general translation, consider submitting it through upstream, as we will pull these changes later on.

## Development tips and tricks

### compiling for debugging

Run configure with the `--enable-debug` option, then make. Or run configure with `CXXFLAGS="-g -ggdb -O0"` or whatever debug flags you need.

### debug.log

If the code is behaving strangely, take a look in the `debug.log` file in the data directory; error and debugging messages are written there.

The -debug=... command-line option controls debugging; running with just -debug will turn on all categories (and give you a very large debug.log file).

The Qt code routes `qDebug()` output to debug.log under category "qt": run with `-debug=qt` to see it.

### DEBUG_LOCKORDER

Crypton Core is a multithreaded application, and deadlocks or other multithreading bugs can be very difficult to track down. Compiling with `-DDEBUG_LOCKORDER` (configure `CXXFLAGS="-DDEBUG_LOCKORDER -g"`) inserts run-time checks to keep track of which locks are held, and adds warnings to the debug.log file if inconsistencies are detected.

## License

Crypton is released under the terms of the MIT license. See http://opensource.org/licenses/MIT for more information.

## Under Development

Mobile applications
Overlay smart contract network

