# font\_flags

This enum determines which flags a font object should possess. Setting those flags is only possible during type construction.

### shadow﻿ <a href="#shadow" id="shadow"></a>

Field

Adds a 1px shadow to font glyphs.

### outline﻿ <a href="#outline" id="outline"></a>

Field

Adds a 1px outline to font glyphs.

### anti\_alias﻿ <a href="#anti-alias" id="anti-alias"></a>

Field

Enable antialiasing on font glyphs. This flag only works on GDI fonts.

### no\_dpi﻿ <a href="#no-dpi" id="no-dpi"></a>

Field

Disable DPI scaling on this font. By default, font glyphs will be scaled in accordance to the global DPI scale.

### no\_kern﻿ <a href="#no-kern" id="no-kern"></a>

Field

Disable glyph kerning on this font.

### mono﻿ <a href="#mono" id="mono"></a>

Field

Enables a strong hinting algorithm for rasterization. Only works on FreeType fonts.

### light﻿ <a href="#light" id="light"></a>

Field

Enables a light hinting algorithm for rasterization. Only works on FreeType fonts.
