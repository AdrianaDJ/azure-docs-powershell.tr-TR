---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6187F603-5298-4854-94F3-0C38FCF3125F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
ms.openlocfilehash: f9f0808db919ad5d1d38b29daa720fb9b8a5baee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588291"
---
# <span data-ttu-id="60907-101">Get-AzureRmBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="60907-101">Get-AzureRmBackupJobDetails</span></span>

## <span data-ttu-id="60907-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60907-102">SYNOPSIS</span></span>
<span data-ttu-id="60907-103">Yedekleme işinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="60907-103">Gets the details of a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60907-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="60907-104">SYNTAX</span></span>

### <span data-ttu-id="60907-105">İş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="60907-105">JobsFiltersSet (Default)</span></span>
```
Get-AzureRmBackupJobDetails -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="60907-106">Idfiltersset</span><span class="sxs-lookup"><span data-stu-id="60907-106">IdFiltersSet</span></span>
```
Get-AzureRmBackupJobDetails -Vault <AzureRMBackupVault> -JobId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60907-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="60907-107">DESCRIPTION</span></span>
<span data-ttu-id="60907-108">**Get-AzureRmBackupJobDetails** cmdlet 'i, bir Azure yedekleme işinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="60907-108">The **Get-AzureRmBackupJobDetails** cmdlet gets the details of an Azure Backup job.</span></span>
<span data-ttu-id="60907-109">Başarısız olan bir iş hakkında bilgi toplamak için bu cmdlet 'i kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="60907-109">You can use this cmdlet to gather information about a job that fails.</span></span>

## <span data-ttu-id="60907-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="60907-110">EXAMPLES</span></span>

### <span data-ttu-id="60907-111">Örnek 1: başarısız işin ayrıntılarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="60907-111">Example 1: Display the details of a failed job</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Jobs = Get-AzureRmBackupJob -Vault $Vault -Status Failed
PS C:\> $JobDetails = Get-AzureRmBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
ErrorCode ErrorMessage                            Recommendations
--------- ------------                            ---------------
   400001 Command execution failed.               {Another operation is currently in p...
```

<span data-ttu-id="60907-112">İlk komut **Get-Azurermbackupkasa** cmdlet 'Ini kullanarak Vault03 adlı kasayı alır.</span><span class="sxs-lookup"><span data-stu-id="60907-112">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="60907-113">Komut bu nesneyi $Vault değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="60907-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="60907-114">İkinci komut $Vault kasadan başarısız işleri alır ve $Jobs dizi değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="60907-114">The second command gets failed jobs from the vault in $Vault, and then stores them in the $Jobs array variable.</span></span>

<span data-ttu-id="60907-115">Üçüncü iş, $Jobs değişkenindeki ilk işin ayrıntılarını alır ve $JobDetails değişkeninde bu ayrıntıları depolar.</span><span class="sxs-lookup"><span data-stu-id="60907-115">The third job gets details for the first job in the $Jobs variable, and then stores those details in the $JobDetails variable.</span></span>

<span data-ttu-id="60907-116">Final komutu, standart nokta söz dizimini kullanarak $JobDetails 'un **ErrorDetails** özelliğini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="60907-116">The final command displays the **ErrorDetails** property of $JobDetails by using standard dot syntax.</span></span>

### <span data-ttu-id="60907-117">Örnek 2: başarısız iş için önerilen eylemi görüntüleme</span><span class="sxs-lookup"><span data-stu-id="60907-117">Example 2: Display the recommended action for a failed job</span></span>
```
PS C:\>$JobDetails.ErrorDetails.Recommendations
Another operation is currently in progress on this item. Please wait until the previous operation is completed, and then retry.
```

<span data-ttu-id="60907-118">Bu komut, ilk örnekte oluşturulan $JobDetails değişkeninden önerilen eylemi görüntüler.</span><span class="sxs-lookup"><span data-stu-id="60907-118">This command displays the recommended action from the $JobDetails variable that was created in the first example.</span></span>

## <span data-ttu-id="60907-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="60907-119">PARAMETERS</span></span>

### <span data-ttu-id="60907-120">-Job</span><span class="sxs-lookup"><span data-stu-id="60907-120">-Job</span></span>
<span data-ttu-id="60907-121">Bu cmdlet 'in ayrıntıları aldığı işi belirtir.</span><span class="sxs-lookup"><span data-stu-id="60907-121">Specifies a job for which this cmdlet gets details.</span></span>
<span data-ttu-id="60907-122">**Azurermbackupjob** nesnesi almak için Get-AzureRmBackupJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="60907-122">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobsFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60907-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="60907-123">-JobId</span></span>
<span data-ttu-id="60907-124">Bu cmdlet 'in ayrıntıları aldığı iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="60907-124">Specifies the ID of a job for which this cmdlet gets details.</span></span>
<span data-ttu-id="60907-125">ID, **Azurermbackupjob** nesnesinin **InstanceId** özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="60907-125">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="60907-126">**Azurermbackupjob** nesnesi almak için Get-AzureRmBackupJob seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="60907-126">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

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

### <span data-ttu-id="60907-127">-Kasa</span><span class="sxs-lookup"><span data-stu-id="60907-127">-Vault</span></span>
<span data-ttu-id="60907-128">Bu cmdlet 'in iş ayrıntılarını aldığı yedek kasayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="60907-128">Specifies the Backup vault for which this cmdlet gets job details.</span></span>
<span data-ttu-id="60907-129">**Azurermbackupkasa** nesnesi almak için Get-AzureRmBackupVault cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="60907-129">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="60907-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60907-130">-DefaultProfile</span></span>
<span data-ttu-id="60907-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="60907-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60907-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60907-132">CommonParameters</span></span>
<span data-ttu-id="60907-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="60907-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60907-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60907-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60907-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="60907-135">INPUTS</span></span>

### <span data-ttu-id="60907-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="60907-136">None</span></span>

## <span data-ttu-id="60907-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="60907-137">OUTPUTS</span></span>

### <span data-ttu-id="60907-138">AzureRmBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="60907-138">AzureRmBackupJobDetails</span></span>

## <span data-ttu-id="60907-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="60907-139">NOTES</span></span>
* <span data-ttu-id="60907-140">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="60907-140">None</span></span>

## <span data-ttu-id="60907-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="60907-141">RELATED LINKS</span></span>

[<span data-ttu-id="60907-142">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="60907-142">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="60907-143">Get-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="60907-143">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


