---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 44C5AF58-ADC1-4BC6-9771-3FD8F0480106
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
ms.openlocfilehash: d502596b8c5ddde576b5fd22ee31398b2c4e869a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594314"
---
# <span data-ttu-id="6c1bd-101">Stop-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="6c1bd-101">Stop-AzureRmBackupJob</span></span>

## <span data-ttu-id="6c1bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c1bd-102">SYNOPSIS</span></span>
<span data-ttu-id="6c1bd-103">Var olan yedekleme işini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="6c1bd-103">Cancels an existing Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c1bd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6c1bd-104">SYNTAX</span></span>

### <span data-ttu-id="6c1bd-105">Idfiltersset</span><span class="sxs-lookup"><span data-stu-id="6c1bd-105">IdFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Vault <AzureRMBackupVault> -JobID <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c1bd-106">İş Filtreleriayarla</span><span class="sxs-lookup"><span data-stu-id="6c1bd-106">JobFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c1bd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6c1bd-107">DESCRIPTION</span></span>
<span data-ttu-id="6c1bd-108">**Stop-AzureRmBackupJob** cmdlet 'i mevcut bir Azure yedekleme işini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="6c1bd-108">The **Stop-AzureRmBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="6c1bd-109">Çok uzun süren ve diğer etkinlikleri engelleyen bir işi durdurmak için bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="6c1bd-109">Use this parameter to stop a job that takes too long and blocks other activities.</span></span>

<span data-ttu-id="6c1bd-110">Yalnızca aşağıdaki iş türlerini iptal edebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="6c1bd-110">You can cancel only the following types of jobs:</span></span> 

- <span data-ttu-id="6c1bd-111">Yedeğinin</span><span class="sxs-lookup"><span data-stu-id="6c1bd-111">Backup</span></span>
- <span data-ttu-id="6c1bd-112">Kurtarma</span><span class="sxs-lookup"><span data-stu-id="6c1bd-112">Restore</span></span>

## <span data-ttu-id="6c1bd-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6c1bd-113">EXAMPLES</span></span>

### <span data-ttu-id="6c1bd-114">Örnek 1: iş KIMLIĞI kullanarak yedekleme işini durdurma</span><span class="sxs-lookup"><span data-stu-id="6c1bd-114">Example 1: Stop a backup job by using a job ID</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Job = Get-AzureRmBackupJob -Vault $Vault -Operation Backup
PS C:\> Stop-AzureRmBackupJob -Vault $Vault -JobID $Job.InstanceId
```

<span data-ttu-id="6c1bd-115">İlk komut **Get-Azurermbackupkasa** cmdlet 'Ini kullanarak Vault03 adlı kasayı alır.</span><span class="sxs-lookup"><span data-stu-id="6c1bd-115">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="6c1bd-116">Komut bu nesneyi $Vault değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6c1bd-116">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="6c1bd-117">İkinci komut, **Get-AzureRmBackupJob** cmdlet 'ini kullanarak $Vault kasadan bir yedekleme işi alır.</span><span class="sxs-lookup"><span data-stu-id="6c1bd-117">The second command gets a backup job from the vault in $Vault by using the **Get-AzureRmBackupJob** cmdlet.</span></span>
<span data-ttu-id="6c1bd-118">Komut, işi $Job değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6c1bd-118">The command stores the job in the $Job variable.</span></span>
<span data-ttu-id="6c1bd-119">Bu örnekte, belirtilen kasada yalnızca bir yedekleme işlemi vardır.</span><span class="sxs-lookup"><span data-stu-id="6c1bd-119">In this example, there is only one backup operation in the specified vault.</span></span>

<span data-ttu-id="6c1bd-120">Son komutu belirtilen KIMLIĞE sahip işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="6c1bd-120">The final command stops the job that has the specified ID.</span></span>

### <span data-ttu-id="6c1bd-121">Örnek 2: tüm geri yükleme işlemlerini durdurma</span><span class="sxs-lookup"><span data-stu-id="6c1bd-121">Example 2: Stop all Restore operations</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Operation Restore | Stop-AzureRmBackupJob
```

<span data-ttu-id="6c1bd-122">Bu komut $Vault kasadaki tüm geri yükleme işlemlerini alır ve ardından bunları geçerli cmdlet 'e geçirerek ardışık düzen işlecini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6c1bd-122">This command gets all the restore operations in the vault in $Vault, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6c1bd-123">Geçerli cmdlet her işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="6c1bd-123">The current cmdlet stops each job.</span></span>

## <span data-ttu-id="6c1bd-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6c1bd-124">PARAMETERS</span></span>

### <span data-ttu-id="6c1bd-125">-Job</span><span class="sxs-lookup"><span data-stu-id="6c1bd-125">-Job</span></span>
<span data-ttu-id="6c1bd-126">Bu cmdlet 'in iptal olduğu bir iş belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c1bd-126">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="6c1bd-127">**Azurermbackupjob** nesnesi almak için Get-AzureRmBackupJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6c1bd-127">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c1bd-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="6c1bd-128">-JobID</span></span>
<span data-ttu-id="6c1bd-129">Bu cmdlet 'in iptal olduğu bir iş belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c1bd-129">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="6c1bd-130">**Azurermbackupjob** nesnesi almak için Get-AzureRmBackupJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6c1bd-130">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c1bd-131">-Kasa</span><span class="sxs-lookup"><span data-stu-id="6c1bd-131">-Vault</span></span>
<span data-ttu-id="6c1bd-132">Bu cmdlet 'in işi iptal ettiğinde yedek kasayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c1bd-132">Specifies the Backup vault in which this cmdlet cancels a job.</span></span>
<span data-ttu-id="6c1bd-133">**Azurermbackupkasa** nesnesi almak için Get-AzureRmBackupVault cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6c1bd-133">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c1bd-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c1bd-134">-DefaultProfile</span></span>
<span data-ttu-id="6c1bd-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6c1bd-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c1bd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c1bd-136">CommonParameters</span></span>
<span data-ttu-id="6c1bd-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6c1bd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c1bd-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c1bd-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c1bd-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6c1bd-139">INPUTS</span></span>

### <span data-ttu-id="6c1bd-140">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="6c1bd-140">AzureRmBackupJob</span></span>

## <span data-ttu-id="6c1bd-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6c1bd-141">OUTPUTS</span></span>

### <span data-ttu-id="6c1bd-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6c1bd-142">None</span></span>

## <span data-ttu-id="6c1bd-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6c1bd-143">NOTES</span></span>

## <span data-ttu-id="6c1bd-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6c1bd-144">RELATED LINKS</span></span>

[<span data-ttu-id="6c1bd-145">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="6c1bd-145">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="6c1bd-146">Get-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="6c1bd-146">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="6c1bd-147">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="6c1bd-147">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)


