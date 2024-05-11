# social-video-HD Converter
i extract the output codec of Whatsapp+Tiktok+Youtube/Short+Instagram. Then place they codec to this app,

You need install python first to run this app,
https://www.python.org/downloads/


1. Select video in input
2. Select output folder
3. Select the Social Codec for your video to be HD 
4. Convert
5. Upload 

Rules:
1. Basic Video must be HD at 720-4k
2. 59 Sec Duration (or you can try more duration, in tiktok 2min i still get HD same codec).
`'Then when you upload them in to Social you choose, they will still HD because the video not need to Convert again in the Social. Social will read that the video have same codec with them'`

## Note
Tiktok Codec same can use in Whatsapp too, because Tiktok also use the Whatsapp codec, they will HD output when you upload the converted video.


This is the codec i have extracted from many video HD at Tiktok, Whatsapp, Youtube, Instagram
       
           "TikTok":
            command = f'ffmpeg -i "{input_file}" -vf "{scale_option}" -c:v h264 -profile:v high -b:v 2057k -r 60 -c:a aac -ar 44100 -ac 2 -b:a 128k "{output_filename}"'

            "Youtube":
            command = f'ffmpeg -i "{input_file}" -vf "{scale_option}" -c:v vp9 -b:v 18591k -r 60 -c:a aac -ar 44100 -ac 2 -b:a 127k "{output_filename}"'

            "Youtube Short":
            command = f'ffmpeg -i "{input_file}" -vf "{scale_option}" -c:v vp9 -b:v 9290k -r 60 -c:a aac -ar 44100 -ac 2 -b:a 127k "{output_filename}"'

            "Instagram":
            command = f'ffmpeg -i "{input_file}" -vf "{scale_option}" -c:v h264 -profile:v high -b:v 2549k -r 30 -c:a aac -ar 44100 -ac 2 -b:a 128k "{output_filename}"'
