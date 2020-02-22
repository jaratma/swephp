# swephp
Swiss Ephemeris minimalist port to PHP 7.4

This is a minimal php 7.4 extension for awesome Swiss Epehemeris 2.08 library, from astro.com. Get sources, data and docs from them.

## Build

Make sure you have the Swiss library compiled and installed as a dynamic lib (`libswe.so`), 
and header files installed in a standard location - `/user/local/include/swe` p.e.

Clone this repo: git clone https://github.com/jaratma/swephp.git

In project directory:
```
$ phpize
$ ./configure
$ make
// check:
$ php -d extension=modules/swephp.so --re swephp 
```

## Implemented Functions

- swe_version
- swe_get_library_path
- swe_calc_ut
- swe_houses
- swe_get_planet_name
- swe_julday
- swe_date_conversion
- swe_revjul
- swe_set_ephe_path // automatic (see below)
- swe_close // automatic

If you set env variable for data location:

`export SE_EPHE_PATH=/usr/share/ephe`

library/extension will pick it at load time and no more steps are needed. This is as it is by now, although you could configure the extension to use inner calculation instead of data.  

