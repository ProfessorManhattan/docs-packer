<div align="center">
  <h4>
    <a href="https://app.vagrantup.com/{{ variables.vagrantup_user }}">VagrantUp Profile</a>
    <span> | </span>
    <a href="https://app.vagrantup.com/{{ variables.vagrantup_user }}/boxes/{{ variables.box_basename }}">VagrantUp Box</a>
    <span> | </span>
    <a href="{{ repository.group.packer }}/{{ variables.box_basename }}/-/blob/master/CONTRIBUTING.md">Contributing</a>
    <span> | </span>
    <a href="{{ chat_url }}">Chat</a>
    <span> | </span>
    <a href="{{ website.homepage }}">Website</a>
  </h4>
</div>
<p style="text-align:center;">
  <a href="{{ repository.group.packer }}/{{ variables.box_basename }}">
    <img alt="Version" src="https://img.shields.io/badge/version-{{ variables.iso_version }}-blue.svg?cacheSeconds=2592000" />
  </a>
  <a href="{{ website.documentation }}/packer" target="_blank">
    <img alt="Documentation" src="https://img.shields.io/badge/documentation-yes-brightgreen.svg" />
  </a>
  <a href="{{ repository.group.packer }}/{{ variables.box_basename }}/-/raw/master/LICENSE" target="_blank">
    <img alt="License: {{ license }}" src="https://img.shields.io/badge/License-{{ license }}-yellow.svg" />
  </a>
  <a href="https://twitter.com/{{ profile.twitter }}" target="_blank">
    <img alt="Twitter: {{ profile.twitter }}" src="https://img.shields.io/twitter/follow/{{ profile.twitter }}.svg?style=social" />
  </a>
</p>
