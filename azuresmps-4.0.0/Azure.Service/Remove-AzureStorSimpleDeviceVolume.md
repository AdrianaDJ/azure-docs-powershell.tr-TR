---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A62D1A9D-C0EF-4305-B1F9-3AE68A79222D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a5023abffae6bbc2b70b7400e604ffabb1d24e6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106460"
---
# <span data-ttu-id="67248-101">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="67248-101">Remove-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="67248-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67248-102">SYNOPSIS</span></span>
<span data-ttu-id="67248-103">StorSimple aygıtından bir birimi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="67248-103">Removes a volume from a StorSimple device.</span></span>

## <span data-ttu-id="67248-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="67248-104">SYNTAX</span></span>

### <span data-ttu-id="67248-105">Identifybyname</span><span class="sxs-lookup"><span data-stu-id="67248-105">IdentifyByName</span></span>
```
Remove-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="67248-106">Identifybyobject</span><span class="sxs-lookup"><span data-stu-id="67248-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleDeviceVolume -DeviceName <String> -Volume <VirtualDisk> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="67248-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="67248-107">DESCRIPTION</span></span>
<span data-ttu-id="67248-108">**Remove-AzureStorSimpleDeviceVolume** cmdlet 'ı StorSimple aygıtından bir birimi çıkarır.</span><span class="sxs-lookup"><span data-stu-id="67248-108">The **Remove-AzureStorSimpleDeviceVolume** cmdlet removes a volume from a StorSimple device.</span></span>
<span data-ttu-id="67248-109">*Force* parametresini belirtmediğiniz sürece bu cmdlet onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="67248-109">This cmdlet prompts you for confirmation unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="67248-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="67248-110">EXAMPLES</span></span>

### <span data-ttu-id="67248-111">Örnek 1: ardışık düzeni kullanarak bir birimi kaldırma</span><span class="sxs-lookup"><span data-stu-id="67248-111">Example 1: Remove a volume by using the pipeline</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" | Remove-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm"
VERBOSE: ClientRequestId: 2933e24d-9564-42b5-9053-5f0bc4f59ea8_PS
VERBOSE: ClientRequestId: 7c2d854b-537a-4253-bb0c-c15bc8aa2b49_PS
VERBOSE: ClientRequestId: 4bf749ac-517c-49e7-8027-a8f62e272014_PS
VERBOSE: ClientRequestId: 7d9ec87a-616d-4ca9-bfb8-158859174d59_PS

Confirm
Are you sure you want to remove the volume? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 67a38e28-a015-44b1-8159-c1a6604f4d81_PS
VERBOSE: About to run a job to remove your volume! 
VERBOSE: ClientRequestId: 56101c10-07ca-40f4-8f19-c6fdd895e3a5_PS
32925451-4451-4478-89f7-d8930505d3fb
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
32925451-4451-4478-89f7-d8930505d3fb for tracking the task's status
VERBOSE: Volume with name: Volume18 is found.
```

<span data-ttu-id="67248-112">Bu komut, Contoso63-AppVm adlı cihazda Volume18 adındaki birimi alır ve bu birimi ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="67248-112">This command gets the volume named Volume18 on the device named Contoso63-AppVm, and then passes that volume to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="67248-113">Current cmdlet, birimi kaldıran ve bir **Taskresponse** nesnesini döndüren görevi başlatır.</span><span class="sxs-lookup"><span data-stu-id="67248-113">The current cmdlet starts the task that removes the volume, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="67248-114">Görevin durumunu görmek için **Get-AzureStorSimpleTask** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="67248-114">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>
<span data-ttu-id="67248-115">Komut *Force* parametresini belirtmezse, cmdlet sizden onay ister.</span><span class="sxs-lookup"><span data-stu-id="67248-115">The command does not specify the *Force* parameter, so the cmdlet prompts you for confirmation.</span></span>

