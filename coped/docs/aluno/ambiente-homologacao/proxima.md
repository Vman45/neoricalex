export VAGRANT_WSL_ENABLE_WINDOWS_ACCESS="1"
export PATH="$PATH:/mnt/c/Program Files/Oracle/VirtualBox" 
export VAGRANT_WSL_WINDOWS_ACCESS_USER_HOME_PATH="/mnt/e/Development"

config.vm.provider:
    v.customize [ 
        "modifyvm", :id, "--uartmode1", "disconnected" 
        ]

<!--vagrant@vagrant-10:/mnt/c/Users/vagrant$ export DOCKER_HOST=tcp://127.0.0.1:2375-->