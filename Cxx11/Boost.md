# Homebrew

Install Boost like this:
```
brew install boost boost-bcp
```

Create a "minimal" collection of headers that you can copy elsewhere:
```
bcp --boost=/usr/local/Cellar/boost/1.64.0_1/include boost/range/irange.hpp .
```

Then change this line in `prk_util.h` from
```
# include <boost/range/irange.hpp>
```
to
```
# include "boost/range/irange.hpp"
```
and make sure that the `boost/` subdirectory generated by `bcp` lives in `PRK/Cxx11/.`