### <span data-ttu-id="67248-116">Örnek 2: onaysız birimi silme</span><span class="sxs-lookup"><span data-stu-id="67248-116">Example 2: Remove a volume without confirmation</span></span>
```
PS C:\>Remove-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Force
VERBOSE: ClientRequestId: 72f13290-41eb-4ac4-9535-da1a42d0fa0b_PS
VERBOSE: ClientRequestId: ae0c1d99-1a66-4a69-9260-f2c8c12546bd_PS
VERBOSE: ClientRequestId: 9610744f-d031-488f-87e6-3ecddb305e13_PS
VERBOSE: About to run a job to remove your volume! 
VERBOSE: ClientRequestId: d33525d8-7276-4d2a-942d-d10f8078f1f7_PS
483f8cb4-ebc3-46a9-a9e6-0989e25738a0
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
483f8cb4-ebc3-46a9-a9e6-0989e25738a0 for tracking the task's status
```

<span data-ttu-id="67248-117">Bu komut, Volume18 adındaki birimi Contoso63-AppVm adlı cihazdan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="67248-117">This command removes the volume named Volume18 from the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="67248-118">Komut *Force* parametresini belirtir; böylece cmdlet sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="67248-118">The command specifies the *Force* parameter, so the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="67248-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="67248-119">PARAMETERS</span></span>

### <span data-ttu-id="67248-120">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="67248-120">-DeviceName</span></span>
<span data-ttu-id="67248-121">Kaldırılacak olan StorSimple aygıtının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="67248-121">Specifies the name of the StorSimple device on which to the volume to remove exists.</span></span>

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

### <span data-ttu-id="67248-122">-Force</span><span class="sxs-lookup"><span data-stu-id="67248-122">-Force</span></span>
<span data-ttu-id="67248-123">Bu cmdlet 'in sizden onay istemez olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="67248-123">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="67248-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="67248-124">-Profile</span></span>
<span data-ttu-id="67248-125">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="67248-125">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="67248-126">-Hacim</span><span class="sxs-lookup"><span data-stu-id="67248-126">-Volume</span></span>
<span data-ttu-id="67248-127">Bir **VirtualDisk** nesnesi olarak kaldırılacak birimi belirtir.</span><span class="sxs-lookup"><span data-stu-id="67248-127">Specifies the volume to remove, as a **VirtualDisk** object.</span></span>
<span data-ttu-id="67248-128">**VirtualDisk** nesnesi edinmek için **Get-AzureStorSimpleDeviceVolume** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="67248-128">To obtain a **VirtualDisk** object, use the **Get-AzureStorSimpleDeviceVolume** cmdlet.</span></span>

```yaml
Type: VirtualDisk
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67248-129">-BirimAdı</span><span class="sxs-lookup"><span data-stu-id="67248-129">-VolumeName</span></span>
<span data-ttu-id="67248-130">Kaldırılacak birimin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="67248-130">Specifies the name of the volume to remove.</span></span>

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

### <span data-ttu-id="67248-131">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="67248-131">-WaitForComplete</span></span>
<span data-ttu-id="67248-132">Bu cmdlet 'in, denetimi Windows PowerShell konsoluna geri göndermeden önce tamamlamasını beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="67248-132">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="67248-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67248-133">CommonParameters</span></span>
<span data-ttu-id="67248-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="67248-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67248-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67248-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67248-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="67248-136">INPUTS</span></span>

### <span data-ttu-id="67248-137">VirtualDisk</span><span class="sxs-lookup"><span data-stu-id="67248-137">VirtualDisk</span></span>
<span data-ttu-id="67248-138">Bu cmdlet, silinecek **VirtualDisk** nesnesini veya silinecek **VirtualDisk** birimini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="67248-138">This cmdlet accepts either the **VirtualDisk** object to delete or the volume name of the **VirtualDisk** to delete.</span></span>

## <span data-ttu-id="67248-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="67248-139">OUTPUTS</span></span>

### <span data-ttu-id="67248-140">Taskstatusınfo</span><span class="sxs-lookup"><span data-stu-id="67248-140">TaskStatusInfo</span></span>
<span data-ttu-id="67248-141">Bu cmdlet, *Waitforcomplete* parametresini belirtirseniz bir **taskstatusınfo** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="67248-141">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="67248-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="67248-142">NOTES</span></span>

## <span data-ttu-id="67248-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="67248-143">RELATED LINKS</span></span>

[<span data-ttu-id="67248-144">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="67248-144">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="67248-145">New-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="67248-145">New-AzureStorSimpleDeviceVolume</span></span>](./New-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="67248-146">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="67248-146">Set-AzureStorSimpleDeviceVolume</span></span>](./Set-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="67248-147">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="67248-147">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


