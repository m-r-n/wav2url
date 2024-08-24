THE IDEA: Storing audio messages on url servers.
--
For testing purposes, 2 executables for Matlab are provided.
The files will automatically install into Matlab under "Apps".
Functions: recording, uploading, downloading, playback of audio messages.


1. After recording the msg, audio files are cut into frames. 
2. These audio frames are stored as url-strings on name-servers.
3. Neighboring audio frames are linked using the hash of neighbouring frames.
4. When uploading, the hash of the prev frame is appended to the actual frame.
5. When downloading, the hash of the prev frame is read from the actual frame.
6. To download any audio file, the only thing we need is the hash of its last frame. 
7. Since those hashes are (usually) 8 character long,
by transmitting those 8 characters, we can virtually "transmit" the audio msg.

