# PHPmux

PHP wrapper to load tmux panes.

## Install

Clone, `chmod +x phpmux`, add to path. Depends on PHP at `/usr/php`.

## Run

Example: `phpmux --argument_file "app_log_names.txt" --command "tail -f /var/log/%1/%2.log" --session whatever`

It will open new tmux session named after `--session` argument.

Then each line in argument_file opens a pane using `--command` argument as a template.

It will replace `%n` subtring with exploded/space-delimited line content at position n from `--argument_file`


