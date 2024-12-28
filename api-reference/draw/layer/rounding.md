# rounding

This enum is used to determine the rounding for rounded shapes.

### tl﻿ <a href="#tl" id="tl"></a>

Field

Round top-left corner.

### tr﻿ <a href="#tr" id="tr"></a>

Field

Round top-right corner.

### bl﻿ <a href="#bl" id="bl"></a>

Field

Round bottom-left corner.

### br﻿ <a href="#br" id="br"></a>

Field

Round bottom-right corner.

### t﻿ <a href="#t" id="t"></a>

Field

Round both of the top corners. This produces the same result as using `bit.bor(draw.rounding.tl, draw.rounding.tr)`.

### l﻿ <a href="#l" id="l"></a>

Field

Round both of the left corners. This produces the same result as using `bit.bor(draw.rounding.tl, draw.rounding.bl)`.

### r﻿ <a href="#r" id="r"></a>

Field

Round both of the right corners. This produces the same result as using `bit.bor(draw.rounding.tr, draw.rounding.br)`.

### b﻿ <a href="#b" id="b"></a>

Field

Round both of the bottom corners. This produces the same result as using `bit.bor(draw.rounding.bl, draw.rounding.br)`.

### all﻿ <a href="#all" id="all"></a>

Field

Round all corners. This produces the same result as using `bit.bor(draw.rounding.tl, draw.rounding.tr, draw.rounding.bl, draw.rounding.br)`.
