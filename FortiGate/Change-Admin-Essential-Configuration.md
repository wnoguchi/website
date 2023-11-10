# FortiGate の最初の設定

## タイムゾーン

```
config system global
    set timezone 60
end
```

## 言語

```
config system global
    set language japanese
end
```

## タイムアウト

```
config system global
    set admintimeout 480
end
```

## ログ

```
FortiGate-VM64-KVM # show system global
config system global
    set admintimeout 480
    set alias "FortiGate-VM64-KVM"
    set hostname "FortiGate-VM64-KVM"
    set language japanese
    set timezone 60
end

FortiGate-VM64-KVM (global) # set language
english       English.
french        French.
spanish       Spanish.
portuguese    Portuguese.
japanese      Japanese.
trach         Traditional Chinese.
simch         Simplified Chinese.
korean        Korean.

FortiGate-VM64-KVM (global) # set timezone
01    (GMT-11:00) Midway Island, Samoa
02    (GMT-10:00) Hawaii

(snip)

58    (GMT+8:00) Perth
59    (GMT+8:00) Taipei
60    (GMT+9:00) Osaka, Sapporo, Tokyo, Seoul
62    (GMT+9:30) Adelaide
63    (GMT+9:30) Darwin

(snip)

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
