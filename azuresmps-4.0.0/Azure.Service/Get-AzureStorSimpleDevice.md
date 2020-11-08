---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: C5A2A8D2-A840-4712-A8BD-F49C6063D193
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1156b4887e7b97d4e783ec738a939d320fe397a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106292"
---
# <span data-ttu-id="babef-101">Get-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="babef-101">Get-AzureStorSimpleDevice</span></span>

## <span data-ttu-id="babef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="babef-102">SYNOPSIS</span></span>
<span data-ttu-id="babef-103">Kaynağa bağlı cihazları alır.</span><span class="sxs-lookup"><span data-stu-id="babef-103">Gets devices attached to the resource.</span></span>

## <span data-ttu-id="babef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="babef-104">SYNTAX</span></span>

### <span data-ttu-id="babef-105">Boş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="babef-105">Empty (Default)</span></span>
```
Get-AzureStorSimpleDevice [-Type <String>] [-ModelID <String>] [-Detailed] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="babef-106">Identifybyıd</span><span class="sxs-lookup"><span data-stu-id="babef-106">IdentifyById</span></span>
```
Get-AzureStorSimpleDevice [-DeviceId <String>] [-Type <String>] [-ModelID <String>] [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="babef-107">Identifybyname</span><span class="sxs-lookup"><span data-stu-id="babef-107">IdentifyByName</span></span>
```
Get-AzureStorSimpleDevice [-DeviceName <String>] [-Type <String>] [-ModelID <String>] [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="babef-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="babef-108">DESCRIPTION</span></span>
<span data-ttu-id="babef-109">**Get-AzureStorSimpleDevice** cmdlet 'i kaynağa bağlı StorSimple aygıtların bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="babef-109">The **Get-AzureStorSimpleDevice** cmdlet gets a list of StorSimple devices attached to the resource.</span></span>
<span data-ttu-id="babef-110">Cihaz KIMLIĞI, adı, model KIMLIĞI ve türünü belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="babef-110">You can specify device ID, name, model ID, and type.</span></span>
<span data-ttu-id="babef-111">Diğer StorSimple cmdlet 'lerinin cihazlarını belirtmek için bu cmdlet kullanılarak alınan **DeviceID** özelliğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="babef-111">Use the **DeviceID** property obtained by using this cmdlet to specify devices for other StorSimple cmdlets.</span></span>

## <span data-ttu-id="babef-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="babef-112">EXAMPLES</span></span>

### <span data-ttu-id="babef-113">Örnek 1: kaynakta kullanılabilir cihazları alma</span><span class="sxs-lookup"><span data-stu-id="babef-113">Example 1: Get available devices on a resource</span></span>
```
PS C:\>Get-AzureStorSimpleDevice
DeviceId                  : 6f9ab151-39c7-4ded-b7d0-f5b0968f2766
DeviceName                : 8600-: SHX0881018G88
SerialNumber              : SHX0881018G88
DeviceSoftwareVersion     : 6.3.9600.17430
Location                  : 
ModelDescription          : 8600
Status                    : Offline
Type                      : Appliance
TargetIQN                 : iqn.1991-05.com.microsoft:storsimple8600-shx0991018g00e4-target
TimeZone                  : Pacific Standard Time
ActivationTime            : 2015-04-07T16:32:30.2960842Z
AvailableStorageInBytes   : 535363378479104
ProvisionedStorageInBytes : 14392435408896
TotalStorageInBytes       : 549755813888000
UsingStorageInBytes       : 12693995520

DeviceId                  : eb30ea31-c856-4cf2-9a02-aee611d6a3b9
DeviceName                : 8100-Delta 001
SerialNumber              : SHX90391XXXXXXX
DeviceSoftwareVersion     : 6.3.9600.17430
Location                  : 
ModelDescription          : 8100
Status                    : Online
Type                      : Appliance
TargetIQN                 : iqn.1991-05.com.microsoft:storsimple8100-shx90193xxxxxxx-target
TimeZone                  : Eastern Standard Time
ActivationTime            : 2015-03-26T14:53:14.4219391Z
AvailableStorageInBytes   : 205509890146304
ProvisionedStorageInBytes : 14392435408896
TotalStorageInBytes       : 219902325555200
UsingStorageInBytes       : 23904321536

DeviceId                  : edcb0b9b-1ed5-4102-9c5d-c589f7632994
DeviceName                : 8600-Bravo 001
SerialNumber              : SHX0900915G44SY
DeviceSoftwareVersion     : 6.3.9600.17430
Location                  : 
ModelDescription          : 8600
Status                    : Online
Type                      : Appliance
TargetIQN                 : iqn.1991-05.com.microsoft:storsimple8600-shx0900915g44sy-target
TimeZone                  : Eastern Standard Time
ActivationTime            : 2015-03-26T15:36:26.0870525Z
AvailableStorageInBytes   : 535363378479104
ProvisionedStorageInBytes : 14392435408896
TotalStorageInBytes       : 549755813888000
UsingStorageInBytes       : 978893799424
```

<span data-ttu-id="babef-114">Bu komut, bir kaynaktaki kullanılabilir tüm cihazları alır.</span><span class="sxs-lookup"><span data-stu-id="babef-114">This command gets all available devices on a resource.</span></span>
<span data-ttu-id="babef-115">Bu örnekte yalnızca bir cihaz kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="babef-115">In this example, only one device is available.</span></span>

### <span data-ttu-id="babef-116">Örnek 2: bir kaynakta belirli kullanılabilir cihazları alma</span><span class="sxs-lookup"><span data-stu-id="babef-116">Example 2: Get specific available devices on a resource</span></span>
```
PS C:\>Get-AzureStorSimpleDevice -DeviceName "8600-SHX90193XXXXXXX" -Type Appliance -ModelId "8600"
DeviceId                  : f9db31da-8a6c-4718-8f5b-5ce89e600f28
DeviceName                : 8600-SHX90193XXXXXXX
SerialNumber              : SHX90193XXXXXXX
DeviceSoftwareVersion     : 6.3.9600.17430
Location                  : 
ModelDescription          : 8600
Status                    : Online
Type                      : Appliance
TargetIQN                 : iqn.1991-05.com.microsoft:storsimple8600-shx90193xxxxxxx-target
TimeZone                  : Pacific Standard Time
ActivationTime            : 2015-04-07T18:10:46.4524766Z
AvailableStorageInBytes   : 535363378479104
ProvisionedStorageInBytes : 14392435408896
TotalStorageInBytes       : 549755813888000
UsingStorageInBytes       : 14445182976
```

<span data-ttu-id="babef-117">Bu komut, bir kaynaktaki belirtilen ad, tür ve model KIMLIĞI içeren kullanılabilir tüm cihazları alır.</span><span class="sxs-lookup"><span data-stu-id="babef-117">This command gets all available devices on a resource that have the specified name, type, and model ID.</span></span>

### <span data-ttu-id="babef-118">Örnek 3: aygıtın ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="babef-118">Example 3: Get details for a device</span></span>
```
PS C:\>Get-AzureStorSimpleDevice -Name "8600-SHX90193XXXXXXX" -Type Appliance -Detailed
AlertNotification              : Microsoft.WindowsAzure.Management.StorSimple.Models.AlertNotificationSettings
Chap                           : Microsoft.WindowsAzure.Management.StorSimple.Models.ChapSettings
DeviceProperties               : Microsoft.WindowsAzure.Management.StorSimple.Models.DeviceInfo
DnsServer                      : Microsoft.WindowsAzure.Management.StorSimple.Models.DnsServerSettings
InstanceId                     : f9db31da-8a6c-4718-8f5b-5ce89e600f28
Name                           : 
NetInterfaceList               : {Data0, Data1, Data2, Data3...} 
OperationInProgress            : None
RemoteMgmtSettingsInfo         : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteManagementSettings

RemoteMinishellSecretInfo      : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteMinishellSettings
SecretEncryptionCertThumbprint : 
Snapshot                       : Microsoft.WindowsAzure.Management.StorSimple.Models.SnapshotSettings
TimeServer                     : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeSettings
Type                           : Appliance
VirtualApplianceProperties     : Microsoft.WindowsAzure.Management.StorSimple.Models.VirtualApplianceInfo
WebProxy                       : Microsoft.WindowsAzure.Management.StorSimple.Models.WebProxySettings
```

<span data-ttu-id="babef-119">Bu komut, bir kaynaktaki belirtilen adı ve türü içeren kullanılabilir tüm cihazları alır.</span><span class="sxs-lookup"><span data-stu-id="babef-119">This command gets all available devices on a resource that have the specified name and type.</span></span>
<span data-ttu-id="babef-120">Bu komut, *ayrıntılı* parametreyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="babef-120">This command specifies the *Detailed* parameter.</span></span>
<span data-ttu-id="babef-121">Komut döndürdüğü aygıtlarla ilgili ek bilgiler sağlar.</span><span class="sxs-lookup"><span data-stu-id="babef-121">The command provides additional details about the devices it returns.</span></span>

## <span data-ttu-id="babef-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="babef-122">PARAMETERS</span></span>

### <span data-ttu-id="babef-123">-Ayrıntılı</span><span class="sxs-lookup"><span data-stu-id="babef-123">-Detailed</span></span>
<span data-ttu-id="babef-124">Bu cmdlet 'in aldığı cihazların cihaz ayrıntılarını döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="babef-124">Indicates that this cmdlet returns device details for the devices that it gets.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="babef-125">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="babef-125">-DeviceId</span></span>
<span data-ttu-id="babef-126">Alınacak aygıtın örnek KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="babef-126">Specifies the instance ID of the device to get.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: ID

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="babef-127">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="babef-127">-DeviceName</span></span>
<span data-ttu-id="babef-128">Alınacak StorSimple aygıtının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="babef-128">Specifies the name of the StorSimple device to get.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="babef-129">-ModelId</span><span class="sxs-lookup"><span data-stu-id="babef-129">-ModelID</span></span>
<span data-ttu-id="babef-130">Alınacak StorSimple aygıtlarının modelinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="babef-130">Specifies the ID of the model of StorSimple devices to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="babef-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="babef-131">-Profile</span></span>
<span data-ttu-id="babef-132">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="babef-132">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="babef-133">-Tür</span><span class="sxs-lookup"><span data-stu-id="babef-133">-Type</span></span>
<span data-ttu-id="babef-134">StorSimple aygıtının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="babef-134">Specifies the type of a StorSimple device.</span></span>
<span data-ttu-id="babef-135">Geçerli değerler: Gereç ve VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="babef-135">Valid values are: Appliance and VirtualAppliance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="babef-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="babef-136">CommonParameters</span></span>
<span data-ttu-id="babef-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="babef-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="babef-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="babef-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="babef-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="babef-139">INPUTS</span></span>

### <span data-ttu-id="babef-140">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="babef-140">None</span></span>

## <span data-ttu-id="babef-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="babef-141">OUTPUTS</span></span>

### <span data-ttu-id="babef-142">Liste \<DeviceDetails\> , IEnumerable\<DeviceInfo\></span><span class="sxs-lookup"><span data-stu-id="babef-142">List\<DeviceDetails\>, IEnumerable\<DeviceInfo\></span></span>
<span data-ttu-id="babef-143">Bu cmdlet, *ayrıntılı* parametreyi belirttiğinizde bir **liste \<DeviceDetails\>** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="babef-143">This cmdlet returns a **List\<DeviceDetails\>** object, if you specify the *Detailed* parameter.</span></span>
<span data-ttu-id="babef-144">Parametreyi belirtmezseniz, **IEnumerable \<DeviceInfo\>** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="babef-144">If you do not specify that parameter, it returns an **IEnumerable\<DeviceInfo\>** object.</span></span>

## <span data-ttu-id="babef-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="babef-145">NOTES</span></span>

## <span data-ttu-id="babef-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="babef-146">RELATED LINKS</span></span>

[<span data-ttu-id="babef-147">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="babef-147">Get-AzureStorSimpleResourceContext</span></span>](./Get-AzureStorSimpleResourceContext.md)

[<span data-ttu-id="babef-148">Select-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="babef-148">Select-AzureStorSimpleResource</span></span>](./Select-AzureStorSimpleResource.md)


