# CPCDiskAdapter
A Universal Floppy Disk Drive Adapter for the Amstrad / Schneider CPC 464 

## Purpose 

A versatile floppy disk drive adapter board for the Amstrad /
Schneider CPC.  This printed circuit board (PCB) is primarily intended
for the CPC 464.

![Board Front](images/floppy-adapter-board-front.png)

![Board Back](images/floppy-adapter-board-back.png)

The Gerbers are [here.](gerbers.zip) 

Connecting disk drives other than the standard Amstrad DD1 / DF1
drives to the CPC via the DDI-1 disk controller usually requires some
floppy cable mods. Moreover, these mods usually fix the drive 
to either being CPC A or B drive.  

With this adapter board, one can flexibly use the DIP switches to
select 2 out of 3 possible disk drives, and flexibly determine which
one is A or B, and no more (destructive) cable mods are
required. Also, no twisted floppy cables.

The following drives can be used: 

- Amstrad DD1 / FD1 3" flopy
- 3.5" floppy 
- 5.25" floppy
- Gotek floppy drive

 If a certain drive does not emit the READY signal, then the READY
signal can be "faked" by grounding it via the corresponding READY DIP
switch (grounding the READY line is a standard CPC floppy cable hack). 

The pictures show an application example. I am using the Amstrad DDI-1 disk controller and an old 2bay SCSI enclosure. 

Check out the schematics. I1 and I2 are input sockets for the Amstrad DDI-1 connectors - note that **both connectors have to be used, in order to recover the A, B selection lines**. With a different controller only one socket may be needed. O1, O2, and O3 are outputs. Note that **5V is not supplied over the adapter.** 

Please [check the schematics.](schematics.pdf) 

## Using the Amstrad DDI-1 Disk Controller 

Please note that by default, the DDI-1 is **powered by the DD1 / DF1 3" floppy drive**. However, the adapter DOES NOT connect the 5V power lines in order to protect other drives (powering drives over the floppy ribbon cable was an Amstrad "non-standard" invention). Hence, in order to be able to use the DDI-1 with this adapter board, a **modification has to be applied** to the DDI-1 controller. After the modification, the DDI-1 will be powered by the CPC over the expansion bus. 

The modification is described [here.]([http://www.cpcwiki.eu/index.php/DDI_Modification]). I have put a switch in my DDI-1 that allows me to power it either via the CPC, or via the floppy cable from the drive.  

## Application Examples 

![Adapter 1](images/adapter1.JPG)

![Adapter 2](images/adapter2.JPG)

![Adapter 3](images/adapter3.JPG)

![Adapter 4](images/adapter4.JPG)

![Adapter 5](images/adapter5.JPG)






