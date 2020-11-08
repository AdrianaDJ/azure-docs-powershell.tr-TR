---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 53580FF1-D905-40FD-A5F0-D5FBCD036E0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a51fd8210d2fe7fb224ed43650a354e383ed4e54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105776"
---
# <span data-ttu-id="171d7-101">Start-AzureStorSimpleDeviceFailoverJob</span><span class="sxs-lookup"><span data-stu-id="171d7-101">Start-AzureStorSimpleDeviceFailoverJob</span></span>

## <span data-ttu-id="171d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="171d7-102">SYNOPSIS</span></span>
<span data-ttu-id="171d7-103">Birim kapsayıcı gruplarının bir yük devretme işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="171d7-103">Initiates a failover operation of volume container groups.</span></span>

## <span data-ttu-id="171d7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="171d7-104">SYNTAX</span></span>

### <span data-ttu-id="171d7-105">Boş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="171d7-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="171d7-106">Identifybyıd</span><span class="sxs-lookup"><span data-stu-id="171d7-106">IdentifyById</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceId <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="171d7-107">Identifybyname</span><span class="sxs-lookup"><span data-stu-id="171d7-107">IdentifyByName</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceName <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceName <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="171d7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="171d7-108">DESCRIPTION</span></span>
<span data-ttu-id="171d7-109">**Start-AzureStorSimpleDeviceFailoverJob** cmdlet 'i bir cihazdan diğerine bir veya daha fazla birim kapsayıcı grubundan bir yük devretme işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="171d7-109">The **Start-AzureStorSimpleDeviceFailoverJob** cmdlet initiates a failover operation of one or more volume container groups from one device to another.</span></span>

## <span data-ttu-id="171d7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="171d7-110">EXAMPLES</span></span>

### <span data-ttu-id="171d7-111">Örnek 1: adlandırılmış bir cihaz ve adlandırılmış hedef cihaz için bir yük devretme işi başlatma</span><span class="sxs-lookup"><span data-stu-id="171d7-111">Example 1: Start a failover job for a named device and named target device</span></span>
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Start-AzureStorSimpleDeviceFailoverJob -DeviceName "ChewD_App7" -TargetDeviceName "Fuller05" -Force
a3d902be-8ffb-42a4-bbf8-0a1b30db71b2_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

<span data-ttu-id="171d7-112">Bu komut, **Get-AzureStorSimpleFailoverVolumeContainers** cmdlet 'ini kullanarak ChewD_App7 adlı cihazın yük devretme birimi kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="171d7-112">This command gets the failover volume containers for the device named ChewD_App7 by using the **Get-AzureStorSimpleFailoverVolumeContainers** cmdlet.</span></span>
<span data-ttu-id="171d7-113">Bu komut sonuçları, **ısdcgroupeligiblefordr** özelliği için $true dışında bir değer içeren kapsayıcıları geçen **nesne** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="171d7-113">The command passes the results to the **Where-Object** cmdlet, which drops those containers that have a value other than $True for the **IsDCGroupEligibleForDR** property.</span></span>
<span data-ttu-id="171d7-114">Daha fazla bilgi için yazın `Get-Help Where-Object` .</span><span class="sxs-lookup"><span data-stu-id="171d7-114">For more information, type `Get-Help Where-Object`.</span></span>
<span data-ttu-id="171d7-115">Geçerli cmdlet kalan çalışma bölümü kapsayıcılarının yük devretme işlerini başlatır.</span><span class="sxs-lookup"><span data-stu-id="171d7-115">The current cmdlet starts failover jobs for the remaining failover volume containers.</span></span>
<span data-ttu-id="171d7-116">Komut, cihaz adını ve hedef cihaz adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="171d7-116">The command specifies the device name and target device name.</span></span>
<span data-ttu-id="171d7-117">Komut, cmdlet 'in başladığı işin örnek KIMLIĞINI döndürür.</span><span class="sxs-lookup"><span data-stu-id="171d7-117">The command returns the instance ID of the job that the cmdlet starts.</span></span>

### <span data-ttu-id="171d7-118">Örnek 2: KIMLIĞI belirtilen bir cihaz ve hedef cihaz için bir yük devretme işi başlatma</span><span class="sxs-lookup"><span data-stu-id="171d7-118">Example 2: Start a failover job for a device and target device specified by ID</span></span>
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Select-Object -First 1 | Start-AzureStorSimpleDeviceFailoverJob -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925" -TargetDeviceId "0ee59ae9-0293-46e2-ae56-bc308c8e5520" -Force
4c5ac0d0-4b66-465c-98f5-aec90505ad12_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

