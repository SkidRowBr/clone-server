# clone-server
A Linux Based disk cloning "server"

OK, so there it goes, this is basicaly an alias i created on my work to make it easier to format and configure new Pc's, since there was a lot of programs and configs we should be doing after just installing the system image, this tool just does everything for us nice and easy.
Also, you might want to note that this is running on latest ubuntu distro, so, some commands like Zenity often change a bit, just make sure to check if everything will work properly before running the command, you don't want to mess things up.

    *The alias:* <alias clonar='zenity --question --text="Deseja iniciar o processo de Clonagem? todas as partições do HD clonado serão deletadas!!!" && wipefs -a /dev/sdc && echo -e "\e[31mPartições Deletadas, Clonagem Iniciada!" && dd if=/dev/sda of=/dev/sdc bs=64k conv=noerror,sync status=progress && echo-e "\e[32mClonagem finalizada, por favor verifique a existencia de erros.";

The "if" and "of" specify the targets, so the "if" sends to the "of", in my case i'm using sda and sdc because sdb is a second HDD on the server running other distro that i don't want cloned, the sdc gotta be an easy removable hard disk because it's receiving the cloning and should be sent to the final user later, so make sure to get the wiring in a way that it's easy to install and remove the third (or second) HDD. i hope it helps you in any way, its pretty simple and i'm thinking on turnin it in to a function later instead of an alias but it does the job as it is. :)
  
