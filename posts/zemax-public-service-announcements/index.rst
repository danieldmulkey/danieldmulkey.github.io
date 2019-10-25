.. title: Zemax Public Service Announcements
.. slug: zemax-public-service-announcements
.. date: 2019-10-25 02:58:10 UTC-07:00
.. tags: 
.. category: 
.. link: 
.. description: 
.. type: text

* Zemax Programming Language (ZPL) macros ignore case. D is the same as d.
* If you run a ZPL macro from the Programming tab that changes the system, your lens file will be updated. If you run the same macro as a ZPLM operand, your system will *not* be updated.
* Uncertain about a new Physical Optics Propagation (POP) calculation? Use a universal plot to check some parameters vs. distance and make sure it passes some sanity checks.
* You never know what well-hidden setting on some surface accidentally got changed by the scroll wheel on your mouse when the cursor just happened to be in the wrong place. If in doubt, rebuild your design with a new file just to check.
* If your system only has one wavelength and you try to plot index vs wavelength on a material, your plot won't show anything. Add a second wavelength and then it should work.
* Using polarization in POP mostly just accounts for coatings (or lack thereof). If you have any sets of Birefringent In / Out surfaces, it'll convert to rays to propagate through them. Maybe that works for your application, but not for mine.
* POP is centered on the chief ray of whatever field you pick, so if you don't see the beam position moving even though your chief ray changes height, that's why.
* This bug might be fixed now, but if you import a lens, haven't saved recently, and try to change the color of multiple surfaces in the Lens Data Editor (LDE), watch out for weird things like the stop surface or a surface type changing.
* If your MechE can't see rays from a .step file, when they import the file they have to change their settings in SolidWorks to include importing 3D drawings.
* If you do a Universal Plot of coupling efficiency vs distance and see a weird jump where it should be smooth, update your copy of Zemax.
* You can use tilted surfaces to mimic light from an APC ferrule. This is also a great way to learn to use PC ferrules any time you're fiber coupling. Otherwise, your coupling efficiency depends on ferrule axial rotation angle.
* Need to multithread a POP ZPL macro but have to write to a file? There's a function you can use to get a random number. Cast that to a string and drop that onto the end of your filename, and now you can (fairly safely) ensure each instance of your macro won't try to write to the same file. This fails rarely, but it does happen.

