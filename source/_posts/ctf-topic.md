---
title: ctf_topic
date: 2022-08-21 23:11:45
tags:ctf
---

很遗憾，不知道为什么改的文件基本不生效，甚至会瘫痪

```python
爆破e , 排除错误写法:
for e in range(10000):
    if gmpy2.is_prime(e):
        try:
            d = gmpy2.invert(e, phi_n)
            m = gmpy2.powmod(c, d, n)
            flag = libnum.n2s(int(m))
            if 'flag' in str(flag) or "ctf" in str(flag):
                print(flag)
        except ZeroDivisionError:
            continue
  # 写这道ctf题的时候，emm..倒是犯了互不互质的问题。
           
```

