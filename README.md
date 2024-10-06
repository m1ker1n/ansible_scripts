ansible all -m ping -i inventory

# encrypt password for linux hosts
ansible all -i localhost, -m debug -a "msg={{ 'changeme' | password_hash('sha512') }}"

# screen copy to clipboard
apt install xsel (to copy to clip)

`cat | xsel -b`, `ctrl+a+[`, cursor on the first end of text, `space`, cursor on the second end of text, `space`, `ctrl+a+]`, `ctrl+d`

# missing sudo password ansible
ansible-playbook mail.yml -kK
-k, --ask-pass: ask for connection password
-K, --ask-become-pass: ask for privilege escalation password