---
description: Zen Studios
---

# Pinball FX

<div align="left"><figure><img src="../../../.gitbook/assets/image (706).png" alt="" width="375"><figcaption></figcaption></figure></div>

## Overview

**Pinball FX** is the pinball platform from **Zen Studios** released in 2023 (Early Access on the Epic Games Store in 2022), successor of Pinball FX3. The game is free; tables are bought one by one or in collections. Wild West Rampage, Fish Tales and Sorcerer's Lair are free.

RetroBat starts a table directly, in the chosen game mode.

{% embed url="https://zenstudios.com/games/pinball-fx/" %}

## At a glance

<table><thead><tr><th width="216.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\pinballfx</code></td></tr><tr><td><strong>Extensions</strong></td><td>.table</td></tr><tr><td><strong>Default emulator</strong></td><td>pinballfx (steam version)</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller setup</strong></td><td>By the game (not changed by RetroBat)</td></tr><tr><td><strong>Save states</strong></td><td>No</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr></tbody></table>

## Which emulator to choose?

The `pinballfx` emulator has two versions (core):

<table><thead><tr><th width="158.25">Version</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>steam</strong> (default)</td><td>The game installed with Steam is started by Steam, directly on the chosen table.</td><td>Steam must be installed, with the game.</td></tr><tr><td><strong>nonsteam</strong></td><td>Starts the game executable directly, without Steam.</td><td>The game must be in <code>emulators\pinballfx</code>.</td></tr></tbody></table>

With **nonsteam**, RetroBat looks for `PinballFX.exe` in the `emulators\pinballfx` folder. If the game is not there, a message gives the expected folder.

## BIOS

No BIOS needed.

## Add tables

Each table is a small `.table` text file that contains the **table number**:

1. In `roms\pinballfx`, create a text file, for example `Wild West.txt`.
2. Write the table number on the first line (75 for Wild West Rampage).
3. Save, then change the `.txt` extension to `.table`.

<div align="left"><figure><img src="../../../.gitbook/assets/image (708).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
Only the tables you own start from RetroBat (in addition to the free tables).
{% endhint %}

<details>

<summary>Table numbers</summary>

