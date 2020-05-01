# Thunder VIP Mac without update

[English](#Thunder-VIP-Mac-without-update) | 中文(懒得写了)

This is a backup for Cracked Thunder 9.9.9 on Mac

and a solution for banning forced update

Enjoy high-speed download on your mac by following steps.

# Install

Download `Thunder.zip` of master

>  md5 of compressed file: `6652bee1b055860fa420ee363172dd60`

Drag `Thunder.app` from zip to Application folder

Run it **(check the all documentation before you RUN it)**

# Remove Update Push

Very annoying, it keeps popping up and cannot use it normally if you do not update.

So here’s solution

## 1. Edit Hosts

**This way doesn’t work for me, but I suggest you guys follow this step.** I have two version(one official release and this cracked) on my laptop, and actually there's no update pop-up when I first run it while it popped up in the second run and always popping even if reinstalling. Hence I presume the software generated some files on the Mac for checking update after the first run.

**So better set up this step and trying to run it as your first time.**

I searched for a solution, so at the very first. Add this line to your hosts file where stored at `/etc/hosts`

> You can use hosts editor [Helm](https://helm.sh/) for a better experience.

```
127.0.0.1 liveupdate.mac.sandai.net
```

![](https://user-images.githubusercontent.com/15688641/80823042-6f1fb080-8c0e-11ea-8899-91d6a0731216.png)

Where you can see, better don’t ban `sandai.net` in the hosts, it refers to downloading session.

## 2. Remove Live Update plugin

If it still pop up after the first step, here’s the final solution.

it’s in`/Users/zoengjinnbiu/Library/Application Support/Thunder/PlugIns/9.9.9.2844`

![](https://user-images.githubusercontent.com/15688641/80824115-6039fd80-8c10-11ea-8374-cfae61924238.png)

It could happened that your folder is different from mine, anyway, `9.9.9.2844` is the version mark, find something looks like `liveupdate.xlplugin` such as `liveupdate 12.09.44 AM.xlplugin`

Remove it and reopen Thunder, you won’t find the pop-up.

Noticed, another one `liveupdate.xlpigun` is in the package contents of Thunder, I deleted it at fitst time but nothing changed to Thunder. But I presume it’s ok to delete both.

![](https://user-images.githubusercontent.com/15688641/80824421-0423a900-8c11-11ea-9642-52da42dfec8d.png)