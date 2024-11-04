---
ns: VEHICLE
aliases: ["0x2FA2494B47FDD009"]
---
## SET_TRAILER_ATTACHMENT_ENABLED

```c
// SetTrailerAttachmentEnabled
void SET_TRAILER_ATTACHMENT_ENABLED(Vehicle vehicle, BOOL enabled);
```

## Parameters
* **vehicle**: The trailer to set the attachment state for
* **enabled**: Enable or disable trailer attachment

## Examples

```lua
  local trailerModel = `tanker`

  RequestModel(trailerModel)

  while not HasModelLoaded(trailerModel) do
    Wait(0)
  end

  local trailerIndex = CreateVehicle(trailerModel, 0.0, 0.0, 0.0, 0.0, true, false)

  SetTrailerAttachmentEnabled(trailerIndex, false)
  SetModelAsNoLongerNeeded(trailerIndex)
```