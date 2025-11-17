# magento2-upgrader
Simple bash script to upgrade magento and composer requirements


## Setup
- You must be in the Magento project root
- You must have `auth.json` configured
- You must have the correct version of PHP for the target Magento version installed


## Running
```bash
curl -sL https://raw.githubusercontent.com/zero1limited/magento2-upgrader/refs/heads/master/upgrade | /bin/bash -s -- --magento-version 2.4.8-p3
```
Replace `2.4.8-p3` with whatever version you're wanting to install

## Limitations
- Only `repositores`, `extra.patches` and `require` are persisted, if you have other modification you will need to copy them after the install.
  These can be seen with `diff -u composer.json.bak composer.json`
- No test of Magento functions