# Self Hosted

This is a repo for my self hosted applications. The plan is to use Docker for most applications and host on DigitalOcean.

### Planned Applications

- [x] [TracksApp](http://www.getontracks.org/)
- [ ] [OpenVPN](https://openvpn.net/)
- [ ] [Shout IRC](http://shout-irc.com/)
- [ ] [Huginn build agents](https://github.com/cantino/huginn)
- [ ] [ThinkUp](https://www.thinkup.com/)
- [ ] [SnowPlow Analytics](http://snowplowanalytics.com/)
- [ ] [Mumble](http://wiki.mumble.info/wiki/Main_Page)
- [ ] [Feed HQ Reader](https://feedhq.org/)
- [ ] 750words.com clone (work in progress)
- [ ] [MindMaps](https://github.com/drichard/mindmaps)
- [ ] [wger workout tracker](https://github.com/rolandgeider/wger)
- [ ] [Dillinger markdown](https://github.com/joemccann/dillinger/)
- [ ] [Reportr](https://github.com/Reportr/dashboard)
- [ ] [Gogs](https://github.com/gogits/gogs)
- [ ] [Jenkins CI](https://jenkins-ci.org/)
- [ ] [Kanboard](http://kanboard.net/)

## Installation

1. [Install Ansible](http://docs.ansible.com/ansible/intro_installation.html)
2. Install required Ansible plugins using `ansible-galaxy install -r requirements.yml`
3. Install [Vagrant](https://docs.vagrantup.com/v2/installation/) for local development
4. Run `vagrant up`

## Usage

To run agaist a remote host, configure another host in the `hosts` inventory file, add required
application variables to `vars/main.yml` and execute `ansible-playbook -i hosts playbook.yml`

## TODO

- [ ] Bootstrap database on initial provision
- [ ] Backup database snapshots to S3
- [ ] Use example `yml` files for secrets
- [ ] Makefile for common tasks

## License

The MIT License (MIT)

Copyright (c) 2015 Matt Fritz

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
