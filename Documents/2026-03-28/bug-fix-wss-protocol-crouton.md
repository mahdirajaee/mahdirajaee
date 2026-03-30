# Bug Fix: WSS Protocol in edfungus/Crouton

## Date
2026-03-28

## Summary
Fixed a bug in the Crouton project (edfungus/Crouton) where checking the "WSS Protocol" checkbox in the MQTT connection dialog would set the protocol to `"ws"` instead of `"wss"`. This meant secure WebSocket connections were never actually established even when explicitly requested by the user.

The fix was a one-line change: replacing `this.protocol = "ws"` with `this.protocol = "wss"` inside the `if(this.wssProtocol == true)` block.

## Files Modified
- `public/app/framework/crouton-connect-mqtt/crouton-connect-mqtt.pug` (line 157)

## References
- Issue: https://github.com/edfungus/Crouton/issues/55
- PR: https://github.com/edfungus/Crouton/pull/58
