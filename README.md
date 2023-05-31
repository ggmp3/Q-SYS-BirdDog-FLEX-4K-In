# Q-SYS-BirdDog-FLEX-4K-In

- BirdDog FLEX 4K IN Q-Sys User Component (REST API)
- Written by Glen Gorton
- Tested with Firmware version: BirdDog Flex_In 4.5.192-LTS


## NOTES:
  
1. If a response string is corrupt it will contain %!s(<nil>). Within the Result() function I have added a check that if this is discovered it will SetStatus to compromised, then the pollTimer will start again after one hour. "Settings Status with Code: '1', Message: 'Data response for query (decodesetup) from the device is corrupt: %!s(<nil>). May require a reboot or firmware reload."
Response example: {VideoSampleRate":"%!s(<nil>)","NDIAudio":"%!s(<nil>)}
