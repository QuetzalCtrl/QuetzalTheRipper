# Quetzal the Ripper password cracker, version 1.0.0

Quetzal the Ripper is a home-made Password cracker in bash, created for educational purposes only. 
```
===========================================================================
                 ___             _            _ 
                / _ \ _   _  ___| |_ ______ _| |
               | | | | | | |/ _ \ __|_  / _\`| |
               | |_| | |_| |  __/ |_ / / (_| | |
                \__\_\\__,_|\___|\__/___\__,_|_|

        Quetzal the Ripper password cracker, version 1.0.0
        by QuetzalCoatl, https://github.com/QuetzalCtrl/
        contact me : hugo.vrbs@gmail.com

===========================================================================
```

## System Requirements

- Only available for Linux systems

- Openssl:

	By default, it is already installed in most Linux systems. 
	
	But if that isn’t the case in yours, you will need to install it before using this tool.

## Installation

To install this tool from the git repository, follow these steps:

- Clone the repository to your local machine:

  ```git clone https://github.com/QuetzalCtrl/QuetzalTheRipper.git```

- Navigate to the directory where the repository was cloned:

  `cd QuetzalTheRipper`

- Install the tool using the installation script:

  `chmod +x install.sh && ./install.sh`

## Usage

To use Quetzal the Ripper, run the following command:

`quetzal [options]`

### Options

```
-h=HASH, --hash=HASH            hashed password to crack, stdin used if HASH not specified
-h, --help                      display this summary
-l, --list                      list all the hash type NAME supported
-v, --verbose                   verbose mode, display detailled progression
-f=NAME, --format=NAME          force hash type NAME
-w=FILE, --wordlist=FILE        read words from FILE
-o=FILE, --out=FILE             output to FILE rather than stdout
 ```

### Examples

To crack a sha3-384 hash stored in a text file, using the small.txt wordlist:

`cat hash.txt | quetzal -f=sha3-384 -w=small.txt`

To list the available hash types:

`quetzal -l`

To crack a md5 hash in verbose mode, using the rockyou.txt wordlist:

`quetzal --hash=0f4137ed1502b5045d6083aa258b5c42 --formatf=md5 --wordlist=rockyou.txt --verbose`

