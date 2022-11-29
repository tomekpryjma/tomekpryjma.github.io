---
layout: default
title: Quake Modding
---

# Write the first mod
<ul>
    <li>Download the FTEQW [engine](https://www.fteqw.org/)</li>
    <li>Download the FTEQCC [compiler](https://www.fteqcc.org/)</li>
    <li>Download the Quake [source code](https://github.com/id-Software/quake-rerelease-qc)
        <ul>
            <li>Extract this somewhere, for example <strong>C:/quake-source</strong></li>
        </ul>
    </li>
    <li>Find your copy of Quake. For example, if you installed it via Steam, it will be in <strong>steamapps/common/Quake</strong>
        <ul>
            <li>Place the FTEQW engine you downloaded earlier in this directory.</li>
            <li>In the main Quake directory, create a folder and name it whatever you want, let's use <strong>mymod</strong> as an example.</li>
            <li>In the mod folder create a <strong>src</strong> directory. Feel free to call it whatever you want.</li>
            <li>Copy the contents of <strong>C:/quake-source/quakec</strong> into <strong>mymod/src</strong></li>
        </ul>
    </li>   
    <li>Open your favourite code editor in <strong>mymod/src</strong>
        <ul>
            <li>Go into the <strong><code>weapons.qc</code></strong> file and find the functional called <strong><code>W_FireRocket</code></strong></li>
            <li>Change the line that says <strong><code>missile.velocity = missile.velocity * 1000;</code></strong> to <strong><code>missile.velocity = missile.velocity * 50;</code></strong></li>
            <li>Save the file.</li>
        </ul>
    </li>
    <li>Launch the FTEQCC compiler you downloaded earlier, it will ask for a file. You will need to give it the <strong>progs.src</strong> file in <strong>mymod/src</strong>.</li> 
    <li>Hit <strong>F7</strong> to compile. If the left hand side turns yellow, it should be OK.</li>
    <li>Hit <strong>F5</strong> to play.
        <ul>
        <li>The compiler will ask you for a quake executable to launch. Locate <strong>fteglqw64.exe</strong> inside your Quake directory. (Since we are using the FTEQCC compiler, we need to launch the FTE executable.)</li>
        </ul>
    </li>
    <li>Click <strong>New Game</strong>. If you are met with red errors and the game not loading, please refer to the issues list at the bottom of this page.</li>
    <li>Once you are in the level, hit the backtick key (usually below the Esc key).
        <ul>
            <li>
                Type in <strong>give 7</strong> (this gives you the rocket launcher)
            </li>
            <li>
                Type in <strong>give r 99</strong> (this gives you 99 rockets)
            </li>
        </ul>
    </li>
    <li>Switch to the rocket launcher and watch your rockets fly at a snail's pace!</li>
</ul>

# Issues I ran into

## ex_bprint and other undefined things
I ran into the issue where, even though everything was compiling fine, when I launched the game and tried to play I got errors such as these:
```
SV_ERROR:
BUILTIN 0: EX_BPRINT NOT IMPLEMENTED
MOD IS NOT COMPATIBLE.
HOST_ENDGAME:
BUILTIN 0: EX_BPRINT NOT IMPLEMENTED
MOD IS NOT COMPATIBLE.
```
To fix this, I downloaded the [latest FTEQW engine](https://www.fteqw.org/)
<p>