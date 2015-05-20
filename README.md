# Ansible playbook for setup thumbor server

Tested on CentOS 6 and 7

## Install Softwares

* [thumbor](https://github.com/thumbor/thumbor ) (PIL, GraphicsMagick, OpenCV)
* [supervisor](http://supervisord.org/)
* [nginx}](http://nginx.org/)
* Python 2.7 (CentOS 6)

## Usage

```
ansible-playbook -i xxx.xxx.xxx.xxx, -u root -e engine=pil thumbor.yml
```

or

```
ansible-playbook -i xxx.xxx.xxx.xxx, -s -e engine=pil thumbor.yml
```

Choose the `engine` from `pil`, `pgmagick` and `opencv`.

## Limitations

opencv supported on CentOS 7 only. Because CentOS 7 has opencv package.

pgmagick require at least 1 GB RAM. (I do not know know why , but it requires a lot of memory to compile pgmagick)