<table><thead><tr><th width="208.25">No.</th><th>Table</th></tr></thead><tbody><tr><td>1</td><td>Civil War</td></tr><tr><td>2</td><td>Star Wars™ Pinball: Masters of the Force</td></tr><tr><td>4</td><td>South Park™: Super Sweet Pinball</td></tr><tr><td>5</td><td>Fear Itself</td></tr><tr><td>6</td><td>Star Wars™ Pinball: Starfighter Assault</td></tr><tr><td>7</td><td>Thor</td></tr><tr><td>10</td><td>Star Wars™ Pinball: Han Solo</td></tr><tr><td>12</td><td>Star Wars™ Pinball: Episode IV A New Hope</td></tr><tr><td>17</td><td>Marvel's The Avengers</td></tr><tr><td>20</td><td>Excalibur</td></tr><tr><td>21</td><td>Ghost Rider</td></tr><tr><td>22</td><td>Deadpool</td></tr><tr><td>23</td><td>Pasha</td></tr><tr><td>24</td><td>Star Wars™ Pinball: Episode VI Return of the Jedi</td></tr><tr><td>27</td><td>Biolab</td></tr><tr><td>28</td><td>Star Wars™ Pinball: Darth Vader</td></tr><tr><td>29</td><td>Adventure Land</td></tr><tr><td>30</td><td>Doctor Strange</td></tr><tr><td>31</td><td>Rome</td></tr><tr><td>33</td><td>Sorcerer's Lair</td></tr><tr><td>36</td><td>Super League Football</td></tr><tr><td>38</td><td>Fantastic Four</td></tr><tr><td>40</td><td>CastleStorm</td></tr><tr><td>43</td><td>Star Wars™ Pinball: Episode V The Empire Strikes Back</td></tr><tr><td>45</td><td>Blade</td></tr><tr><td>46</td><td>Spider-Man</td></tr><tr><td>47</td><td>Star Wars™ Pinball: The Clone Wars</td></tr><tr><td>48</td><td>Captain America</td></tr><tr><td>49</td><td>Moon Knight</td></tr><tr><td>50</td><td>Marvel's Guardians of the Galaxy</td></tr><tr><td>53</td><td>Star Wars™ Pinball: Boba Fett</td></tr><tr><td>55</td><td>South Park™: Butters' Very Own Pinball Game</td></tr><tr><td>56</td><td>World War Hulk</td></tr><tr><td>58</td><td>Star Wars™ Pinball: Droids™</td></tr><tr><td>59</td><td>X-Men</td></tr><tr><td>60</td><td>The Infinity Gauntlet</td></tr><tr><td>65</td><td>Iron Man</td></tr><tr><td>66</td><td>Secrets of the Deep</td></tr><tr><td>67</td><td>Epic Quest</td></tr><tr><td>71</td><td>Wolverine</td></tr><tr><td>73</td><td>Venom</td></tr><tr><td>75</td><td>Wild West Rampage</td></tr><tr><td>77</td><td>Star Wars™ Pinball: Star Wars Rebels™</td></tr><tr><td>78</td><td>Marvel's Avengers: Age of Ultron</td></tr><tr><td>79</td><td>Marvel's Ant-Man</td></tr><tr><td>80</td><td>Son of Zeus</td></tr><tr><td>88</td><td>Star Wars™ Pinball: The Force Awakens™</td></tr><tr><td>89</td><td>Star Wars™ Pinball: Might of the First Order</td></tr><tr><td>90</td><td>Fallout™ Pinball</td></tr><tr><td>91</td><td>The Elder Scrolls V: Skyrim™ Pinball</td></tr><tr><td>92</td><td>DOOM™ Pinball</td></tr><tr><td>93</td><td>Marvel's Women of Power: A-Force</td></tr><tr><td>94</td><td>Marvel's Women of Power: Champions</td></tr><tr><td>95</td><td>Jaws™ Pinball</td></tr><tr><td>96</td><td>E.T.™ Pinball</td></tr><tr><td>97</td><td>Back to the Future™ Pinball</td></tr><tr><td>98</td><td>Star Wars™ Pinball: Rogue One™</td></tr><tr><td>100</td><td>Jurassic Park™ Pinball</td></tr><tr><td>101</td><td>Jurassic World™ Pinball</td></tr><tr><td>102</td><td>Jurassic Park Pinball Mayhem™</td></tr><tr><td>103</td><td>Star Wars™ Pinball: The Last Jedi™</td></tr><tr><td>104</td><td>Star Wars™ Pinball: Ahch-To Island</td></tr><tr><td>105</td><td>Star Wars™ Pinball: Solo</td></tr><tr><td>106</td><td>Star Wars™ Pinball: Calrissian Chronicles</td></tr><tr><td>107</td><td>Star Wars™ Pinball: Battle of Mimban</td></tr><tr><td>108</td><td>Fish Tales</td></tr><tr><td>109</td><td>Williams™ Medieval Madness™</td></tr><tr><td>110</td><td>Williams™ JunkYard™</td></tr><tr><td>111</td><td>Williams™ The Getaway: High Speed II™</td></tr><tr><td>112</td><td>Curse of the Mummy</td></tr><tr><td>113</td><td>Sky Pirates: Treasures of the Clouds</td></tr><tr><td>117</td><td>Williams™ Theatre of Magic™</td></tr><tr><td>118</td><td>Williams™ Black Rose™</td></tr><tr><td>119</td><td>Williams™ Attack from Mars™</td></tr><tr><td>120</td><td>Williams™ The Party Zone™</td></tr><tr><td>121</td><td>Williams™ The Champion Pub™</td></tr><tr><td>122</td><td>Williams™ Safe Cracker™</td></tr><tr><td>123</td><td>Pinball Noir</td></tr><tr><td>124</td><td>Williams™ White Water™</td></tr><tr><td>125</td><td>Williams™ Red and Ted's Road Show™</td></tr><tr><td>126</td><td>Williams™ Hurricane™</td></tr><tr><td>127</td><td>Williams™ Cirqus Voltaire™</td></tr><tr><td>128</td><td>Williams™ No Good Gofers™</td></tr><tr><td>129</td><td>Williams™ Space Station™</td></tr><tr><td>130</td><td>Williams™ Monster Bash™</td></tr><tr><td>131</td><td>Williams™ Creature from the Black Lagoon™</td></tr><tr><td>132</td><td>Williams™ Tales of the Arabian Nights™</td></tr><tr><td>133</td><td>Williams™ Indiana Jones™: The Pinball Adventure</td></tr><tr><td>134</td><td>Williams™ FunHouse™</td></tr><tr><td>135</td><td>Williams™ Dr. Dude and his Excellent Ray™</td></tr><tr><td>136</td><td>Star Wars™ Pinball: The Mandalorian</td></tr><tr><td>137</td><td>Star Wars™ Pinball: Classic Collectibles</td></tr><tr><td>138</td><td>Hasbro's MY LITTLE PONY</td></tr><tr><td>139</td><td>DreamWorks Kung Fu Panda Pinball</td></tr><tr><td>140</td><td>DreamWorks Trolls Pinball</td></tr><tr><td>141</td><td>DreamWorks How to Train Your Dragon Pinball</td></tr><tr><td>145</td><td>Garfield Pinball</td></tr><tr><td>146</td><td>Peanuts' Snoopy Pinball</td></tr><tr><td>147</td><td>Wrath of the Elder Gods</td></tr><tr><td>148</td><td>Williams™ The Machine™: Bride of Pin·Bot™</td></tr><tr><td>149</td><td>Williams™ Swords of Fury™</td></tr><tr><td>150</td><td>Homeworld®: Journey to Hiigara Pinball</td></tr><tr><td>151</td><td>Brothers in Arms®: Win the War Pinball</td></tr><tr><td>152</td><td>Borderlands®: Vault Hunter Pinball</td></tr><tr><td>153</td><td>Kong Pinball</td></tr><tr><td>154</td><td>World War Z Pinball</td></tr><tr><td>155</td><td>Grimm Tales</td></tr><tr><td>156</td><td>Williams™ The Addams Family</td></tr><tr><td>157</td><td>Williams™ World Cup Soccer</td></tr><tr><td>158</td><td>Godzilla Pinball</td></tr><tr><td>160</td><td>Godzilla vs Kong Pinball</td></tr><tr><td>161</td><td>Crypt of the NecroDancer Pinball</td></tr><tr><td>162</td><td>Williams™ Twilight Zone</td></tr><tr><td>163</td><td>Williams™ Pinball: Star Trek™: The Next Generation</td></tr><tr><td>164</td><td>Verne's Mysterious Island</td></tr><tr><td>165</td><td>A Samurai's Vengeance</td></tr><tr><td>166</td><td>Star Trek™ Pinball: Kelvin Timeline</td></tr><tr><td>167</td><td>Xena: Warrior Princess Pinball</td></tr><tr><td>168</td><td>Williams™ Whirlwind</td></tr><tr><td>169</td><td>Star Trek™ Pinball: Discovery</td></tr><tr><td>170</td><td>Battlestar Galactica Pinball</td></tr><tr><td>172</td><td>Star Trek™ Pinball: Deep Space Nine</td></tr><tr><td>173</td><td>Terraforming Mars Pinball</td></tr><tr><td>177</td><td>Knight Rider Pinball</td></tr><tr><td>178</td><td>Exploding Kittens®: A Pinball Cat-astrophe</td></tr><tr><td>179</td><td>Gloomhaven™ Pinball</td></tr><tr><td>181</td><td>A Charlie Brown Christmas™ Pinball</td></tr><tr><td>182</td><td>Tomb Raider Pinball: Adventures of Lara Croft</td></tr><tr><td>183</td><td>System Shock Pinball</td></tr><tr><td>184</td><td>The Princess Bride Pinball</td></tr><tr><td>186</td><td>Pacific Rim Pinball</td></tr><tr><td>187</td><td>Goat Simulator Pinball</td></tr><tr><td>188</td><td>Banzai Run™</td></tr><tr><td>189</td><td>Earthshaker!™</td></tr><tr><td>190</td><td>Black Knight™ 2000</td></tr><tr><td>191</td><td>Camp Bloodbrook</td></tr><tr><td>192</td><td>Tomb Raider Pinball: Secrets of Croft Manor</td></tr><tr><td>194</td><td>PIN·BOT™</td></tr><tr><td>195</td><td>WHO dunnit™</td></tr><tr><td>196</td><td>TAXI™</td></tr><tr><td>197</td><td>Williams™ Pinball: Elvira and the Party Monsters</td></tr><tr><td>198</td><td>Williams™ Pinball: Scared Stiff</td></tr><tr><td>199</td><td>Comet™</td></tr><tr><td>200</td><td>Fire!™</td></tr><tr><td>201</td><td>Diner™</td></tr><tr><td>202</td><td>Judge Dredd™</td></tr></tbody></table>

