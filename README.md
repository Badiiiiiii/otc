# 🔮 OTC Loader  / ![Windows](https://github.com/0x000cb/otc/workflows/Windows/badge.svg?branch=master&event=push) /

----------------------------------------------------

Hello. This loader loads and initializes onetap crack in the CS:GO game.

-----------------------------------------------------

# FAQ
  * How clone this repository?
     * ``` git clone https://github.com/0x000cb/otc.git  && cd otc && git submodule update --init --recursive ```

  * Everything worked out, but when i inject onetap, menu it does not render.
     * Enable multi-threaded rendering (in csgo) and then inject OTC. 
     * If everything still does not work before, add a flag to disable d3x9 in the CS: GO startup parameters.
  
  * When you already fix what I need so much ??? I can’t play without it !!! (There should be a function name without which you cannot play)
     * First of all, we try to solve the most important problems. 
     * In TODO, you can see the order in which work is currently being performed.

  * The game crashes when I try inject OTC.
     * Make sure you have the latest version of OTC. 
     * If you inject an addon then try without it, very often it causes crashes.
     * Injector problems are also possible. (Try use process hacker)
     > p.s Injection through crashhandler spoofing can also cause crashes.

  * I found this repository, but can't find OneTap source code.
    * Right. This is just a loader, that initializes & patch & invoke a binary file in game memory. 
    * You can watch/patch file [**here**](https://github.com/0x000cb/otc/blob/master/OTC/cpp/segment/Segment.cpp).

  * How update signatures, index's, and netvars?

    * Signatures.
       * Vector: [m_signatures](https://github.com/0x000cb/otc/blob/master/OTC/headers/frameworks/SegmentFramework.h#L78) 
       * FAQ: [#12](https://github.com/0x000cb/otc/issues/12) 

    * Index's
       * Function: [CustomVirtualCaller](https://github.com/0x000cb/otc/blob/master/OTC/cpp/frameworks/SegmentFramework.cpp#L86)
       * You just need to go to unknowncheats, find out which index the rest have shifted from, and how much, and set this as a rule in the method.
       * Example:
           I know that indexes since 190 have shifted by 2.
           So I need to do like this: index> 189 index + = 2;
           This will quickly and easily fix indexes.

     * Netvars:
        * Vector: [m_netvars](https://github.com/0x000cb/otc/blob/master/OTC/headers/frameworks/SegmentFramework.h#L72)
        * Just change the second argument in the structure to the current value. It's all. (Recommend use: hazedumper)
-----------------------------------------------------

 # TODO (Issues)

  - [ ] Random crash caused triggerbot/backtrack. ([#1](https://github.com/0x000cb/otc/issues/1), [#20](https://github.com/0x000cb/otc/issues/20))
  - [ ] Buy-Bot. ([#3](https://github.com/0x000cb/otc/issues/3), [#8](https://github.com/0x000cb/otc/issues/8))
  - [ ] Binds. (Key-non-trigger)
  - [ ] Animations. (Chams) ([#8](https://github.com/0x000cb/otc/issues/8))
  
-----------------------------------------------------

# Last build

   * [**Download**](https://github.com/0x000cb/otc/releases/tag/master)
     * [Build](https://github.com/0x000cb/otc/releases/download/master/OTC.zip)
     * [Output](https://github.com/0x000cb/otc/releases/download/master/Output.zip)
     
------------------------------------------------------

# Configs
  > [Big collection #1 (827 configs)](https://yadi.sk/d/KZNcRdMSheLTfw)

------------------------------------------------------

# Credits

  * [0x000cb](https://github.com/0x000cb) - it's me! (Project creator & reverse staff)
  * [HoShiMin](https://github.com/HoShiMin) - Legacy & Native help. (Easy hook with HookLib :d)
  * [playday3008](https://github.com/playday3008) - Help with github & frequent pull requests.

  ------

  *  ♥ Community - Thank you for helping to develop and improve the project.
  *  ♥ toast, wnz, d3x - Thank you for starting all this. (p.s Original onetap crack authors)

  ------

  *  🛡️ flyingllama - Thank you for skeet level security.
