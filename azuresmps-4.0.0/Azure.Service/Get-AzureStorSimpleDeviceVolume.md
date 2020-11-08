---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 79EE846E-D5BE-4808-BC6F-E3B16A308AB0
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9d0cd7ef0eacc7ff3e38c4619b60a0bd61f24f1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105566"
---
# <span data-ttu-id="20f72-101">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="20f72-101">Get-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="20f72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20f72-102">SYNOPSIS</span></span>
<span data-ttu-id="20f72-103">Aygıttaki birimleri alır.</span><span class="sxs-lookup"><span data-stu-id="20f72-103">Gets volumes on a device.</span></span>

## <span data-ttu-id="20f72-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="20f72-104">SYNTAX</span></span>

### <span data-ttu-id="20f72-105">Identifybyparentobject</span><span class="sxs-lookup"><span data-stu-id="20f72-105">IdentifyByParentObject</span></span>
```
Get-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeContainer <DataContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="20f72-106">Identifybyname</span><span class="sxs-lookup"><span data-stu-id="20f72-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="20f72-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="20f72-107">DESCRIPTION</span></span>
<span data-ttu-id="20f72-108">**Get-AzureStorSimpleDeviceVolume** cmdlet 'i belirtilen bir birim kapsayıcısının veya belirtilen ada sahip birimdeki birimlerin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="20f72-108">The **Get-AzureStorSimpleDeviceVolume** cmdlet gets a list of volumes for a specified volume container, or volume that has the specified name.</span></span>
<span data-ttu-id="20f72-109">Döndürülen nesne aşağıdaki özellikleri içerir:</span><span class="sxs-lookup"><span data-stu-id="20f72-109">The returned object contains the following properties:</span></span> 

- <span data-ttu-id="20f72-110">**AccessType**</span><span class="sxs-lookup"><span data-stu-id="20f72-110">**AccessType**</span></span>
- <span data-ttu-id="20f72-111">**AcrList**</span><span class="sxs-lookup"><span data-stu-id="20f72-111">**AcrList**</span></span>
- <span data-ttu-id="20f72-112">**AppType**</span><span class="sxs-lookup"><span data-stu-id="20f72-112">**AppType**</span></span>
- <span data-ttu-id="20f72-113">**Veri kapsayıcısı**</span><span class="sxs-lookup"><span data-stu-id="20f72-113">**DataContainer**</span></span>
- <span data-ttu-id="20f72-114">**Veri Containerıd**</span><span class="sxs-lookup"><span data-stu-id="20f72-114">**DataContainerId**</span></span>
- <span data-ttu-id="20f72-115">**Örnek**</span><span class="sxs-lookup"><span data-stu-id="20f72-115">**InstanceId**</span></span>
- <span data-ttu-id="20f72-116">**Isbackupenabled**</span><span class="sxs-lookup"><span data-stu-id="20f72-116">**IsBackupEnabled**</span></span>
- <span data-ttu-id="20f72-117">**Isadefaultbackupenabled**</span><span class="sxs-lookup"><span data-stu-id="20f72-117">**IsDefaultBackupEnabled**</span></span>
- <span data-ttu-id="20f72-118">**Ismonitoringenabled**</span><span class="sxs-lookup"><span data-stu-id="20f72-118">**IsMonitoringEnabled**</span></span>
- <span data-ttu-id="20f72-119">**Adlandır**</span><span class="sxs-lookup"><span data-stu-id="20f72-119">**Name**</span></span>
- <span data-ttu-id="20f72-120">**Medya**</span><span class="sxs-lookup"><span data-stu-id="20f72-120">**Online**</span></span>
- <span data-ttu-id="20f72-121">**Operationınprogress**</span><span class="sxs-lookup"><span data-stu-id="20f72-121">**OperationInProgress**</span></span>
- <span data-ttu-id="20f72-122">**SizeInBytes**</span><span class="sxs-lookup"><span data-stu-id="20f72-122">**SizeInBytes**</span></span>
- <span data-ttu-id="20f72-123">**VSN**</span><span class="sxs-lookup"><span data-stu-id="20f72-123">**VSN**</span></span>

## <span data-ttu-id="20f72-124">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="20f72-124">EXAMPLES</span></span>

### <span data-ttu-id="20f72-125">Örnek 1: belirtilen kapsayıcıdaki birimleri alma</span><span class="sxs-lookup"><span data-stu-id="20f72-125">Example 1: Get volumes in a specified container</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container03" | Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm"
InstanceId             : BA-1503262017214433280-ade42af6-dabb-449d-b66b-4f5d06891d4c
Name                   : Volume 1 Clone
Online                 : True
SizeInBytes            : 3298534883328
AccessType             : ReadWrite
AcrList                : {Windows_XYUSFL718-RV_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : BA-1503262017214433280-ade42af6-dabb-449d-b66b-4f5d06891d4c

InstanceId             : BA-1503262017366008684-cf8bb1a3-21e5-4cfc-ba0d-bfe238d77ebe
Name                   : Volume 3 Clone
Online                 : True
SizeInBytes            : 1717986918400
AccessType             : ReadWrite
AcrList                : {Linux_XYUSFL719_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : BA-1503262017366008684-cf8bb1a3-21e5-4cfc-ba0d-bfe238d77ebe

InstanceId             : SS-VOL-2180be94-36f1-473e-a42b-a3ebd2cdb481
Name                   : Volume 4
Online                 : True
SizeInBytes            : 1610612736000
AccessType             : ReadWrite
AcrList                : {Linux_XYUSFL719_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : SS-VOL-2180be94-36f1-473e-a42b-a3ebd2cdb481
```

