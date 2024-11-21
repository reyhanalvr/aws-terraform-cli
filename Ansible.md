## Setup Konfigurasi dengan Ansible

### Buat Inventory dan ansible.cfg

Inventory sendiri berfungsi untuk menampung Host

Ansible cfg untuk konfigurasi awal dari ansible kita

![image](https://github.com/user-attachments/assets/c9b684ce-8f7e-472c-8112-916da3aab587)
![image](https://github.com/user-attachments/assets/3ba9385b-a5f8-4b88-8bff-1e3ef4cde011)



### Ansible Playbook untuk Instalasi Docker

```yaml
---
# tasks file for roles/docker

- name: Update apt cache
  apt:
    update_cache: yes

- name: Install required packages for Ubuntu
  apt:
    name:
      - apt-transport-https
      - ca-certificates
      - curl
      - software-properties-common
    state: present


- name: Add Docker GPG key
  apt_key:
    url: "https://download.docker.com/linux/{{ ansible_distribution | lower }}/gpg"
    state: present

- name: Add Docker repository
  apt_repository:
    repo: "deb [arch=amd64] https://download.docker.com/linux/{{ ansible_distribution | lower }} {{ ansible_distribution_release }} stable"
    state: present

- name: Install Docker and related packages
  apt:
    name:
      - docker-ce
      - docker-ce-cli
      - containerd.io
      - docker-buildx-plugin
      - docker-compose-plugin
    state: present

- name: Start Docker service
  service:
    name: docker
    state: started
    enabled: yes

- name: Add user to docker group
  user:
    name: "{{ user_name }}"
    groups: docker
    append: yes
  notify: Restart Docker

```

### Docker telah terinstall
![image](https://github.com/user-attachments/assets/ddfe51bd-53a7-4b3e-8c27-26e02540e758)
