Working-with-Media
Working With Audio
To create a visually appealing dog image, use the figcaption element to wrap the text and designate it as a caption. Place the image and caption together in a figure element, providing more information about the content and connecting it to search engines and AI. These elements are useful for visual illustrations and concept demonstrations.
<!--<audio controls src="audio.mp3"></audio> -->

The text suggests linking to an MP3 file, but it doesn't provide any useful controls. The user should request the browser to offer play button, timeline, and volume control, but using built-in controls is optional.

Create your own audio player controls using JavaScript and the HTML media element API. Add the "controls" attribute, allowing for play, pause, volume adjustment, time display, and timeline navigation. This exercise showcases the power of HTML in providing functionality without creating it from scratch.

Note:The audio element can be manipulated using attributes like "loop" to repeat the file from its beginning, and "autoplay" to automatically play the audio upon page load, but caution is advised as it may cause discomfort.

To support multiple audio file formats, remove the source attribute from the audio element and place it on a separate source element. This allows for the addition of other source elements with alternative audio file formats. MP3s are widely supported in modern browsers, while OGG has some advantages but has not gained popularity. There is no second audio format recommended at the moment, but understanding syntax for supporting multiple formats is crucial in the future.

Note:Create multiple files and list them in separate source elements, and the browser will use the first compatible file in the list.

The audio element in HTML offers fallback text for browsers that don't understand it, demonstrating its resilience and versatility in displaying audio files and player content.

Working with Video
The source attribute specifies the video file, and adding the controls attribute automatically creates a video player in the browser. However, some issues need to be addressed.

Video files are encoded using various codecs like Real Video, Sorenson, Windows Media, Flash, and H.263. H.264 was the dominant codec from 2015 to 2020, but it's a patented codec owned by a consortium that charges licensing fees for devices, operating systems, browsers, and cameras. They plan to increase fees for H.265.

H.264, unlike other free image file formats like JPEG or GIF, is proprietary. This raises the question of why video codecs should be treated differently, as web technologies like HTML and CSS are not patented. Efforts have been made to create an open, non-patented video codec.

The WebM versus AV1 debate remains uncertain, with AV1 potentially being a superior video codec and free of royalty charges. HTML video elements allow simultaneous use of H.264, WebM, and AV1, with browsers playing compatible files.

HTML doesn't automatically adjust video sizes based on network conditions, causing devices to adapt resolutions. Major streaming platforms like Netflix, Hulu, HBO, YouTube, and Vimeo use adaptive bitrate streaming, a server farm of transcoding robots, to ensure seamless switching between different resolutions.

Working With Capitons and Subtitles
Websites can incorporate audio and video content, but not everyone can fully comprehend it due to factors like hearing loss, intermittent hearing, or other limitations.

The track element will be linked to a text file to add captions to a video, allowing viewers to toggle captions or switch subtitle options. The web video text tracks will be used, with each line accompanied by a time code.

To display captions on a video, insert a track element within the video element, specifying the file, kind, label, language, and default attribute. Use the source attribute to specify the file, the kind attribute to display captions, and the lang attribute to indicate language.

The captioning icon allows users to turn off captions, enable automatic captioning, or select English captions. To include Spanish subtitles, set the kind attribute to "subtitles", source lang to "es", and label attribute to "Español", resulting in a second subtitle option.

The kind attribute offers options like "descriptions" for visual descriptions, making videos accessible to visually impaired users, and "chapters" for text files listing video sections, allowing users to jump to specific parts.

Embedding Media via Iframes
You're likely to use a video hosting service to embed their video player onto a webpage instead of handling it directly.

Note:Embedding refers to taking content from one site and placing it within the middle of another site's page. 
There is a wide range of content that can be embedded on a page. For instance, a map from Google or Mapbox, a code demo from CodePen or Glitch, or even a slide deck from Speaker Deck or Notist. It is common practice to embed complex content from a service that handles the technical aspects. Instead of figuring out how to build a mapping service, a slide deck system, a code demo platform, or an adaptive bitrate server, you can rely on someone else's toolkit to handle all of that. 

Iframes are powerful but security concerns arise when using content management systems like WordPress or Drupal. These platforms may not allow random embed codes from trusted sources, so it's best to consult an expert.

