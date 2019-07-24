```# Customize this file based on your bundler location, app directory, etc.
# Put this in /usr/lib/systemd/system (CentOS) or /lib/systemd/system (Ubuntu).
# Run:
#   - systemctl enable sidekiq
#   - systemctl {start,stop,restart} sidekiq
#
# This file corresponds to a single Sidekiq process.  Add multiple copies
# to run multiple processes (sidekiq-1, sidekiq-2, etc).
#
# See Inspeqtor's Systemd wiki page for more detail about Systemd:
# https://github.com/mperham/inspeqtor/wiki/Systemd
#
[Unit]
Description=sidekiq
After=syslog.target network.target

[Service]
Type=simple
WorkingDirectory=/usr/local/rails_apps/ipdw-internal/current
ExecStart=/home/vu.hai.ha/.rvm/wrappers/ruby-2.6.3/bundle exec sidekiq -e production
User=vu.hai.ha
Group=sudo
UMask=0002
Environment=RAILS_ENV=production
EnvironmentFile=/home/deploy/.env.backend
# if we crash, restart
RestartSec=1
#Restart=on-failure
Restart=always

# output goes to /var/log/syslog
StandardOutput=file:/var/log/sidekiq.log
StandardError=file:/var/log/sidekiq.log

# This will default to "bundler" if we don't specify it
SyslogIdentifier=sidekiq

[Install]
WantedBy=multi-user.target```
