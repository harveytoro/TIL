# Force kill running service

- First need to find PID `> sc queryex <service name>`

- Then to force kill with taskkill running in administrator mode `taskkill /F /pid <service pid>`
