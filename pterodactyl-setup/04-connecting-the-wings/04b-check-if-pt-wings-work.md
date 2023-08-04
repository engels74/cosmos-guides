# 04b) Check if pt-wings work

In this section, we'll verify that our config.yml works as expected. Then we'll connect our 'pt-wings' container to the 'pterodactyl\_nw' network we created in our config file.

### Restarting the `pt-wings`

1. Finally, we can restart our pt-wings container:

![](https://i.imgur.com/7rkDKBN.png)

1. We should now examine the container's logs. To do so, navigate to the Logs menu in the pt-wings container's Details.
2. Something along the lines of this should be there:

```log
2023-07-26 19:28:52
  INFO: [Jul 26 21:28:52.731] loading configuration from file config_file=/etc/pterodactyl/config.yml
2023-07-26 19:28:52
  INFO: [Jul 26 21:28:52.732] configured wings with system timezone timezone=Europe/Berlin
2023-07-26 19:28:52
  INFO: [Jul 26 21:28:52.733] configured system user successfully gid=988 uid=988 username=pterodactyl
2023-07-26 19:28:52
  INFO: [Jul 26 21:28:52.737] fetching list of servers from API
2023-07-26 19:28:53
  INFO: [Jul 26 21:28:53.051] processing servers returned by the API total_configs=0
2023-07-26 19:28:53
  INFO: [Jul 26 21:28:53.051] finished processing server configurations duration=467.113µs
2023-07-26 19:28:53
  INFO: [Jul 26 21:28:53.056] configuring system crons  interval=1m0s subsystem=cron
2023-07-26 19:28:53
  INFO: [Jul 26 21:28:53.057] starting cron processes   subsystem=cron
2023-07-26 19:28:53
  INFO: [Jul 26 21:28:53.058] configuring internal webserver host_address=0.0.0.0 host_port=443 use_auto_tls=false use_ssl=false
2023-07-26 19:28:53
  INFO: [Jul 26 21:28:53.059] updating server states on Panel: marking installing/restoring servers as normal
2023-07-26 19:28:53
  INFO: [Jul 26 21:28:53.062] sftp server listening for connections listen=0.0.0.0:2022 public_key=ssh-ed25519 AAAAC3NzaC1lZDIXNTE5AABAIGagsxnhw/CplLwwJVe/WhpiC4zybb66ZXI7Okjvmxdg
```

3. Go to the **Network** tab of the `pt-wings`: <img src="https://i.imgur.com/t8T5r9G.png" alt="" data-size="line">
4. Find the `pterodactyl_nw` network and select **Connect**.

<figure><img src="https://i.imgur.com/ryvgm0Q.gif" alt=""><figcaption></figcaption></figure>

### Check if the reverse proxy work

1. To see if the `pt-wings` reverse proxying is working as intended, load up your `https://pterodactylnode.domain.com` site up in a new tab in your browser.
2. In my case, that would be `https://pterodactylnode.engels.zip`.
3. It should give you this message:

<pre class="language-json"><code class="lang-json"><strong>"The required authorization heads were not present in the request."
</strong></code></pre>

4. Oddly enough, this means that it's working as intended.

### On to the next step!
