/*
 * @Author: kelton.xian 
 * @Date: 2018-10-03 18:34:58 
 * @Last Modified by:   kelton.xian 
 * @Last Modified time: 2018-10-03 18:34:58 
 */

# .profile
    export PS1='\h : \w \$ '

    export EDITOR=vi

    export ANDROID_SDK_ROOT=/Users/kelton/Documents/sdk/android_sdk
    export ANDROID_HOME=$ANDROID_SDK_ROOT
    export ANDROID_NDK_ROOT=/Users/kelton/Documents/sdk/android-ndk-r10d
    export NDK_ROOT=$ANDROID_NDK_ROOT
    export ANT_ROOT=/usr/local/apache-ant-1.9.4/bin
    export PATH=${PATH}:${ANT_ROOT}
    #export PATH=$PATH:/usr/local/bin
    export PATH=$PATH:$ANDROID_SDK_ROOT
    export PATH=$PATH:$ANDROID_SDK_ROOT/tools:$ANDROID_SDK_ROOT/platform-tools
    export PATH=$PATH:$ANDROID_NDK_ROOT
    export PATH=$PATH:/usr/local/mysql/bin

    alias cdasset="cd ~/Library/Unity/Asset\ Store-5.x/"

    # Add RVM to PATH for scripting. Make sure this is the last PATH variable change.
    export PATH="$PATH:$HOME/.rvm/bin"

    [[ -s "$HOME/.rvm/scripts/rvm" ]] && source "$HOME/.rvm/scripts/rvm" # Load RVM into a shell session *as a function*