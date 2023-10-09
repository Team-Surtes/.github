# Welcome to Team SURTES' Codespace
You'll find all of the code we're working on at the moment here in this organisation.

## Tech Stack
We're running WordPress, the [roots.io](roots.io/) way:
- [Trellis](roots.io/trellis) (Virtual Machine)
- [Bedrock](roots.io/bedrock) (Restructured WordPress Folder Structure)
- [Acorn](roots.io/acorn) (Laravel in WordPress)
- [Sage](roots.io/sage) (WordPress Starter Theme w/ Tailwind CSS)
- [Clover](roots.io/clover) (WordPress Starter Plugin)

## Contributing
You can contribute to the project by doing the following:
1. Mac and Linux users, open Terminal, Windows users, open Bash in WSL**v2**.
2. Create a folder `teamsurtes.com`
3. Change directory into your new folder `teamsurtes.com` and clone both `https://github.com/Team-Surtes/trellis` and `https://github.com/Team-Surtes/site`
4. Then, change your directory to `teamsurtes.com/trellis` and `nano .vault_pass`.
   You'll need the Ansible vault password from another member of the team for Trellis to work.
   You can obtain the Ansible Vault password from the Team SURTES committee. (It will be in their handover document)
5. Next, you'll need to install [Homebrew](https://brew.sh) 
6. Then install the following formulae with `brew`:
   - `brew install ansible` (Installs Ansible)
   - `brew install roots/tap/trellis-cli` (Installs Trellis CLI)
   - **(Mac Users Only)** `brew install lima` (Installs Lima VM)
7. Change your terminal directory to `teamsurtes.com/site/web/app/themes` and clone `https://github.com/Team-Surtes/theme`
8. Change your terminal directory again to `teamsurtes.com/site/web/app/plugins` and clone `https://github.com/Team-Surtes/sponsors`.
10. You're now ready to start getting the VM ready.
   Go back to `teamsurtes.com` in your terminal and `cd trellis`.
   Now run `trellis vault decrypt development` and `trellis init`.
11. Enusre your 
12. Now, start your VM.
   - Mac Users use Lima: `trellis vm start`
   - Linux/WSL use Vagrant: `trellis up`
13. Finally, provision your VM with `trellis provision development`
14. You should now be able to navigate to [teamsurtes.test](teamsurtes.test) and access the VM. Check nginx is running on the VM by accessing the VM's shell and running `systemctl status nginx`.
