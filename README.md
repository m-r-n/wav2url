THE IDEA: Storing audio messages on url servers.
--
For testing purposes, an executable 'pcode' file for Matlab is provided.
The file will automatically install into Matlab under "Apps".
Yes, Matlab is needed to test it.
Functions: recording, uploading, downloading, playback of audio messages.
--- more details ---
1. Audio files are cut into frames. 
2. These audio frames are stored as url-strings on name-servers.
3. Neighboring audio frames are linked using the hash of neighbouring frames.
4. When uploading, the hash of the prev frame is appended to the actual frame.
5. The audio file is restored (downloaded) by using only the last hash.
6. Since these hashes are (usually) 8 character long,
by transmitting those 8 characters, we can "transmit" the audio msg.
--