<span data-ttu-id="20f72-126">Bu komut, **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet 'ini kullanarak Contoso63-AppVm adlı cihazda Container03 adındaki birim kapsayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="20f72-126">This command gets the volume container named Container03 on the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="20f72-127">Bu komut, bu kapsayıcıyı geçerli cmdlet 'e geçirmek için ardışık düzen işlecini kullanır.</span><span class="sxs-lookup"><span data-stu-id="20f72-127">The command uses the pipeline operator to pass that container to the current cmdlet.</span></span>
<span data-ttu-id="20f72-128">Bu cmdlet, Contoso63-AppVm adlı aygıtta bu kapsayıcıdaki tüm birimleri alır.</span><span class="sxs-lookup"><span data-stu-id="20f72-128">That cmdlet gets all the volumes in that container for the device named Contoso63-AppVm.</span></span>

### <span data-ttu-id="20f72-129">Örnek 2: adını kullanarak bir birimi alma</span><span class="sxs-lookup"><span data-stu-id="20f72-129">Example 2: Get a volume by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18"
InstanceId             : SS-VOL-c75e9636-1dcf-43db-92df-3af1ecf3f18a
Name                   : Volume18
Online                 : True
SizeInBytes            : 2748779069440
AccessType             : ReadWrite
AcrList                : {Windows_XYUSFL718-RV_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : SS-VOL-c75e9636-1dcf-43db-92df-3af1ecf3f18a
```

<span data-ttu-id="20f72-130">Bu komut, Contoso63-AppVm adındaki cihazda Volume18 adındaki birimi alır.</span><span class="sxs-lookup"><span data-stu-id="20f72-130">This command gets the volume named Volume18 on the device named Contoso63-AppVm.</span></span>

## <span data-ttu-id="20f72-131">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="20f72-131">PARAMETERS</span></span>

### <span data-ttu-id="20f72-132">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="20f72-132">-DeviceName</span></span>
<span data-ttu-id="20f72-133">Birimlerin alınacağı StorSimple aygıtının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="20f72-133">Specifies the name of the StorSimple device from which to get volumes.</span></span>

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

### <span data-ttu-id="20f72-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="20f72-134">-Profile</span></span>
<span data-ttu-id="20f72-135">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="20f72-135">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="20f72-136">-Birimkapsayıcısı</span><span class="sxs-lookup"><span data-stu-id="20f72-136">-VolumeContainer</span></span>
<span data-ttu-id="20f72-137">Alınacak birimleri içeren bir **datacontainer** nesnesi olarak birim kapsayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="20f72-137">Specifies the volume container, as a **DataContainer** object, that includes the volumes to get.</span></span>
<span data-ttu-id="20f72-138">**Datacontainer** almak için **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="20f72-138">To obtain a **DataContainer** , use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: IdentifyByParentObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20f72-139">-BirimAdı</span><span class="sxs-lookup"><span data-stu-id="20f72-139">-VolumeName</span></span>
<span data-ttu-id="20f72-140">Alınacak birimin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="20f72-140">Specifies the name of the volume to get.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20f72-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20f72-141">CommonParameters</span></span>
<span data-ttu-id="20f72-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="20f72-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20f72-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20f72-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20f72-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="20f72-144">INPUTS</span></span>

### <span data-ttu-id="20f72-145">Veri kapsayıcısı</span><span class="sxs-lookup"><span data-stu-id="20f72-145">DataContainer</span></span>
<span data-ttu-id="20f72-146">Bu cmdlet, alınacak birimi içeren bir **Datacontainer** nesnesini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="20f72-146">This cmdlet accepts a **DataContainer** object that contains the volume to get.</span></span>

## <span data-ttu-id="20f72-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="20f72-147">OUTPUTS</span></span>

### <span data-ttu-id="20f72-148">VirtualDisk, IList\<VirtualDisk\></span><span class="sxs-lookup"><span data-stu-id="20f72-148">VirtualDisk, IList\<VirtualDisk\></span></span>
<span data-ttu-id="20f72-149">Bu cmdlet, *BirimAdı* parametresini belirttiğinizde bir **VirtualDisk** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="20f72-149">This cmdlet returns a **VirtualDisk** object if you specify the *VolumeName* parameter.</span></span>
<span data-ttu-id="20f72-150">*Birimkapsayıcısı* belirtirseniz, bu cmdlet bir **IList \<VirtualDisk\>** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="20f72-150">If you specify the *VolumeContainer* , this cmdlet returns an **IList\<VirtualDisk\>** object.</span></span>

## <span data-ttu-id="20f72-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="20f72-151">NOTES</span></span>

## <span data-ttu-id="20f72-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="20f72-152">RELATED LINKS</span></span>

[<span data-ttu-id="20f72-153">New-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="20f72-153">New-AzureStorSimpleDeviceVolume</span></span>](./New-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="20f72-154">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="20f72-154">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="20f72-155">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="20f72-155">Set-AzureStorSimpleDeviceVolume</span></span>](./Set-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="20f72-156">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="20f72-156">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)


