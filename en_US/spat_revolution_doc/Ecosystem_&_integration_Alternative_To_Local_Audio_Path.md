# Alternative to local audio path

## Pro and cons of the local audio path

The local audio path is designed to easily create audio connections between an audio application that can host plug-ins and SPAT Revolution, while also providing the automation data.

But in some cases, LAP can met some limitations due to the used DAW. For example, both Logic and Ableton Live have some internal strategy to save CPU usage which can generate issues with our SPAT send and return plug-ins.

Also, as most DAW only allow for pre-fader and pre-mute plug-ins insert, this can either lead to some constraint on the mixing workflow or very much complexify the routing to allow post-fader send to SPAT Revolution.

When dealing with such issues, it is interesting to look at virtual loopback devices.

## Virtual loopback devices

Virtual loopback devices allows to take the audio output of an application to fed another application. In this case, we use the direct out of our DAW console to feed the input of SPAT Revolution. In case we would like to record our mix, we will then need to send back the output of SPAT Revolution to our DAW.

### Virtual loopback with macOS

Inside the macOS environnement, you will need to download a virtual driver, such as [Blackhole](https://github.com/ExistentialAudio/BlackHole), to send audio from one application to another.

When using application that support different input and output devices (such as SPAT Revolution of Ableton Live), you could for exemple set your DAW to use an audio interface as an input, set its output to blackhole, and do the opposite in SPAT Revolution.

If your application does not support different i/o devices, you could try to use aggregate audio, but beware, the latency may be greatly increased.

### Virtual loopback with Windows

Unfortunatly, Windows audio environnement is very much less prompt to multi-client audio connections. Thus, there's no many solution for software loopback inside Microsoft OS.

However, some audio interfaces, such as RME ones, allows to loopback an output. If your audio interface as enough audio output, it can be a good solution.