# scaling-resolution
[documentation](https://docs.microsoft.com/en-us/windows/win32/api/wingdi/ne-wingdi-displayconfig_scaling)

# location 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\GraphicsDrivers\Configuration\ACR06D42451618332_16_07E3_CC^EB03C515D889ECFCFBC9471DDD63665B\00\00  
"Scaling"=dword:00000001  
your folder will be different from my acr folder. if you use dual monitors it will have more folders than just 00  
scaling=1 should be no change as documented in the link above and pasted below


```DISPLAYCONFIG_SCALING_IDENTITY
Value: 1
Indicates the identity transformation; the source content is presented with no change. This transformation is available only if the path's source mode has the same spatial resolution as the path's target mode.
DISPLAYCONFIG_SCALING_CENTERED
Value: 2
Indicates the centering transformation; the source content is presented unscaled, centered with respect to the spatial resolution of the target mode.
DISPLAYCONFIG_SCALING_STRETCHED
Value: 3
Indicates the content is scaled to fit the path's target.
DISPLAYCONFIG_SCALING_ASPECTRATIOCENTEREDMAX
Value: 4
Indicates the aspect-ratio centering transformation.
DISPLAYCONFIG_SCALING_CUSTOM
Value: 5
Indicates that the caller requests a custom scaling that the caller cannot describe with any of the other DISPLAYCONFIG_SCALING_XXX values. Only a hardware vendor's value-add application should use DISPLAYCONFIG_SCALING_CUSTOM, because the value-add application might require a private interface to the driver. The application can then use DISPLAYCONFIG_SCALING_CUSTOM to indicate additional context for the driver for the custom value on the specified path.
DISPLAYCONFIG_SCALING_PREFERRED
Value: 128
Indicates that the caller does not have any preference for the scaling. The SetDisplayConfig function will use the scaling value that was last saved in the database for the path. If such a scaling value does not exist, SetDisplayConfig will use the default scaling for the computer. For example, stretched (DISPLAYCONFIG_SCALING_STRETCHED) for tablet computers and aspect-ratio centered (DISPLAYCONFIG_SCALING_ASPECTRATIOCENTEREDMAX) for non-tablet computers.
DISPLAYCONFIG_SCALING_FORCE_UINT32
Value: 0xFFFFFFFF
Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. You should not use this value.```
