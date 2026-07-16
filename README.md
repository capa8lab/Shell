# Shell

## Propmpt Personalizada

pasos:

* abre y pega esto en tu terminal

````bash
$ nano ~/.bashrc
````

* pega lo siguiente hasta abajo de tu archivo `.bashrc` ya que te permitira tener tu prompt personalizado

````bash
case "$(grep '^ID=' /etc/os-release | cut -d= -f2 | tr -d '"')" in
    arch)     distro_logo="󰣇" ;;
    ubuntu)   distro_logo="󰕈" ;;
    debian)   distro_logo="󰣚" ;;
    fedora)   distro_logo="󰣛" ;;
    linuxmint)distro_logo="󰣭" ;;
    opensuse*)distro_logo="" ;;
    *)        distro_logo="🐧" ;;
esac

PS1="${distro_logo} session: \u ❯ "
````

* Das Guardas (Ctrl + o) Das enter y sales (Ctrl + x)
* Recargas tu consola con el siguiente comando

````bash
$ source /.bashrc
````