Official list: [pinballfx.com](https://www.pinballfx.com/?page_id=7754).

</details>

Epic Games Store version: started with the **nonsteam** version (`emulators\pinballfx` folder), the table starts, but without the Epic online services (no leaderboards).

## Controls

The game handles the controller itself (XInput controller recommended): RetroBat does not change its configuration. Controls are changed in the game options.

<table><thead><tr><th width="261.5">Action</th><th>Controller</th></tr></thead><tbody><tr><td>Left flipper</td><td>L1 or L2</td></tr><tr><td>Right flipper</td><td>R1 or R2</td></tr><tr><td>Launch the ball</td><td>Right stick down (pull, then release)</td></tr><tr><td>Auto launch the ball</td><td>SOUTH</td></tr><tr><td>Backbox view</td><td>Right stick up</td></tr><tr><td>Nudge the table</td><td>Left stick</td></tr><tr><td>Visual extras</td><td>EAST</td></tr><tr><td>Wizard power</td><td>WEST</td></tr><tr><td>Change view</td><td>NORTH</td></tr><tr><td>Menu</td><td>START or SELECT</td></tr></tbody></table>

## Hotkeys

<table><thead><tr><th width="247.75">Action</th><th>Controller</th></tr></thead><tbody><tr><td>Quit the game</td><td>HOTKEY + START</td></tr></tbody></table>

The Game Control Center is not available for these systems.

## Useful options

In the advanced system or game settings:

* **GAME OPTIONS > GAME MODE**: mode started with the table. When not set, the game keeps the mode chosen in its menu.

<table><thead><tr><th width="287.75">Choice</th><th>Game mode</th></tr></thead><tbody><tr><td>Classic</td><td>Classic game (<code>Classic</code>)</td></tr><tr><td>Pro</td><td>Pro mode (<code>Pro</code>)</td></tr><tr><td>Practice</td><td>Practice (<code>Practice</code>)</td></tr><tr><td>Hotseat 2 / 3 / 4 Players</td><td>Multiplayer, taking turns (<code>Hotseat_2</code> to <code>Hotseat_4</code>)</td></tr><tr><td>1 ball challenge</td><td>One ball only (<code>Challenge_BallLimited</code>)</td></tr><tr><td>5 minute time challenge</td><td>Game limited to 5 minutes (<code>Challenge_TimeLimited</code>)</td></tr><tr><td>Distance challenge</td><td>Distance challenge (<code>Challenge_DistanceLimited</code>)</td></tr><tr><td>Flips challenge</td><td>Limited number of flips (<code>Challenge_FlipLimited</code>)</td></tr></tbody></table>

* **VIDEO > VIDEO MODE**: Windows resolution during the game.
* **EMULATION > KILL LAUNCHER WHEN EXIT**: closes Steam when quitting the game (steam version).

A mode that does not exist for the table is ignored: the table starts with its default settings.

## Folders

<table><thead><tr><th width="259">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Tables</td><td><code>roms\pinballfx</code></td></tr><tr><td>Game (nonsteam version)</td><td><code>emulators\pinballfx</code></td></tr><tr><td>Saves, scores, settings</td><td>Handled by the game (and by Steam)</td></tr></tbody></table>

## Known issues

* **The game opens without starting the table**: you do not own the table, or its number is wrong.
* **"'….table' must contain the table number on its first line."**: the `.table` file is empty or does not contain a number.
* **"Game not found: copy it in '…'"** (nonsteam version): the game is not in the given folder, or its executable has another name.
* **"Steam is not installed."** (steam version): Steam was not found.
