### When I open a swift pitch perfect project in xcode , ui elements didn't appear in the xcode main.storyboard view but when I run the projects it's appear in the simulator ? ﻿
Question by  kuhan Nagalingam and Ans by Atikur Rahman 

You need to change size class from storyboard. Check this documentation page for details about how to change size class -

https://developer.apple.com/library/ios/recipes/xcode_help-IB_adaptive_sizes/chapters/SelectingASizeClass.html

Most probably, user selected "Compact Width | Regular Height", which corresponds to iPhone in portrait orientation.﻿
