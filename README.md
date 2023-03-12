# Patches applied

I added volume control:

config.h
```
/* ... */
/* Volume controls */
static const char *vol_down[] = { "amixer", "-c", "1", "set", "Master", "10%-", NULL };
static const char *vol_up[] = { "amixer", "-c", "1", "set", "Master", "10%+", NULL };
/* ... */

```
```
static Key keys[] = {
	{ 0,                            XK_F2,     spawn,          {.v = vol_down } },
	{ 0,                            XK_F3,     spawn,          {.v = vol_up } },
};
```
