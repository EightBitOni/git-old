

Install VNC
```
sudo apt update
sudo reboot
sudo apt install x11vnc
```

create x11vnc service
```
sudo nano /lib/systemd/system/x11vnc.service
```

Copy and paste these in nano while configuring x11vnc.service - note: change the password - then reboot
```
[Unit]
Description=x11vnc service
After=display-manager.service network.target syslog.target

[Service]
Type=simple
ExecStart=/usr/bin/x11vnc -forever -display :0 -auth guess -passwd "password"
ExecStop=/usr/bin/killall x11vnc
Restart=on-failure

[Install]
WantedBy=multi-user.target
```

Save file and run these commands to start service:

```
systemctl daemon-reload
systemctl enable x11vnc.service
systemctl start x11vnc.service
systemctl status x11vnc.service
```

You can check on the status of this service, like others, using `systemctl status x11vnc.service`

other information
Website: [https://bit.ly/2IOJUd8](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbjFHVm5xWVAyWXl5V3pERlFSd0tvRndNUy1YUXxBQ3Jtc0tsdlJOdzBPUHFmZ1B2T3FLbmk3cXU4VlZ4MURKeHd1VHpOTmhGYko4aXBiQndkU25vX3d6VEc3U3hoeW5BVTItZ2tZTW1UcHlWR000WE5mNTR5SkpjV2FRbkRJZEhzMEpBVnk3UXFjbFptNTRxSF9Nbw&q=https%3A%2F%2Fbit.ly%2F2IOJUd8&v=3K1hUwxxYek)
youtube video: [David Bombal](https://www.youtube.com/watch?v=3K1hUwxxYek)

