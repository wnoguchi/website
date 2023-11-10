# Change FortiGate GUI / CLI Session Timeout

デフォルトは死ぬほど短い。本番運用時はいいかもしれないが、開発、検証中には向かない。

管理アクセスのタイムアウト時間を設定したい
https://csps.hitachi-solutions.co.jp/fortinet/faq/FG-01-0023/index.html

```
config system global
    set admintimeout <1 - 480 (min)   default = 5)>
end
```

```
FortiGate-VM64-KVM # config system global

FortiGate-VM64-KVM (global) # show
config system global
    set alias "FortiGate-VM64-KVM"
    set hostname "FortiGate-VM64-KVM"
    set timezone 04
end

FortiGate-VM64-KVM (global) # show full-configuration | grep admintimeout
    set admintimeout 5

FortiGate-VM64-KVM (global) # set admintimeout
admintimeout    Enter an integer value from <1> to <480> (default = <5>).

FortiGate-VM64-KVM (global) # show
config system global
    set admintimeout 480
    set alias "FortiGate-VM64-KVM"
    set hostname "FortiGate-VM64-KVM"
    set timezone 04
end

FortiGate-VM64-KVM (global) # end
```
