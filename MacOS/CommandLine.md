/*
 * @Author: kelton.xian 
 * @Date: 2018-10-07 12:47:25 
 * @Last Modified by: kelton.xian
 * @Last Modified time: 2018-10-07 12:53:47
 */

# Install CMake on MacOS
    brew install cmake
#### 如提示Error: Cannot write to /usr/local/Cellar，则输入
    sudo chmod a+w /usr/local/Cellar/
#### 如提示Error: Permission denied - /Library/Caches/Homebrew/Formula/cmake.brewing，则输入
    sudo chown -R ${USER} /Library/Caches/Homebrew/
#### 如提示/bin/sh: cmake: command not found，则在~/.profile中加入
    export PATH=/usr/local/Cellar/cmake/3.2.2/bin:$PATH

# Pack IPA on MacOS
    #!/bin/sh

    name=$1
    rm -rf ${name}
    mkdir ${name}
    mkdir ${name}/Payload
    cp -r ${name}.app ${name}/Payload/${name}.app
    cp Icon.png ${name}/iTunesArtwork
    cd ${name}
    zip -r ${name}.ipa Payload iTunesArtwork
    exit 0

# Install IPA to device on MacOS
#### 安装命令
    ideviceinstaller -i target.ipa
#### 如缺失ideviceinstaller，则安装
    brew install ideviceinstaller
#### 如提示Homebrew must be run under Ruby 2.3，则安装
    curl -L get.rvm.io | bash -s stable
    rvm install 2.4
#### 如提示Error: Xcode alone is not sufficient on Sierra，则安装
    xcode-select --install
#### 如提示Could not connect to lockdownd. Exiting，则输入
    sudo chmod -R 777 /var/db/lockdown/