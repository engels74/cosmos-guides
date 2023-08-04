# 02c) Setting up CORS

### Setting up CORS

Setting up CORS is critical because it is required for the Panel to connect to the Wings. Alternatively, the Wings must be configured to allow connections from the Panel. That is what CORS is for!

There are two choices.

1. [Option 1](02ca-cors-option-1-secure.md): Enabling CORS to only allow connections from the Panel URL only. This is the most secure option, but it may not be compatible with all systems and network configurations.
2. [Option 2](02cb-cors-option-2-failsafe.md): Enabling CORS to allow connections from any URL. This is the "**failsafe**" option because it has a bigger chance of working on more systems and network configurations. However, it is not as safe as the first option.

Still, I would recommend [Option 1](02ca-cors-option-1-secure.md) because it is the most secure!

You should only choose option 2, if the Node doesn't show up as Online, [later in the guide](../../04-connecting-the-wings/04c-final-touches.md).

### On to the next step!
