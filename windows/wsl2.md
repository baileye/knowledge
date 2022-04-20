# Windows Subsystem for Linux 2 (WSL2)

WSL lets you install Linux terminal and run it within Windows. It's not 100% identical to running a dedicated Linux box, but it's super iseful and helpful for day-to-day tasks when in Windows and doens't require a VM. I run Ubuntu and Debian.

## Set up Ubuntu

The [WSL Docs](https://docs.microsoft.com/en-us/windows/wsl/about) will contain the latest set up and isntall steps to get Ubuntu on your machine. Personal to me I like to set up the following:

 - Git
    - `git config --global user.name = "Me"`
    - `git config --global user.email = "me@example.org"`
    - New SSH key: `ssh-keygen -t ed25519 -C "me@example.org"`
 - Oh-my-zsh
    - Install zsh
    - Install oh-my-zsh
    - [zsh autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
    - [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)
    - [Powershell 10k (zsh)](https://github.com/romkatv/powerlevel10k)
 - rbenv
    - [Install](https://github.com/rbenv/rbenv#installation)
    - `rbenv install -l` (list lasted ruby versions)
    - `rbenv global 3.1.1`
 - tfenv
    - [Install](https://github.com/tfutils/tfenv#installation)
    - `sudo apt install unzip`
    - `tfenv install 1.1.8`
    - `tfenv use 1.1.8`

## Notify-Send replacement

notify-send is a little tool to send a notification from your terminal. Stuart Leeks has written a 
[tool](https://github.com/stuartleeks/wsl-notify-send) to get this working in WSL2 and sending a 
notification to the Windows Toast notification.

Handy for long-running processes, when I want to know if they're finished, e.g.:

`terraform apply --auto-approve; notify-send "Terraform apply complete"`

## Links

 - [WSL Docs](https://docs.microsoft.com/en-us/windows/wsl/about)
 - [New SSH key - add to SSH agent](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
 - [Oh-mh-zsh](https://github.com/ohmyzsh/ohmyzsh)
 - [rbenv Digital Ocean guide](https://www.digitalocean.com/community/tutorials/how-to-install-ruby-on-rails-with-rbenv-on-ubuntu-20-04)
