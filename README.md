# Valet Service Ticket

## Introduction

In january 2015 I went to the Philippines for a wedding and to give a hand to the organisation.

The manager assigned me to make the valet service tickets. Actually everything was done and by everything I mean the PSD file quickly made and good enough to print hundreds of tickets. The small detail that changed everything was that every ticket has a unique number. The PSD could accept only 4 numbers and I had to print 200 of them.

A simple process could have been to manually change the numbers and save a JPG version of each. But, 200... It represents 50 iterations and I'm too lazy for that.

After a quick research on Google I've learned some basics on creating a JavaScript script to manipulate PSDs. Thanks Adobe for this feature which made us to save time. We don't even know if it's old or not but it's useful! Just the time to go through their doc and read a blog post. A short loop and it was done!

Later, we agreed to share that experience here.

## Install and use

The script is setted to manipulate the PSD file currently opened.

1. Open the PSD file `valet_service_tickets.psd`
2. Open the script `tickets_counter_script.jsx` with ExtendScript Toolkit (Installed with Photoshop)
3. Click `No` to the question : __Do you want to launch the script?__
4. `Line 163` you'll find the variable `nbPages`. Since every page has 4 tickets, set it to 50 to generate 200 tickets. (200 / 4 = 50)
5. Click the green Play button on the top right corner to launch the loop.

Your JPGs will be saved in the same folder.



## Requirement

Since layers are called by the script, they need to keep their names and to be at the root. It is 100% sure that we can browse folders to find layers by name but I did it as fast as possible.


## Credits

Don Ruiz (Wedding planner / Graphic designer) : Graphic design

[Nicolas Bages](http://weinto.com) (UX designer) : Photoshop script

[simonmeggle / sahi2omd](https://github.com/simonmeggle/sahi2omd/blob/master/userdata/include/sprintf.inc) : sprintf function