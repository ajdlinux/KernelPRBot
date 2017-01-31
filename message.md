Hi @{{ username }}!

Thanks for your contribution to the Linux kernel!

Linux kernel development happens on mailing lists, rather than on GitHub - this GitHub repository is a read-only mirror that isn't used for accepting contributions. So that your change can become part of Linux, please email it to us as a patch.

Sending patches isn't quite as simple as sending a pull request, but fortunately it is a well documented process.

Here's what to do:

* Format your contribution according to kernel requirements
* Decide who to send your contribution to
* Set up your system to send your contribution as an email
* Send your contribution and wait for feedback

How do I format my contribution?
--------------------------------

The Linux kernel community is notoriously picky about how contributions are formatted and sent. Fortunately, they have documented their expectations.

Firstly, all contributions need to be formatted as patches. A patch is a plain text document showing the change you want to make to the code, and documenting why it is a good idea.

You can create patches with [`git format-patch`](https://git-scm.com/docs/git-format-patch).

Secondly, patches need 'commit messages', which is the human-friendly documentation explaining what the change is and why it's necessary.

Thirdly, changes have some technical requirements. There is a Linux kernel coding style, and there are licensing requirements you need to comply with.

Both of these are documented in the [Submitting Patches documentation](https://kernel.org/doc/html/latest/process/submitting-patches.html) that is part of the kernel.

Note that you will almost certainly have to modify your existing git commits to satisfy these requirements. Don't worry: there are many guides on the internet for doing this.

Who do I send my contribution to?
---------------------------------

The Linux kernel is composed of a number of subsystems. These subsystems are maintained by different people, and have different mailing lists where they discuss proposed changes.

If you don't already know what subsystem your change belongs to, the [`get_maintainer.pl`](https://github.com/torvalds/linux/blob/master/scripts/get_maintainer.pl) script in the kernel source can help you.

`get_maintainer.pl` will take the patch or patches you created in the previous step, and tell you who is responsible for them, and what mailing lists are used. You can also take a look at the [MAINTAINERS](https://www.kernel.org/doc/linux/MAINTAINERS) file by hand.

Make sure that your list of recipients includes a mailing list. If you can't find a more specific mailing list, then [LKML - the Linux Kernel Mailing List](http://vger.kernel.org/vger-lists.html#linux-kernel) - is the place to send your patches.

It's not usually necessary to subscribe to the mailing list before you send the patches, but if you're interested in kernel development, subscribing to a subsystem mailing list is a good idea. (At this point, you probably don't need to subscribe to LKML - it is a very high traffic list with about a thousand messages per day, which is often not useful for beginners.)

How do I send my contribution?
------------------------------

Use [`git send-email`](https://git-scm.com/docs/git-send-email), which will ensure that your patches are formatted in the standard manner. In order to use `git send-email`, you'll need to configure git to use your SMTP email server.

For more information about using `git send-email`, look at the [Git documentation](https://git-scm.com/docs/git-send-email) or type `git help send-email`. There are a number of useful guides and tutorials about `git send-email` that can be found on the internet.

How do I get help if I'm stuck?
-------------------------------

Firstly, don't get discouraged! There are an enormous number of resources on the internet, and many kernel developers who would like to see you succeed.

Many issues - especially about how to use certain tools - can be resolved by using your favourite internet search engine.

If you can't find an answer, there are a few places you can turn:

* [Kernel Newbies](https://kernelnewbies.org) - this website contains a lot of useful resources for new kernel developers.
* If you'd like a step-by-step, challenge-based introduction to kernel development, the [Eudyptula Challenge](http://eudyptula-challenge.org/) would be an excellent start.
* [The kernel documentation](https://www.kernel.org/doc/html/latest/) - see also the `Documentation` directory in the kernel tree.

If you get really, really stuck, you could try the owners of this bot, @daxtens and @ajdlinux. Please be aware that we do have full-time jobs, so we are almost certainly the slowest way to get answers!

I sent my patch - now what?
---------------------------

You wait.

You can check that your email has been received by checking the mailing list archives for the mailing list you sent your patch to. Messages may not be received instantly, so be patient. Kernel developers are generally very busy people, so it may take a few weeks before your patch is looked at.

Then, you keep waiting. Three things may happen:

* You might get a response to your email. Often these will be comments, which may require you to make changes to your patch, or explain why your way is the best way. You should respond to these comments, and you may need to submit another revision of your patch to address the issues raised.
* Your patch might be merged into the subsystem tree. Code that becomes part of Linux isn't merged into the main repository straight away - it first goes into the subsystem tree, which is managed by the subsystem maintainer. It is then batched up with a number of other changes sent to Linus for inclusion. (This process is described in some detail in [the kernel development process guide](https://www.kernel.org/doc/html/latest/process/development-process.html)).
* Your patch might be ignored completely. This happens sometimes - don't take it personally. Here's what to do:
	* Wait a bit more - patches often take several weeks to get a response; more if they were sent at a busy time.
	* Kernel developers often silently ignore patches that break the rules. Check for obvious violations of the the Submitting Patches guidelines, the style guidelines, and any other documentation you can find about your subsystem. Check that you're sending your patch to the right place.
	* Try again later. When you resend it, don't add angry commentary, as that will get your patch ignored. It might also get you silently blacklisted.

Further information
-------------------

* [Working with the kernel development community](https://www.kernel.org/doc/html/latest/process/index.html) - the official documentation for new kernel contributors

Happy hacking!

*This message was posted by a bot - if you have any questions or suggestions, please talk to my owners, @ajdlinux and @daxtens, or raise an issue at https://github.com/ajdlinux/KernelPRBot.*
