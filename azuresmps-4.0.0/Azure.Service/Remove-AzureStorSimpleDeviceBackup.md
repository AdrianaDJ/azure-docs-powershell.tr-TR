---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 47650E39-758C-4D3C-9653-B70576CA0979
online version: ''
schema: 2.0.0
ms.openlocfilehash: a93791e3184fcabacbf90caebcb2170746922b36
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106467"
---
# <span data-ttu-id="a0cfb-101">Remove-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="a0cfb-101">Remove-AzureStorSimpleDeviceBackup</span></span>

## <span data-ttu-id="a0cfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0cfb-102">SYNOPSIS</span></span>
<span data-ttu-id="a0cfb-103">Yedekleme nesnesini siler.</span><span class="sxs-lookup"><span data-stu-id="a0cfb-103">Deletes a backup object.</span></span>

## <span data-ttu-id="a0cfb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0cfb-104">SYNTAX</span></span>

### <span data-ttu-id="a0cfb-105">Identifybyıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a0cfb-105">IdentifyById (Default)</span></span>
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupId <String> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a0cfb-106">Identifybyobject</span><span class="sxs-lookup"><span data-stu-id="a0cfb-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -Backup <Backup> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a0cfb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0cfb-107">DESCRIPTION</span></span>
<span data-ttu-id="a0cfb-108">**Remove-AzureStorSimpleDeviceBackup** cmdlet 'i tek bir yedekleme nesnesini siler.</span><span class="sxs-lookup"><span data-stu-id="a0cfb-108">The **Remove-AzureStorSimpleDeviceBackup** cmdlet deletes a single backup object.</span></span>
<span data-ttu-id="a0cfb-109">Zaten silinmiş olan bir yedeği silmeye çalışırsanız, bu cmdlet hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="a0cfb-109">If you attempt to delete a backup that has already been deleted, this cmdlet returns an error.</span></span>

## <span data-ttu-id="a0cfb-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0cfb-110">EXAMPLES</span></span>

### <span data-ttu-id="a0cfb-111">Örnek 1: bir cihazın yedeklemesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="a0cfb-111">Example 1: Remove a backup for a device</span></span>
```
PS C:\>Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId "dcb5c991-0485-400f-8d0a-03a1341ee989" -Force
The remove job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 6c73aff2-f5a1-4b5e-
9a4e-857e128dc216 for tracking the job status
```

<span data-ttu-id="a0cfb-112">Bu komut, Contoso63-AppVm adlı cihaz için belirtilen KIMLIĞE sahip olan yedeği kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a0cfb-112">This command removes the backup that has the specified ID for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="a0cfb-113">Komut, **yedekleme** nesnesini kaldıran işlemi başlatır ve ardından bir **taskresponse** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="a0cfb-113">The command starts the operation that removes the **Backup** object, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="a0cfb-114">Görevin durumunu görmek için **Get-AzureStorSimpleTask** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a0cfb-114">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="a0cfb-115">Örnek 2: bir aygıtın KIMLIĞINI kullanarak ilk yedeklemeyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="a0cfb-115">Example 2: Remove the first backup for a device by using its ID</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
PS C:\> Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId $Backup[0].InstanceId -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 53a656c3-c082-4e1f-afb7-bff3db45c791
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f4411f38d07f68b88095682dbeedd9e9
```

<span data-ttu-id="a0cfb-116">İlk komut Contoso63-AppVm adlı cihaz için yedekleri alır ve $Backup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a0cfb-116">The first command gets the backups for the device named Contoso63-AppVm, and then stores them in the $Backup variable.</span></span>

<span data-ttu-id="a0cfb-117">İkinci komut, Contoso63-AppVm adlı cihazdan bir yedeği siler.</span><span class="sxs-lookup"><span data-stu-id="a0cfb-117">The second command deletes a backup from the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="a0cfb-118">Komut, $Backup dizisinin ilk öğesinin **InstanceId** özelliğine başvuruda bulunmak için standart nokta gösterimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a0cfb-118">The command uses standard dot notation to refer to the **InstanceId** property of the first element of the $Backup array.</span></span>
<span data-ttu-id="a0cfb-119">Bu komut, *waitforcomplete* parametresini belirtir ve bu nedenle, komut işlem tamamlanana kadar bekler ve ardından **taskstatusınfo** nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a0cfb-119">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="a0cfb-120">Örnek 3: ardışık düzeni kullanarak bir cihazın ilk yedeklemesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="a0cfb-120">Example 3: Remove the first backup for a device by using the pipeline</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -WaitForComplete
PS C:\> $Backup[0] | Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -Force -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 48059fd8-e355-4b91-9385-630d24f31df6
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e1753f3bf68e6e44ab719436b5111e41
```

