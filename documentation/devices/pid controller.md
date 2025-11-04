The PID controller logic chip allows you to implement PID functionality without the complexity of writing your own. 

BUGS:
1. The PID controller does not store configuration values properly between world exit/start so code should expect these values to be reset, and should write them again.
2. The PID controller does not properly reset time-series calculations when settings change, so a manual reset should be called when settings are updated.
3. The P, I, and D configuration values cannot be set by a screwdriver or labeler in game, and must be set using IC10 code.
4. The values stored in the PID controller settings do not always present properly when read back, even if they were set correctly.