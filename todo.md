
だださん　USB-DAC音量バグ対策案
```
音量が 30% になるまで USB DAC から音が出ない
USB DAC の中には、ある一定の音量に達するまで音が出なくなるものがあります [10] 一般的にこれは約 25%〜30% で、最初の音量が不快なほど大きくなり、低い音量を維持することができなくなります。解決策としては、["api.alsa.soft-mixer"] を true に設定して、ハードウェアミキサーの音量コントロールを無視することが挙げられます。

wireplumber でこれを実現するには、/usr/share/wireplumber/main.lua.d/50-alsa-config.lua 設定に次を使用して構成フラグメントを追加します。 table.insert:

~/.config/wireplumber/main.lua.d/51-volume-fix.lua
table.insert (alsa_monitor.rules, {
    matches = {
      {
        -- This matches all cards.
        { "device.name", "matches", "alsa_card.*" },
      },
    },
    -- Apply properties on the matched object.
    apply_properties = {
      -- Don't use the hardware mixer for volume control. It
      -- will only use software volume. The mixer is still used
      -- to mute unused paths based on the selected port.
      ["api.alsa.soft-mixer"] = true,
    }
  })
次に、pipewire を再起動します。alsamixer でマスターボリュームを設定し、# alsactl store で設定を保存します。これで、ボリュームミキサーを通常どおり使用できるようになります。

```
