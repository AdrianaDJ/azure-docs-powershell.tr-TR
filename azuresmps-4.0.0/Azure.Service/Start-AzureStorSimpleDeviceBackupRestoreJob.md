---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F9C8D0AA-ED97-43E8-ADB1-5AE1A4517666
online version: ''
schema: 2.0.0
ms.openlocfilehash: c524bb90d84df6ad3e37b552b957dac2d75b6a6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105747"
---
# <span data-ttu-id="e9090-101">Start-AzureStorSimpleDeviceBackupRestoreJob</span><span class="sxs-lookup"><span data-stu-id="e9090-101">Start-AzureStorSimpleDeviceBackupRestoreJob</span></span>

## <span data-ttu-id="e9090-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9090-102">SYNOPSIS</span></span>
<span data-ttu-id="e9090-103">StorSimple cihazında yedeklemeyi geri yükleyen bir iş başlatır.</span><span class="sxs-lookup"><span data-stu-id="e9090-103">Starts a job that restores a backup on a StorSimple device.</span></span>

## <span data-ttu-id="e9090-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9090-104">SYNTAX</span></span>

### <span data-ttu-id="e9090-105">Boş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e9090-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName <String> -BackupId <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e9090-106">Identifybyıd</span><span class="sxs-lookup"><span data-stu-id="e9090-106">IdentifyById</span></span>
```
Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName <String> -BackupId <String> -SnapshotId <String>
 [-WaitForComplete] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e9090-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9090-107">DESCRIPTION</span></span>
<span data-ttu-id="e9090-108">**Start-AzureStorSimpleDeviceBackupRestoreJob** cmdlet 'ı StorSimple cihazında yedeklemeyi geri yükleyen bir iş başlatır.</span><span class="sxs-lookup"><span data-stu-id="e9090-108">The **Start-AzureStorSimpleDeviceBackupRestoreJob** cmdlet starts a job that restores a backup on a StorSimple device.</span></span>
<span data-ttu-id="e9090-109">Yedekleme KIMLIĞI ve isteğe bağlı bir anlık görüntü KIMLIĞI belirtin.</span><span class="sxs-lookup"><span data-stu-id="e9090-109">Specify a backup ID and an optional snapshot ID.</span></span>

## <span data-ttu-id="e9090-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9090-110">EXAMPLES</span></span>

### <span data-ttu-id="e9090-111">Örnek 1: bir yedeklemeyi geri yüklemek için bir iş başlatın</span><span class="sxs-lookup"><span data-stu-id="e9090-111">Example 1: Start a job to restore a backup</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName "Contoso63-AppVm" -BackupId "b3b50534-763c-4b05-9724-5ecf62bde721" -WaitForComplete
Confirm
Are you sure you want to restore the backup with backupId b3b50534-763c-4b05-9724-5ecf62bde721? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y


Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 217d0647-c001-4f43-9833-f8155a458e95
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e0aa2dcd2f197a8588c40a067fe0e519
```

<span data-ttu-id="e9090-112">Bu komut, Contoso63-AppVm adlı aygıtta belirtilen KIMLIĞE ve ilişkili anlık görüntülere sahip yedekleme nesnesini geri yükleyen bir iş başlatır.</span><span class="sxs-lookup"><span data-stu-id="e9090-112">This command starts a job that restores the backup object that has the specified ID, and its associated snapshots, on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="e9090-113">Komut *Waitforcomplete* parametresini belirtir; böylece, cmdlet konsola denetimi göndermeden önce biter.</span><span class="sxs-lookup"><span data-stu-id="e9090-113">The command specifies the *WaitForComplete* parameter, so the job finishes before the cmdlet returns control to the console.</span></span>

### <span data-ttu-id="e9090-114">Örnek 2: belirli bir anlık görüntüyü geri yüklemek için bir iş başlatın</span><span class="sxs-lookup"><span data-stu-id="e9090-114">Example 2: Start a job to restore a specific snapshot</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName "Contoso63-AppVm" -BackupId "b3b50534-763c-4b05-9724-5ecf62bde721" -SnapshotId "2d0cfad7-46bf-4266-8859-96549646e947_0000000000000000" -Force

