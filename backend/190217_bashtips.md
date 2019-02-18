[TOC]

# tips

```bash
if [ -z $verableshouldexist ]; then
    return 2>/dev/null || exit
fi
```

1，需要 source 的 bash 脚本可以 return || exit，
return 不会使当前执行的 channel 退出，exit 会，
bash 里的 || 运算符，会先执行左值，如果返回 true，则停止，否则执行右值
不是通过 source 执行的 bash 脚本 return 会失败，然后执行 exit

2，不需要的 stderr 可以重定向到 /dev/null，即就是不打印 stderr

3，-z 可以判断 variable 是否为 empty
