---
title: Module 02: Hints
body-class: index-page
---

## Module 02 - Hints

!!! note "Cloudwatch agent"

    If you run into problems with your cloudwatch agent configuration file, this may help.

    Here is the command to run the cloudwatch agent with the provided configuration file:

    ```
    sudo /opt/aws/amazon-cloudwatch-agent/bin/amazon-cloudwatch-agent-ctl -a fetch-config -m ec2 -s -c file:/opt/aws/amazon-cloudwatch-agent/bin/config.json
    ```

!!! note "Linux Commands"

    Knowledge of Linux Bash commands would be helpful but is not mandatory. Bash commands used in this lab include [cp](https://linux.die.net/man/1/cp), [mv](https://linux.die.net/man/1/mv), [cat](https://linux.die.net/man/1/cat), [sudo](https://linux.die.net/man/8/sudo), [yum](https://linux.die.net/man/8/yum), [wget](https://linux.die.net/man/1/wget), and [find](https://linux.die.net/man/1/find). You are encouraged to familiarize yourself with the purpose of each command if you don't already know them.

    Tip: For information about Linux Bash commands, see the Linux Man Pages on [linux.die.net](https://linux.die.net){:target="_blank"}. To learn about a specific command, enter it in the search box at the top of the page.

