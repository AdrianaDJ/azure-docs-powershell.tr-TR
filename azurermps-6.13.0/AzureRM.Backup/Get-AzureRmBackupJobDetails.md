---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6187F603-5298-4854-94F3-0C38FCF3125F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
ms.openlocfilehash: bf4ba77a7162faaf593e11b68a82fe5a6e55df1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762490"
---
# <span data-ttu-id="a5354-101">Get-AzureRmBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="a5354-101">Get-AzureRmBackupJobDetails</span></span>

## <span data-ttu-id="a5354-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5354-102">SYNOPSIS</span></span>
<span data-ttu-id="a5354-103">Yedekleme işinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="a5354-103">Gets the details of a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5354-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5354-104">SYNTAX</span></span>

### <span data-ttu-id="a5354-105">İş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a5354-105">JobsFiltersSet (Default)</span></span>
```
Get-AzureRmBackupJobDetails -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5354-106">Idfiltersset</span><span class="sxs-lookup"><span data-stu-id="a5354-106">IdFiltersSet</span></span>
```
Get-AzureRmBackupJobDetails -Vault <AzureRMBackupVault> -JobId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5354-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5354-107">DESCRIPTION</span></span>
<span data-ttu-id="a5354-108">**Get-AzureRmBackupJobDetails** cmdlet 'i, bir Azure yedekleme işinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="a5354-108">The **Get-AzureRmBackupJobDetails** cmdlet gets the details of an Azure Backup job.</span></span>
<span data-ttu-id="a5354-109">Başarısız olan bir iş hakkında bilgi toplamak için bu cmdlet 'i kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a5354-109">You can use this cmdlet to gather information about a job that fails.</span></span>

## <span data-ttu-id="a5354-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5354-110">EXAMPLES</span></span>

### <span data-ttu-id="a5354-111">Örnek 1: başarısız işin ayrıntılarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="a5354-111">Example 1: Display the details of a failed job</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Jobs = Get-AzureRmBackupJob -Vault $Vault -Status Failed
PS C:\> $JobDetails = Get-AzureRmBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
ErrorCode ErrorMessage                            Recommendations
--------- ------------                            ---------------
   400001 Command execution failed.               {Another operation is currently in p...
```

<span data-ttu-id="a5354-112">İlk komut **Get-Azurermbackupkasa** cmdlet 'Ini kullanarak Vault03 adlı kasayı alır.</span><span class="sxs-lookup"><span data-stu-id="a5354-112">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="a5354-113">Komut bu nesneyi $Vault değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a5354-113">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="a5354-114">İkinci komut $Vault kasadan başarısız işleri alır ve $Jobs dizi değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a5354-114">The second command gets failed jobs from the vault in $Vault, and then stores them in the $Jobs array variable.</span></span>
<span data-ttu-id="a5354-115">Üçüncü iş, $Jobs değişkenindeki ilk işin ayrıntılarını alır ve $JobDetails değişkeninde bu ayrıntıları depolar.</span><span class="sxs-lookup"><span data-stu-id="a5354-115">The third job gets details for the first job in the $Jobs variable, and then stores those details in the $JobDetails variable.</span></span>
<span data-ttu-id="a5354-116">Final komutu, standart nokta söz dizimini kullanarak $JobDetails 'un **ErrorDetails** özelliğini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="a5354-116">The final command displays the **ErrorDetails** property of $JobDetails by using standard dot syntax.</span></span>

### <span data-ttu-id="a5354-117">Örnek 2: başarısız iş için önerilen eylemi görüntüleme</span><span class="sxs-lookup"><span data-stu-id="a5354-117">Example 2: Display the recommended action for a failed job</span></span>
```
PS C:\>$JobDetails.ErrorDetails.Recommendations
Another operation is currently in progress on this item. Please wait until the previous operation is completed, and then retry.
```

<span data-ttu-id="a5354-118">Bu komut, ilk örnekte oluşturulan $JobDetails değişkeninden önerilen eylemi görüntüler.</span><span class="sxs-lookup"><span data-stu-id="a5354-118">This command displays the recommended action from the $JobDetails variable that was created in the first example.</span></span>

## <span data-ttu-id="a5354-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5354-119">PARAMETERS</span></span>

### <span data-ttu-id="a5354-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5354-120">-DefaultProfile</span></span>
<span data-ttu-id="a5354-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a5354-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5354-122">-Job</span><span class="sxs-lookup"><span data-stu-id="a5354-122">-Job</span></span>
<span data-ttu-id="a5354-123">Bu cmdlet 'in ayrıntıları aldığı işi belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5354-123">Specifies a job for which this cmdlet gets details.</span></span>
<span data-ttu-id="a5354-124">**Azurermbackupjob** nesnesi almak için Get-AzureRmBackupJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a5354-124">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="a5354-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="a5354-125">-JobId</span></span>
<span data-ttu-id="a5354-126">Bu cmdlet 'in ayrıntıları aldığı iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5354-126">Specifies the ID of a job for which this cmdlet gets details.</span></span>
<span data-ttu-id="a5354-127">ID, **Azurermbackupjob** nesnesinin **InstanceId** özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="a5354-127">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="a5354-128">**Azurermbackupjob** nesnesi almak için Get-AzureRmBackupJob seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a5354-128">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

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

### <span data-ttu-id="a5354-129">-Kasa</span><span class="sxs-lookup"><span data-stu-id="a5354-129">-Vault</span></span>
<span data-ttu-id="a5354-130">Bu cmdlet 'in iş ayrıntılarını aldığı yedek kasayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5354-130">Specifies the Backup vault for which this cmdlet gets job details.</span></span>
<span data-ttu-id="a5354-131">**Azurermbackupkasa** nesnesi almak için Get-AzureRmBackupVault cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a5354-131">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="a5354-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5354-132">CommonParameters</span></span>
<span data-ttu-id="a5354-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5354-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5354-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5354-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5354-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5354-135">INPUTS</span></span>

### <span data-ttu-id="a5354-136">Microsoft. Azure. Commands. AzureBackup. modeller. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="a5354-136">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>
<span data-ttu-id="a5354-137">Parametreler: Iş (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a5354-137">Parameters: Job (ByValue)</span></span>

## <span data-ttu-id="a5354-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5354-138">OUTPUTS</span></span>

### <span data-ttu-id="a5354-139">Microsoft. Azure. Commands. AzureBackup. modeller. AzureRMBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="a5354-139">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJobDetails</span></span>

## <span data-ttu-id="a5354-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5354-140">NOTES</span></span>

## <span data-ttu-id="a5354-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5354-141">RELATED LINKS</span></span>

[<span data-ttu-id="a5354-142">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="a5354-142">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="a5354-143">Get-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="a5354-143">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