The start job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 9102ed9a-078f-4648-a
721-3cffbba31336 for tracking the job status
```

<span data-ttu-id="e9090-115">Bu komut, belirtilen KIMLIĞE sahip yedek anlık görüntüsünü geri yükleyen bir iş başlatır.</span><span class="sxs-lookup"><span data-stu-id="e9090-115">This command starts a job that restores the backup snapshot that has the specified ID.</span></span>
<span data-ttu-id="e9090-116">Komut, Contoso63-AppVm adlı cihazda KIMLIĞI belirtilen yedekleme nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9090-116">The command specifies the backup object by ID on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="e9090-117">Komut *Force* parametresini belirtir, bu nedenle işi onaylamanızı istemeden başlatır.</span><span class="sxs-lookup"><span data-stu-id="e9090-117">The command specifies the *Force* parameter, so it starts the job without prompting you to confirm.</span></span>

## <span data-ttu-id="e9090-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9090-118">PARAMETERS</span></span>

### <span data-ttu-id="e9090-119">-BackupID</span><span class="sxs-lookup"><span data-stu-id="e9090-119">-BackupId</span></span>
<span data-ttu-id="e9090-120">Geri yüklenecek yedeğin örnek KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9090-120">Specifies the instance ID of the backup to restore.</span></span>

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

### <span data-ttu-id="e9090-121">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="e9090-121">-DeviceName</span></span>
<span data-ttu-id="e9090-122">Yedeklemenin varolduğu StorSimple aygıtının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9090-122">Specifies the name of the StorSimple device on which the backup exists.</span></span>

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

### <span data-ttu-id="e9090-123">-Force</span><span class="sxs-lookup"><span data-stu-id="e9090-123">-Force</span></span>
<span data-ttu-id="e9090-124">Bu cmdlet 'in sizden onay istemez olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e9090-124">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="e9090-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="e9090-125">-Profile</span></span>
<span data-ttu-id="e9090-126">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9090-126">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="e9090-127">-Anlık anlık kimliği</span><span class="sxs-lookup"><span data-stu-id="e9090-127">-SnapshotId</span></span>
<span data-ttu-id="e9090-128">Geri yüklenecek anlık görüntünün örnek KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9090-128">Specifies the instance ID of the snapshot to restore.</span></span>

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

### <span data-ttu-id="e9090-129">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="e9090-129">-WaitForComplete</span></span>
<span data-ttu-id="e9090-130">Bu cmdlet 'in, denetimi Windows PowerShell konsoluna geri göndermeden önce tamamlamasını beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e9090-130">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="e9090-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9090-131">CommonParameters</span></span>
<span data-ttu-id="e9090-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9090-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9090-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9090-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9090-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9090-134">INPUTS</span></span>

### <span data-ttu-id="e9090-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e9090-135">None</span></span>

## <span data-ttu-id="e9090-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9090-136">OUTPUTS</span></span>

### <span data-ttu-id="e9090-137">Taskstatusınfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="e9090-137">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="e9090-138">*Waitforcomplete* parametresini belirtirseniz, bu cmdlet bir **taskstatusınfo** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="e9090-138">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="e9090-139">Bu parametreyi belirtmezseniz, bir **Taskresponse** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="e9090-139">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="e9090-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9090-140">NOTES</span></span>

## <span data-ttu-id="e9090-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9090-141">RELATED LINKS</span></span>

[<span data-ttu-id="e9090-142">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="e9090-142">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="e9090-143">Start-AzureStorSimpleDeviceBackupJob</span><span class="sxs-lookup"><span data-stu-id="e9090-143">Start-AzureStorSimpleDeviceBackupJob</span></span>](./Start-AzureStorSimpleDeviceBackupJob.md)