<span data-ttu-id="a0cfb-121">İlk komut Contoso63-AppVm adlı cihaz için yedekleri alır ve $Backup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a0cfb-121">The first command gets the backups for the device named Contoso63-AppVm, and then stores them in the $Backup variable.</span></span>

<span data-ttu-id="a0cfb-122">İkinci komut $Backup dizisinde depolanan ilk nesneyi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="a0cfb-122">The second command passes the first object stored in the $Backup array to the current cmdlet.</span></span>
<span data-ttu-id="a0cfb-123">Bu cmdlet, Contoso63-AppVm adlı cihazdan bu yedeği siler.</span><span class="sxs-lookup"><span data-stu-id="a0cfb-123">That cmdlet deletes that backup from the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="a0cfb-124">Bu komut, *waitforcomplete* parametresini belirtir ve bu nedenle, komut işlem tamamlanana kadar bekler ve ardından **taskstatusınfo** nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a0cfb-124">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

## <span data-ttu-id="a0cfb-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0cfb-125">PARAMETERS</span></span>

### <span data-ttu-id="a0cfb-126">-Yedekleme</span><span class="sxs-lookup"><span data-stu-id="a0cfb-126">-Backup</span></span>
<span data-ttu-id="a0cfb-127">Silinecek **yedekleme** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0cfb-127">Specifies the **Backup** object to delete.</span></span>
<span data-ttu-id="a0cfb-128">**Yedekleme** nesnesi edinmek için **Get-AzureStorSimpleDeviceBackup** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a0cfb-128">To obtain a **Backup** object, use the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>

```yaml
Type: Backup
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0cfb-129">-BackupID</span><span class="sxs-lookup"><span data-stu-id="a0cfb-129">-BackupId</span></span>
<span data-ttu-id="a0cfb-130">Silinecek yedeğin örnek KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0cfb-130">Specifies the instance ID of a backup to delete.</span></span>

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

### <span data-ttu-id="a0cfb-131">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="a0cfb-131">-DeviceName</span></span>
<span data-ttu-id="a0cfb-132">Yedeklemenin silineceği StorSimple aygıtının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0cfb-132">Specifies the name of the StorSimple device on which to delete a backup.</span></span>

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

### <span data-ttu-id="a0cfb-133">-Force</span><span class="sxs-lookup"><span data-stu-id="a0cfb-133">-Force</span></span>
<span data-ttu-id="a0cfb-134">Bu cmdlet 'in sizden onay istemez olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0cfb-134">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="a0cfb-135">-Profil</span><span class="sxs-lookup"><span data-stu-id="a0cfb-135">-Profile</span></span>
<span data-ttu-id="a0cfb-136">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0cfb-136">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="a0cfb-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="a0cfb-137">-WaitForComplete</span></span>
<span data-ttu-id="a0cfb-138">Bu cmdlet 'in, denetimi Windows PowerShell konsoluna geri göndermeden önce tamamlamasını beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0cfb-138">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="a0cfb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0cfb-139">CommonParameters</span></span>
<span data-ttu-id="a0cfb-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0cfb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0cfb-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0cfb-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0cfb-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0cfb-142">INPUTS</span></span>

### <span data-ttu-id="a0cfb-143">Yedeğinin</span><span class="sxs-lookup"><span data-stu-id="a0cfb-143">Backup</span></span>

## <span data-ttu-id="a0cfb-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0cfb-144">OUTPUTS</span></span>

### <span data-ttu-id="a0cfb-145">Taskstatusınfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="a0cfb-145">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="a0cfb-146">Bu cmdlet, bu parametreyi belirtmezseniz, *Waitforcomplete* parametresini belirtirseniz **, bir** **taskresponse** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="a0cfb-146">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="a0cfb-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0cfb-147">NOTES</span></span>

## <span data-ttu-id="a0cfb-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0cfb-148">RELATED LINKS</span></span>

[<span data-ttu-id="a0cfb-149">Get-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="a0cfb-149">Get-AzureStorSimpleDeviceBackup</span></span>](./Get-AzureStorSimpleDeviceBackup.md)


