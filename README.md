# webhookly


<div align="center">
  <a href="https://www.oracle.com/java/">
    <img
      src="https://img.shields.io/badge/Written%20in-java-%23EF4041?style=for-the-badge"
      height="30"
    />
  </a>
  <a href="https://jitpack.io/#micartey/webhookly/master-SNAPSHOT">
    <img
      src="https://img.shields.io/badge/jitpack-master-%2321f21?style=for-the-badge"
      height="30"
    />
  </a>
</div>

<div align="center">
    Fork of <a href="https://gist.github.com/k3kdude/fba6f6b37594eae3d6f9475330733bdb">k3kdude/DiscordWebhook</a>
</div>

## 📚 Introduction

webhookly is a Java dependency to send messages via discord webhooks.
The work has already been done by [k3kdude](https://github.com/k3kdude) and just been refactored.
The following example allows you to send a message to a channel.

```java
DiscordWebhook webhook = new DiscordWebhook(...);
        webhook.setAvatarUrl(...);
        webhook.setUsername("Some Title");

EmbedObject embed = new EmbedObject()
        .setTitle("A Title")
        .setColor(new Color(174, 63 ,65))
        .setDescription("Line 1 \\n Line 2")
        .setFooter(new Footer("A Footer", ""));

webhook.addEmbed(embed);
webhook.execute();
```