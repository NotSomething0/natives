---
ns: VEHICLE
aliases: ["0x2FA2494B47FDD009"]
---
## SET_TRAILER_ATTACHMENT_ENABLED

```c
// SetTrailerAttachmentEnabled
void SET_TRAILER_ATTACHMENT_ENABLED(Vehicle vehicle, BOOL enabled);
```

Sets whether the a trailer can attach to vehicles or not

## Parameters
* **vehicle**: The trailer to set attachment state for
* **enabled**: Enable or disable attachment

## Examples

```lua
  local trailerModel = GetHashKey('tanker')
  local trailerCoordinates = vector3(-323.59, -757.83, 53.25)
  local trailerHeading = 247.77

  RequestModel(trailerModel)

  while not HasModelLoaded(trailerModel) do
    Wait(0)
  end

  local trailerIndex = CreateVehicle(trailerModel, trailerCoordinates.x, trailerCoordinates.y, trailerCoordinates.z, trailerHeading, true, false)

  SetTrailerAttachmentEnabled(trailerIndex, false)
  SetModelAsNoLongerNeeded(trailerModel)
```