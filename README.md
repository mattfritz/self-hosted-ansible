# Self Hosted

This is a repo for my self hosted applications. The plan is to use Docker for most applications and host on DigitalOcean.

## Installation

1. [Install Ansible](http://docs.ansible.com/ansible/intro_installation.html)
2. Install required Ansible plugins using `ansible-galaxy install -r requirements.yml`
3. Install [Vagrant](https://docs.vagrantup.com/v2/installation/) for local development
4. Run `vagrant up`

## Usage

To run agaist a remote host, configure another host in the `hosts` inventory file and execute `ansible-playbook -i hosts playbook.yml`

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