<span data-ttu-id="171d7-119">Bu komut, **Get-AzureStorSimpleFailoverVolumeContainers** kullanarak ChewD_App7 adlı cihaz için yük devretme birimi kapsayıcılarını alır.</span><span class="sxs-lookup"><span data-stu-id="171d7-119">This command gets the failover volume containers for the device named ChewD_App7 by using **Get-AzureStorSimpleFailoverVolumeContainers**.</span></span>
<span data-ttu-id="171d7-120">Bu komut sonuçları, **ısdcgroupeligiblefordr** özelliği için $true dışında bir değer içeren bu Containters geçen **nesneye** geçirir.</span><span class="sxs-lookup"><span data-stu-id="171d7-120">The command passes the results to **Where-Object** , which drops those containters that have a value other than $True for the **IsDCGroupEligibleForDR** property.</span></span>
<span data-ttu-id="171d7-121">Cmdlet sonuçları geçerli cmdlet 'e geçilecek ilk nesneyi seçen **seçme-nesne** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="171d7-121">The cmdlet passes the results to the **Select-Object** cmdlet, which selects the first object to pass to the current cmdlet.</span></span>
<span data-ttu-id="171d7-122">Daha fazla bilgi için yazın `Get-Help Select-Object` .</span><span class="sxs-lookup"><span data-stu-id="171d7-122">For more information, type `Get-Help Select-Object`.</span></span>
<span data-ttu-id="171d7-123">Geçerli cmdlet, seçili yük devretme birimi kapsayıcısının yük devretme işlerini başlatır.</span><span class="sxs-lookup"><span data-stu-id="171d7-123">The current cmdlet starts failover jobs for the selected failover volume container.</span></span>
<span data-ttu-id="171d7-124">Komut, cihaz KIMLIĞINI ve hedef cihaz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="171d7-124">The command specifies the device ID and target device ID.</span></span>
<span data-ttu-id="171d7-125">Komut, cmdlet 'in başladığı işin örnek KIMLIĞINI döndürür.</span><span class="sxs-lookup"><span data-stu-id="171d7-125">The command returns the instance ID of the job that the cmdlet starts.</span></span>

## <span data-ttu-id="171d7-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="171d7-126">PARAMETERS</span></span>

### <span data-ttu-id="171d7-127">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="171d7-127">-DeviceId</span></span>
<span data-ttu-id="171d7-128">Birim kapsayıcı gruplarının var olduğu StorSimple aygıtının örnek KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="171d7-128">Specifies the instance ID of the StorSimple device on which the volume container groups exist.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="171d7-129">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="171d7-129">-DeviceName</span></span>
<span data-ttu-id="171d7-130">Birim kapsayıcı gruplarının var olduğu StorSimple aygıtının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="171d7-130">Specifies the name of the StorSimple device on which the volume container groups exist.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="171d7-131">-Force</span><span class="sxs-lookup"><span data-stu-id="171d7-131">-Force</span></span>
<span data-ttu-id="171d7-132">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="171d7-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="171d7-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="171d7-133">-Profile</span></span>
<span data-ttu-id="171d7-134">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="171d7-134">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="171d7-135">-Targetdeviceıd</span><span class="sxs-lookup"><span data-stu-id="171d7-135">-TargetDeviceId</span></span>
<span data-ttu-id="171d7-136">Bu cmdlet 'in birim kapsayıcı grupları üzerinde başarısız olduğu StorSimple aygıtının örnek KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="171d7-136">Specifies the instance ID of the StorSimple device to which this cmdlet fails over the volume container groups.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="171d7-137">-Targetaygıtadı</span><span class="sxs-lookup"><span data-stu-id="171d7-137">-TargetDeviceName</span></span>
<span data-ttu-id="171d7-138">Bu cmdlet 'in birim kapsayıcı grupları üzerinde başarısız olduğu StorSimple aygıtının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="171d7-138">Specifies the name of the StorSimple device to which this cmdlet fails over the volume container groups.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="171d7-139">-Birimcontainergroups</span><span class="sxs-lookup"><span data-stu-id="171d7-139">-VolumecontainerGroups</span></span>
<span data-ttu-id="171d7-140">Başka bir cihaza bu cmdlet 'in başarısız olduğu birim kapsayıcı gruplarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="171d7-140">Specifies the list of volume container groups that this cmdlet fails over to another device.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="171d7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="171d7-141">CommonParameters</span></span>
<span data-ttu-id="171d7-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="171d7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="171d7-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="171d7-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="171d7-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="171d7-144">INPUTS</span></span>

### <span data-ttu-id="171d7-145">Listeniz\<DataContainerGroup\></span><span class="sxs-lookup"><span data-stu-id="171d7-145">List\<DataContainerGroup\></span></span>
<span data-ttu-id="171d7-146">Birim kapsayıcı gruplarının listesini bu cmdlet 'e boru edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="171d7-146">You can pipe a list of volume container groups to this cmdlet.</span></span>

## <span data-ttu-id="171d7-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="171d7-147">OUTPUTS</span></span>

### <span data-ttu-id="171d7-148">Dizisi</span><span class="sxs-lookup"><span data-stu-id="171d7-148">String</span></span>

## <span data-ttu-id="171d7-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="171d7-149">NOTES</span></span>

## <span data-ttu-id="171d7-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="171d7-150">RELATED LINKS</span></span>

[<span data-ttu-id="171d7-151">Get-AzureStorSimpleFailoverVolumeContainers</span><span class="sxs-lookup"><span data-stu-id="171d7-151">Get-AzureStorSimpleFailoverVolumeContainers</span></span>](./Get-AzureStorSimpleFailoverVolumeContainers.md)


