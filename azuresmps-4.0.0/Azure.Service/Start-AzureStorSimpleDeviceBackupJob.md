---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 76826524-480F-458E-A996-A9DBACB8BA9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4aa220334c75d3e6832698ec10fbad71896473d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106027"
---
# <span data-ttu-id="30d6b-101">Start-AzureStorSimpleDeviceBackupJob</span><span class="sxs-lookup"><span data-stu-id="30d6b-101">Start-AzureStorSimpleDeviceBackupJob</span></span>

## <span data-ttu-id="30d6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30d6b-102">SYNOPSIS</span></span>
<span data-ttu-id="30d6b-103">Var olan yedekleme ilkesinden yedek oluşturan yeni bir iş başlatır.</span><span class="sxs-lookup"><span data-stu-id="30d6b-103">Starts a new job that creates a backup from an existing backup policy.</span></span>

## <span data-ttu-id="30d6b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="30d6b-104">SYNTAX</span></span>

### <span data-ttu-id="30d6b-105">Boş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="30d6b-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceBackupJob -DeviceName <String> -BackupPolicyId <String> [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="30d6b-106">Yedek türü verildi</span><span class="sxs-lookup"><span data-stu-id="30d6b-106">BackupTypeGiven</span></span>
```
Start-AzureStorSimpleDeviceBackupJob -DeviceName <String> -BackupPolicyId <String> -BackupType <String>
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="30d6b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="30d6b-107">DESCRIPTION</span></span>
<span data-ttu-id="30d6b-108">**Start-AzureStorSimpleDeviceBackupJob** cmdlet 'ı StorSimple aygıtındaki mevcut bir yedekleme ilkesinden yedek oluşturan yeni bir iş başlatır.</span><span class="sxs-lookup"><span data-stu-id="30d6b-108">The **Start-AzureStorSimpleDeviceBackupJob** cmdlet starts a new job that creates a backup from an existing backup policy on a StorSimple device.</span></span>
<span data-ttu-id="30d6b-109">Varsayılan olarak, bu cmdlet yerel bir anlık görüntü yedeklemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="30d6b-109">By default, this cmdlet creates a local snapshot backup.</span></span>
<span data-ttu-id="30d6b-110">Bulut yedeği oluşturmak için, *backupType* parametresi Için cloudsnapshot değerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="30d6b-110">To create a cloud backup, specify a value of CloudSnapshot for the *BackupType* parameter.</span></span>

## <span data-ttu-id="30d6b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="30d6b-111">EXAMPLES</span></span>

### <span data-ttu-id="30d6b-112">Örnek 1: yerel anlık görüntü yedeklemesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="30d6b-112">Example 1: Create a local snapshot backup</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupJob -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f"
JobId                                                                StatusCode RequestId
-----                                                                ---------- ---------
fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08                                 Accepted   456cf6bafd427103b71c07145e26d35c

VERBOSE: Your backup operation has been submitted for processing. Use commandlet "Get-AzureStorSimpleJob -JobId
fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08" to track status.
```

<span data-ttu-id="30d6b-113">Bu komut, belirtilen ilke KIMLIĞI için yerel bir anlık görüntü yedeklemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="30d6b-113">This command creates a local snapshot backup for the specified policy ID.</span></span>
<span data-ttu-id="30d6b-114">Bu komut işi başlatır ve ardından bir **Taskresponse** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="30d6b-114">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="30d6b-115">İşin durumunu görmek için **Get-AzureStorSimpleTask** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="30d6b-115">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="30d6b-116">Örnek 2: bulut anlık görüntü yedeklemesi oluşturma ve bitirmeyi bekleme</span><span class="sxs-lookup"><span data-stu-id="30d6b-116">Example 2: Create a cloud snapshot backup and wait to finish</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupJob -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f" -BackupType CloudSnapshot -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f28ecf6cf75a7f128ca18e6ae14f9003
```

<span data-ttu-id="30d6b-117">Bu komut belirtilen ilke KIMLIĞI için bulut anlık görüntü yedeklemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="30d6b-117">This command creates a cloud snapshot backup for the specified policy ID.</span></span>
<span data-ttu-id="30d6b-118">Bu komut *Waitforcomplete* parametresini belirtir; böylece komut görevi tamamlar ve ardından iş Için bir **taskstatusınfo** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="30d6b-118">This command specifies the *WaitForComplete* parameter, so the command completes the task, and then returns a **TaskStatusInfo** object for the job.</span></span>

## <span data-ttu-id="30d6b-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="30d6b-119">PARAMETERS</span></span>

### <span data-ttu-id="30d6b-120">-Backuppolicyıd</span><span class="sxs-lookup"><span data-stu-id="30d6b-120">-BackupPolicyId</span></span>
<span data-ttu-id="30d6b-121">Yedekleme oluşturmak için kullanılacak yedekleme ilkesinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="30d6b-121">Specifies the ID of the backup policy to use to create the backup.</span></span>

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

### <span data-ttu-id="30d6b-122">-BackupType</span><span class="sxs-lookup"><span data-stu-id="30d6b-122">-BackupType</span></span>
<span data-ttu-id="30d6b-123">Yedekleme türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="30d6b-123">Specifies the backup type.</span></span>
<span data-ttu-id="30d6b-124">Geçerli değerler: LocalSnapshot ve CloudSnapshot.</span><span class="sxs-lookup"><span data-stu-id="30d6b-124">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

```yaml
Type: String
Parameter Sets: BackupTypeGiven
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d6b-125">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="30d6b-125">-DeviceName</span></span>
<span data-ttu-id="30d6b-126">Yedekleme işinin başlayacağı StorSimple aygıtının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="30d6b-126">Specifies the name of the StorSimple device on which to start the backup job.</span></span>

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

### <span data-ttu-id="30d6b-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="30d6b-127">-Profile</span></span>
<span data-ttu-id="30d6b-128">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="30d6b-128">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="30d6b-129">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="30d6b-129">-WaitForComplete</span></span>
<span data-ttu-id="30d6b-130">Bu cmdlet 'in, denetimi Windows PowerShell konsoluna geri göndermeden önce tamamlamasını beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="30d6b-130">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="30d6b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30d6b-131">CommonParameters</span></span>
<span data-ttu-id="30d6b-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="30d6b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30d6b-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30d6b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30d6b-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="30d6b-134">INPUTS</span></span>

### <span data-ttu-id="30d6b-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="30d6b-135">None</span></span>

## <span data-ttu-id="30d6b-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="30d6b-136">OUTPUTS</span></span>

### <span data-ttu-id="30d6b-137">Taskstatusınfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="30d6b-137">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="30d6b-138">*Waitforcomplete* parametresini belirtirseniz, bu cmdlet bir **taskstatusınfo** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="30d6b-138">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="30d6b-139">Bu parametreyi belirtmezseniz, bir **Taskresponse** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="30d6b-139">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="30d6b-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="30d6b-140">NOTES</span></span>

## <span data-ttu-id="30d6b-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="30d6b-141">RELATED LINKS</span></span>

[<span data-ttu-id="30d6b-142">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="30d6b-142">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="30d6b-143">Start-AzureStorSimpleDeviceBackupRestoreJob</span><span class="sxs-lookup"><span data-stu-id="30d6b-143">Start-AzureStorSimpleDeviceBackupRestoreJob</span></span>](./Start-AzureStorSimpleDeviceBackupRestoreJob.md)


