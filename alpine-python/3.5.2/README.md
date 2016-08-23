
## `python:alpine`

This image is based on the popular [Alpine Linux project][34], available in [the `alpine` official image][35]. Alpine Linux is much smaller than most distribution base images (~5MB), and thus leads to much slimmer images in general. 

   [34]: http://alpinelinux.org
   [35]: https://hub.docker.com/_/alpine

This variant is highly recommended when final image size being as small as possible is desired. The main caveat to note is that it does use [musl libc][36] instead of [glibc and friends][37], so certain software might run into issues depending on the depth of their libc requirements. However, most software doesn't have an issue with this, so this variant is usually a very safe choice. See [this Hacker News comment thread][38] for more discussion of the issues that might arise and some pro/con comparisons of using Alpine-based images. 

   [36]: http://www.musl-libc.org
   [37]: http://www.etalabs.net/compare_libcs.html
   [38]: https://news.ycombinator.com/item?id=10782897

To minimize image size, it's uncommon for additional related tools (such as `git` or `bash`) to be included in Alpine-based images. Using this image as a base, add the things you need in your own Dockerfile (see the [`alpine` image description][39] for examples of how to install packages if you are unfamiliar). 

   [39]: https://hub.docker.com/_/alpine/


## Documentation 

Documentation for this image is stored in the [`python/` directory][49] of the [`docker-library/docs` GitHub repo][50]. Be sure to familiarize yourself with the [repository's `README.md` file][51] before attempting a pull request. 

   [49]: https://github.com/docker-library/docs/tree/master/python
   [50]: https://github.com/docker-library/docs
   [51]: https://github.com/docker-library/docs/blob/master/README.md

## Issues 

If you have any problems with or questions about this image, please contact us through a [GitHub issue][52]. If the issue is related to a CVE, please check for [a `cve-tracker` issue on the `official-images` repository first][53]. 

   [52]: https://github.com/docker-library/python/issues
   [53]: https://github.com/docker-library/official-images/issues?q=label%3Acve-tracker

You can also reach many of the official image maintainers via the `#docker-library` IRC channel on [Freenode][54]. 

   [54]: https://freenode.net

