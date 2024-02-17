# 03a) Creating the first user

### Creating the first admin user

1. To create the admin user, we need to run a command in our SSH terminal:

```bash
docker exec -it pt-panel php artisan p:user:make
```

2. This will start a user-creation session. This is needed to create the first user.
3. It'll ask if you want to create an administrator user, you should write `yes`
4. Enter the email you want associated with the account
5. Enter your name/username (whatever you want basically)
6. Enter your password.
7. You can now login to your panel!

{% hint style="warning" %}
**Warning:** Make sure you enter the right password the first time - it won't ask twice
{% endhint %}

[![asciicast](https://asciinema.org/a/GfSOVuYOhE24B6XTQkmbixSHT.svg)](https://asciinema.org/a/GfSOVuYOhE24B6XTQkmbixSHT)

### On to the next step!
