---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 44C5AF58-ADC1-4BC6-9771-3FD8F0480106
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/stop-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
ms.openlocfilehash: d219f49bd3fa4660048bdf5108ca660344e2bc48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595105"
---
# <span data-ttu-id="7bea7-101">Stop-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="7bea7-101">Stop-AzureRmBackupJob</span></span>

## <span data-ttu-id="7bea7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bea7-102">SYNOPSIS</span></span>
<span data-ttu-id="7bea7-103">Var olan yedekleme işini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="7bea7-103">Cancels an existing Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bea7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7bea7-104">SYNTAX</span></span>

### <span data-ttu-id="7bea7-105">Idfiltersset</span><span class="sxs-lookup"><span data-stu-id="7bea7-105">IdFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Vault <AzureRMBackupVault> -JobID <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7bea7-106">İş Filtreleriayarla</span><span class="sxs-lookup"><span data-stu-id="7bea7-106">JobFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bea7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7bea7-107">DESCRIPTION</span></span>
<span data-ttu-id="7bea7-108">**Stop-AzureRmBackupJob** cmdlet 'i mevcut bir Azure yedekleme işini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="7bea7-108">The **Stop-AzureRmBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="7bea7-109">Çok uzun süren ve diğer etkinlikleri engelleyen bir işi durdurmak için bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="7bea7-109">Use this parameter to stop a job that takes too long and blocks other activities.</span></span>

<span data-ttu-id="7bea7-110">Yalnızca aşağıdaki iş türlerini iptal edebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="7bea7-110">You can cancel only the following types of jobs:</span></span> 

- <span data-ttu-id="7bea7-111">Yedeğinin</span><span class="sxs-lookup"><span data-stu-id="7bea7-111">Backup</span></span>
- <span data-ttu-id="7bea7-112">Kurtarma</span><span class="sxs-lookup"><span data-stu-id="7bea7-112">Restore</span></span>

## <span data-ttu-id="7bea7-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7bea7-113">EXAMPLES</span></span>

### <span data-ttu-id="7bea7-114">Örnek 1: iş KIMLIĞI kullanarak yedekleme işini durdurma</span><span class="sxs-lookup"><span data-stu-id="7bea7-114">Example 1: Stop a backup job by using a job ID</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Job = Get-AzureRmBackupJob -Vault $Vault -Operation Backup
PS C:\> Stop-AzureRmBackupJob -Vault $Vault -JobID $Job.InstanceId
```

<span data-ttu-id="7bea7-115">İlk komut **Get-Azurermbackupkasa** cmdlet 'Ini kullanarak Vault03 adlı kasayı alır.</span><span class="sxs-lookup"><span data-stu-id="7bea7-115">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="7bea7-116">Komut bu nesneyi $Vault değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7bea7-116">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="7bea7-117">İkinci komut, **Get-AzureRmBackupJob** cmdlet 'ini kullanarak $Vault kasadan bir yedekleme işi alır.</span><span class="sxs-lookup"><span data-stu-id="7bea7-117">The second command gets a backup job from the vault in $Vault by using the **Get-AzureRmBackupJob** cmdlet.</span></span>
<span data-ttu-id="7bea7-118">Komut, işi $Job değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7bea7-118">The command stores the job in the $Job variable.</span></span>
<span data-ttu-id="7bea7-119">Bu örnekte, belirtilen kasada yalnızca bir yedekleme işlemi vardır.</span><span class="sxs-lookup"><span data-stu-id="7bea7-119">In this example, there is only one backup operation in the specified vault.</span></span>

<span data-ttu-id="7bea7-120">Son komutu belirtilen KIMLIĞE sahip işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="7bea7-120">The final command stops the job that has the specified ID.</span></span>

### <span data-ttu-id="7bea7-121">Örnek 2: tüm geri yükleme işlemlerini durdurma</span><span class="sxs-lookup"><span data-stu-id="7bea7-121">Example 2: Stop all Restore operations</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Operation Restore | Stop-AzureRmBackupJob
```

<span data-ttu-id="7bea7-122">Bu komut $Vault kasadaki tüm geri yükleme işlemlerini alır ve ardından bunları geçerli cmdlet 'e geçirerek ardışık düzen işlecini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7bea7-122">This command gets all the restore operations in the vault in $Vault, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7bea7-123">Geçerli cmdlet her işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="7bea7-123">The current cmdlet stops each job.</span></span>

## <span data-ttu-id="7bea7-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7bea7-124">PARAMETERS</span></span>

### <span data-ttu-id="7bea7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bea7-125">-DefaultProfile</span></span>
<span data-ttu-id="7bea7-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7bea7-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bea7-127">-Job</span><span class="sxs-lookup"><span data-stu-id="7bea7-127">-Job</span></span>
<span data-ttu-id="7bea7-128">Bu cmdlet 'in iptal olduğu bir iş belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bea7-128">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="7bea7-129">**Azurermbackupjob** nesnesi almak için Get-AzureRmBackupJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7bea7-129">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: AzureRMBackupJob
Parameter Sets: JobFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bea7-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="7bea7-130">-JobID</span></span>
<span data-ttu-id="7bea7-131">Bu cmdlet 'in iptal olduğu bir iş belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bea7-131">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="7bea7-132">**Azurermbackupjob** nesnesi almak için Get-AzureRmBackupJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7bea7-132">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bea7-133">-Kasa</span><span class="sxs-lookup"><span data-stu-id="7bea7-133">-Vault</span></span>
<span data-ttu-id="7bea7-134">Bu cmdlet 'in işi iptal ettiğinde yedek kasayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bea7-134">Specifies the Backup vault in which this cmdlet cancels a job.</span></span>
<span data-ttu-id="7bea7-135">**Azurermbackupkasa** nesnesi almak için Get-AzureRmBackupVault cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7bea7-135">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bea7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bea7-136">CommonParameters</span></span>
<span data-ttu-id="7bea7-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7bea7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bea7-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bea7-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bea7-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7bea7-139">INPUTS</span></span>

### <span data-ttu-id="7bea7-140">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="7bea7-140">AzureRmBackupJob</span></span>

## <span data-ttu-id="7bea7-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7bea7-141">OUTPUTS</span></span>

### <span data-ttu-id="7bea7-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7bea7-142">None</span></span>

## <span data-ttu-id="7bea7-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7bea7-143">NOTES</span></span>

## <span data-ttu-id="7bea7-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7bea7-144">RELATED LINKS</span></span>

[<span data-ttu-id="7bea7-145">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="7bea7-145">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="7bea7-146">Get-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="7bea7-146">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="7bea7-147">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="7bea7-147">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)


