---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CE1C6576-234E-4891-9158-FA45B64B786C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41e8641b01dcb95a6b6939ff3551fe03b642ddf0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105435"
---
# <span data-ttu-id="cb0b9-101">Set-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="cb0b9-101">Set-AzureStorSimpleVirtualDevice</span></span>

## <span data-ttu-id="cb0b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb0b9-102">SYNOPSIS</span></span>
<span data-ttu-id="cb0b9-103">StorSimple Sanal aygıtının aygıt yapılandırmasını oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="cb0b9-103">Creates or updates the device configuration of a StorSimple virtual device.</span></span>

## <span data-ttu-id="cb0b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb0b9-104">SYNTAX</span></span>

```
Set-AzureStorSimpleVirtualDevice -DeviceName <String> -SecretKey <String> -AdministratorPassword <String>
 -SnapshotManagerPassword <String> [-TimeZone <TimeZoneInfo>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cb0b9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb0b9-105">DESCRIPTION</span></span>
<span data-ttu-id="cb0b9-106">**Set-AzureStorSimpleVirtualDevice** cmdlet 'ı bir Azure StorSimple Sanal aygıtının cihaz yapılandırmasını oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="cb0b9-106">The **Set-AzureStorSimpleVirtualDevice** cmdlet creates or updates the device configuration of an Azure StorSimple virtual device.</span></span>

## <span data-ttu-id="cb0b9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb0b9-107">EXAMPLES</span></span>

### <span data-ttu-id="cb0b9-108">Örnek 1: sanal cihazı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="cb0b9-108">Example 1: Update a virtual device</span></span>
```
PS C:\>$TimeZoneInfo = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }
PS C:\> Set-AzureStorSimpleVirtualDevice -DeviceName "Contoso23" -SecretKey "wcZBlBGpCMf4USdSKyt/SQ==" -TimeZone $TimeZoneInfo
VERBOSE: ClientRequestId: e31f0d6b-451d-4c1d-b2f1-3fc84c13972c_PS
VERBOSE: ClientRequestId: df58db83-d563-4a2e-bbb4-9576f0e69ca6_PS
VERBOSE: ClientRequestId: 494a9f0d-79ee-4fde-ab4d-85ee5a357556_PS
VERBOSE: ClientRequestId: ce557cbf-174d-4301-93d4-5ffe082c8413_PS
VERBOSE: ClientRequestId: 31284dad-de2c-4758-a2ef-45962875bfa6_PS
VERBOSE: About to configure the device : win-ff93i74m1e1 ! 
VERBOSE: ClientRequestId: d9c66302-45d8-488a-adda-8ccf957f77d3_PS


TaskId       : 21f530c3-bc47-4591-8c4e-da4d694b751d
TaskResult   : Succeeded
TaskStatus   : Completed
ErrorCode    : 
ErrorMessage : 
TaskSteps    : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: a94f972c-18ea-40b6-9401-2ad209c0c8b4_PS
AlertNotification              : Microsoft.WindowsAzure.Management.StorSimple.Models.AlertNotificationSettings
Chap                           : Microsoft.WindowsAzure.Management.StorSimple.Models.ChapSettings
DeviceProperties               : Microsoft.WindowsAzure.Management.StorSimple.Models.DeviceInfo
DnsServer                      : Microsoft.WindowsAzure.Management.StorSimple.Models.DnsServerSettings
InstanceId                     : d369ebb4-8b9a-47fc-9a6b-60f371e123ae
Name                           : 
NetInterfaceList               : {}
OperationInProgress            : None
RemoteMgmtSettingsInfo         : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteManagementSettings
RemoteMinishellSecretInfo      : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteMinishellSettings
SecretEncryptionCertThumbprint : 
Snapshot                       : Microsoft.WindowsAzure.Management.StorSimple.Models.SnapshotSettings
TimeServer                     : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeSettings
Type                           : VirtualAppliance
VirtualApplianceProperties     : Microsoft.WindowsAzure.Management.StorSimple.Models.VirtualApplianceInfo
WebProxy                       : Microsoft.WindowsAzure.Management.StorSimple.Models.WebProxySettings

