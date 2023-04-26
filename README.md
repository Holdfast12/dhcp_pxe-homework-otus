Взято за исходное состояние то, где папка iso располагается в папке проекта и CentOS-8.4.2105-x86_64-dvd1.iso для виртуальных машин уже находится в распакованном виде по пути /vagrant/iso/

смонтировать iso
mount -t iso9660 /home/michael/dhcp_pxe-homework-otus/CentOS-8.4.2105-x86_64-dvd1.iso /mnt -o loop,ro

  server.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible/playbook.yml"
  end