---
title: clion에서 bits/stdc++.h 사용하기
date: 2021-03-14-14:30
categories:
- Tool

tags:
- IDE
- Clion
- Cpp

---

## clion에서 bts/stdc++.h 을 사용하도록 해봅니다.
> windos의 vs와 마찬가지로, 직접 만들어 주어야 합니다.


### Goal
- bits/stdc++.h 파일을 clion에서 include 할수 있도록 세팅해본다.

---

## include/bits 폴더를 만들어준다.

```
cd /usr/local/include
```

- include 폴더 접근

```
mkdir bits
cd bits
```

- bits 디렉토리 생성 후 접근

---

## stdc++.h 파일을 만들어 준다.
```
vi stdc++.h
```

- 아래 내용을 붙여넣는다.
- 혹은 [링크](https://github.com/tekfyl/bits-stdc-.h-for-mac/blob/master/stdc%2B%2B.h) 의 파일을 다운받는다.

```
// C++ includes used for precompiling -*- C++ -*-

// Copyright (C) 2003-2013 Free Software Foundation, Inc.
//
// This file is part of the GNU ISO C++ Library.  This library is free
// software; you can redistribute it and/or modify it under the
// terms of the GNU General Public License as published by the
// Free Software Foundation; either version 3, or (at your option)
// any later version.

// This library is distributed in the hope that it will be useful,
// but WITHOUT ANY WARRANTY; without even the implied warranty of
// MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
// GNU General Public License for more details.

// Under Section 7 of GPL version 3, you are granted additional
// permissions described in the GCC Runtime Library Exception, version
// 3.1, as published by the Free Software Foundation.

// You should have received a copy of the GNU General Public License and
// a copy of the GCC Runtime Library Exception along with this program;
// see the files COPYING3 and COPYING.RUNTIME respectively.  If not, see
// <http://www.gnu.org/licenses/>.

/** @file stdc++.h
 *  This is an implementation file for a precompiled header.
 */

// 17.4.1.2 Headers

// C
#ifndef _GLIBCXX_NO_ASSERT
#include <cassert>
#endif
#include <cctype>
#include <cerrno>
#include <cfloat>
#include <ciso646>
#include <climits>
#include <clocale>
#include <cmath>
#include <csetjmp>
#include <csignal>
#include <cstdarg>
#include <cstddef>
#include <cstdio>
#include <cstdlib>
#include <cstring>
#include <ctime>

#if __cplusplus >= 201103L
#include <ccomplex>
#include <cfenv>
#include <cinttypes>
#include <cstdbool>
#include <cstdint>
#include <ctgmath>
#include <cwchar>
#include <cwctype>
#endif

// C++
#include <algorithm>
#include <bitset>
#include <complex>
#include <deque>
#include <exception>
#include <fstream>
#include <functional>
#include <iomanip>
#include <ios>
#include <iosfwd>
#include <iostream>
#include <istream>
#include <iterator>
#include <limits>
#include <list>
#include <locale>
#include <map>
#include <memory>
#include <new>
#include <numeric>
#include <ostream>
#include <queue>
#include <set>
#include <sstream>
#include <stack>
#include <stdexcept>
#include <streambuf>
#include <string>
#include <typeinfo>
#include <utility>
#include <valarray>
#include <vector>

#if __cplusplus >= 201103L
#include <array>
#include <atomic>
#include <chrono>
#include <condition_variable>
#include <forward_list>
#include <future>
#include <initializer_list>
#include <mutex>
#include <random>
#include <ratio>
#include <regex>
#include <scoped_allocator>
#include <system_error>
#include <thread>
#include <tuple>
#include <typeindex>
#include <type_traits>
#include <unordered_map>
#include <unordered_set>
#endif
```

## clion 확인

![image](https://user-images.githubusercontent.com/43930419/111025177-dfe64a80-8425-11eb-9961-844b5e3dd997.png)


- stdc++.h 를 사용할 수 있는것을 확인할 수 있다.


---

## 어느날 갑자기 인식을 못하는경우

> 3개월만에 clion을 켜봤는데, 되던것이 갑자기 안되기 시작했다.

- 해당 [링크](https://www.programmersought.com/article/2741905913/)의 글을 보고 따라 해결했다.


```console
/usr/local/bin
```

![image](https://user-images.githubusercontent.com/43930419/121769531-18213480-cb9f-11eb-8b4f-a966eb894fd5.png)

- 위의 커맨드를 입력해, 현재 설치된 버전을 확인한다.
  - 나의 경우 `g++-10`

![image](https://user-images.githubusercontent.com/43930419/121769569-469f0f80-cb9f-11eb-96f2-7084782491d1.png)

- CMake 옵션을 설치된 컴파일러 버전으로 바꾸어준다.

![image](https://user-images.githubusercontent.com/43930419/121769617-941b7c80-cb9f-11eb-83cc-79e092657ada.png)

- 다시 잘되기 시작했다 
- 근데 이러면 디버깅 모드에 문제가 발생한다 -_-
  - m1 실리콘 이슈인거 같은데.. 나중에 해결해보려고한다.
  - https://youtrack.jetbrains.com/issue/CPP-24197

### 다른 해결방법
> 일단 반드시 clion을 업데이트 해야한다!!!!!!!!!!!!!!

![image](https://user-images.githubusercontent.com/43930419/121770800-7dc4ef00-cba6-11eb-8b46-66f9c7d4385f.png)

- [링크](https://codeforces.com/blog/entry/70957?#comment-676543)를 참고했다.
- **반드시 clion을 업데이트 해야한다!!!!!!!!!!!!!!**


```console
/Library/Developer/CommandLineTools/SDKs/MacOSX11.3.sdk/usr/include/c++/v1/

sudo mkdir bits
cd bits
sudo vi stdc++.h 
```

- 드디어 일단 해결...
- 디버깅 모드도 잘 진행된다.

![image](https://user-images.githubusercontent.com/43930419/121770807-874e5700-cba6-11eb-925e-4cdf135b1a00.png)



---

## 추가팁
> c++17을 사용하도록 세팅하는법

![image](https://user-images.githubusercontent.com/43930419/111058623-1f1ea500-84d3-11eb-9485-91d24f80aee8.png)

- set `CMAKE_CXX_STANDARD 14)` 를 사진과 같이 17로 바꾸어준다.

![image](https://user-images.githubusercontent.com/43930419/111058690-62791380-84d3-11eb-8518-c7c9534b296e.png)

- `c++17` 부터 추가된 gcd, lcm 을 사용할 수 있는것을 확인할 수 있다.


---

## Reference
- https://hellogaon.tistory.com/63
- https://subinium.github.io/xcode-header
- https://www.programmersought.com/article/2741905913