VERBOSE: Successfully updated configuration for device Contoso23 with id d369ebb4-8b9a-47fc-9a6b-60f371e123ae
```

<span data-ttu-id="cb0b9-109">İlk komut, Pasifik standart saat dilimini almak için **System. TimeZoneInfo** .NET sınıfını ve standart söz dizimini kullanır ve bu nesneyi $TimeZoneInfo değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cb0b9-109">The first command uses the **System.TimeZoneInfo** .NET class and standard syntax to get Pacific Standard Time zone, and stores that object in the $TimeZoneInfo variable.</span></span>

<span data-ttu-id="cb0b9-110">İkinci komut, $TimeZoneInfo belirtilen saat dilimini kullanmak için Contoso23 adındaki cihazı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="cb0b9-110">The second command updates the device named Contoso23 to use the time zone specified in $TimeZoneInfo.</span></span>
<span data-ttu-id="cb0b9-111">Komut, sanal cihaz yapılandırmasına erişmek için gizli anahtar gerektirir.</span><span class="sxs-lookup"><span data-stu-id="cb0b9-111">The command requires the secret key to access the virtual device configuration.</span></span>

### <span data-ttu-id="cb0b9-112">Örnek 2: ardışık düzen işlecini kullanarak sanal cihazı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="cb0b9-112">Example 2: Update a virtual device by using the pipeline operator</span></span>
```
PS C:\> [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" } | Set-AzureStorSimpleVirtualDevice -DeviceName "Contoso23" -SecretKey "wcZBlBGpCMf4USdSKyt/SQ=="
```

<span data-ttu-id="cb0b9-113">Bu komut, Contoso23 adlı cihazı, komutun oluşturduğu saat dilimini kullanacak şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="cb0b9-113">This command updates the device named Contoso23 to use the time zone that the command creates.</span></span>
<span data-ttu-id="cb0b9-114">Komut, sanal cihaz yapılandırmasına erişmek için gizli anahtar gerektirir.</span><span class="sxs-lookup"><span data-stu-id="cb0b9-114">The command requires the secret key to access the virtual device configuration.</span></span>
<span data-ttu-id="cb0b9-115">Bu komut, önceki örnekle aynı şekilde çalışır, ancak zaman dilimini ardışık düzen işlecini kullanarak güncel cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="cb0b9-115">This command works the same way as the previous example, except that it passes the time zone to the current cmdlet by using the pipeline operator.</span></span>

## <span data-ttu-id="cb0b9-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb0b9-116">PARAMETERS</span></span>

### <span data-ttu-id="cb0b9-117">-\Administrators parolası</span><span class="sxs-lookup"><span data-stu-id="cb0b9-117">-AdministratorPassword</span></span>
<span data-ttu-id="cb0b9-118">Yapılandırılacak sanal cihazın yönetici parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb0b9-118">Specifies the administrator password of the virtual device to configure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb0b9-119">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="cb0b9-119">-DeviceName</span></span>
<span data-ttu-id="cb0b9-120">Yapılandırılacak sanal cihazın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb0b9-120">Specifies the name of the virtual device to configure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb0b9-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="cb0b9-121">-Profile</span></span>
<span data-ttu-id="cb0b9-122">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb0b9-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="cb0b9-123">-SecretKey</span><span class="sxs-lookup"><span data-stu-id="cb0b9-123">-SecretKey</span></span>
<span data-ttu-id="cb0b9-124">Sanal cihaz için bir hizmet şifreleme anahtarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb0b9-124">Specifies a service encryption key for the virtual device.</span></span>
<span data-ttu-id="cb0b9-125">Bu anahtar ilk fiziksel cihaz bir kaynakla kaydedildiğinde oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="cb0b9-125">This key is generated when the first physical device is registered with a resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb0b9-126">-SnapshotManagerPassword</span><span class="sxs-lookup"><span data-stu-id="cb0b9-126">-SnapshotManagerPassword</span></span>
<span data-ttu-id="cb0b9-127">Anlık görüntü yöneticisi parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb0b9-127">Specifies the snapshot manager password.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb0b9-128">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="cb0b9-128">-TimeZone</span></span>
<span data-ttu-id="cb0b9-129">Cihaz için bir saat dilimi belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb0b9-129">Specifies a time zone for the device.</span></span>
<span data-ttu-id="cb0b9-130">**Getsystemtimezone ()** yöntemini kullanarak bir **TimeZoneInfo** nesnesi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb0b9-130">You can create a **TimeZoneInfo** object by using the **GetSystemTimeZone()** method.</span></span>
<span data-ttu-id="cb0b9-131">Örneğin bu komut, Pasifik standart saati için saat dilimi bilgileri nesnesi oluşturur: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span><span class="sxs-lookup"><span data-stu-id="cb0b9-131">For example, this command creates a time zone information object for Pacific Standard Time: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span></span>

```yaml
Type: TimeZoneInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb0b9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb0b9-132">CommonParameters</span></span>
<span data-ttu-id="cb0b9-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb0b9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb0b9-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb0b9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb0b9-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb0b9-135">INPUTS</span></span>

### <span data-ttu-id="cb0b9-136">TimeZoneInfo</span><span class="sxs-lookup"><span data-stu-id="cb0b9-136">TimeZoneInfo</span></span>
<span data-ttu-id="cb0b9-137">Bir **TimeZoneInfo** nesnesini bu cmdlet 'e boru edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb0b9-137">You can pipe a **TimeZoneInfo** object to this cmdlet.</span></span>

## <span data-ttu-id="cb0b9-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb0b9-138">OUTPUTS</span></span>

### <span data-ttu-id="cb0b9-139">DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="cb0b9-139">DeviceJobDetails</span></span>
<span data-ttu-id="cb0b9-140">Bu cmdlet sanal cihazın güncelleştirilmiş cihaz ayrıntılarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="cb0b9-140">This cmdlet returns updated device details for the virtual device.</span></span>

## <span data-ttu-id="cb0b9-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb0b9-141">NOTES</span></span>

## <span data-ttu-id="cb0b9-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb0b9-142">RELATED LINKS</span></span>

[<span data-ttu-id="cb0b9-143">New-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="cb0b9-143">New-AzureStorSimpleVirtualDevice</span></span>](./New-AzureStorSimpleVirtualDevice.md)

[<span data-ttu-id="cb0b9-144">Set-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="cb0b9-144">Set-AzureStorSimpleDevice</span></span>](./Set-AzureStorSimpleDevice.md)


