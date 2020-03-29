# CV CI Pipeline [![Build Status](https://travis-ci.org/Fmrhj/cv-pipeline.svg?branch=master)](https://travis-ci.org/Fmrhj/cv-pipeline)

Continuous integration to build a CV with:
- [Travis](https://travis-ci.org)
- [Github](https://github.com)
- [Overleaf](https://www.overleaf.com)
- [Dropbox API](https://www.dropbox.com/developers)
- [Docker](https://www.docker.com/)
- [Openssl](https://www.openssl.org)

Based on this [medium article](https://medium.com/@baymac/continuous-integration-of-latex-documents-using-travis-ci-a1916c89e978).

## Further notes 
Some of the things I learnt while developing this solution:
1. Skip builds in travis if you change irrelevant files. After commiting any changes in your repository travis will automatically try to build. There are however many cases where this can be annoying, for example, by commiting minor changes in the `README` file. This can be avoided while adding the following in your commit message: 
 
``` bash 
git commit -m "commit msg [skip ci]"
```
2. Check `$TRAVIS_TAG`it may have conflicts. Check build
