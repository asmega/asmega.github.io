---
layout: post
title: "How-to: Deploy Ruby on Rails in a subdirectory and not in root"
date: 2009-02-27
---

Normally one would deploy their rails application in the root directory (top-level) ie where the domain is, for example…

```
www.example.com
```

However, you may want to deploy your app in a subdirectory such as…

```
www.example.com/your_app
```

You may want to do this if you want to deploy several applications on the same domain or temporarily for testing purposes. So heres what to do. Naviagate to the environment.rb file found here…

```
root | configuration | environment.rb
```

Open the file in your favourite text editor. Add the relative url configuration to your config as shown below. I added it to the end of the do statement.

```
Rails::Initializer.run do |config|
  config.action_controller.relative_url_root = "/your_app"
end
```

This setups the environment for rails to now run with url root of your_app.

Happy deploying!
