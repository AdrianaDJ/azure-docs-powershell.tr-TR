---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
ms.openlocfilehash: 133a779a1227c74830fdae69b52db321a63a12e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587499"
---
# <span data-ttu-id="4f277-101">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="4f277-101">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>

## <span data-ttu-id="4f277-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f277-102">SYNOPSIS</span></span>
<span data-ttu-id="4f277-103">Yedekleme işinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="4f277-103">Gets details for a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f277-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f277-104">SYNTAX</span></span>

### <span data-ttu-id="4f277-105">JobFilterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4f277-105">JobFilterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-Job] <JobBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f277-106">Idfilterset</span><span class="sxs-lookup"><span data-stu-id="4f277-106">IdFilterSet</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-JobId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f277-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f277-107">DESCRIPTION</span></span>
<span data-ttu-id="4f277-108">**Get-AzureRmRecoveryServicesBackupJobDetails** cmdlet 'i belirtilen Iş Için Azure yedekleme iş ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="4f277-108">The **Get-AzureRmRecoveryServicesBackupJobDetails** cmdlet gets Azure Backup job details for a specified job.</span></span>

<span data-ttu-id="4f277-109">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4f277-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="4f277-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f277-110">EXAMPLES</span></span>

### <span data-ttu-id="4f277-111">Örnek 1: başarısız işler için yedekleme işi ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="4f277-111">Example 1: Get Backup job details for failed jobs</span></span>
```
PS C:\>$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzureRmRecoveryServicesBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="4f277-112">İlk komut kasada başarısız olan işlerin dizisini alır ve bunları $Jobs dizisinde depolar.</span><span class="sxs-lookup"><span data-stu-id="4f277-112">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>

<span data-ttu-id="4f277-113">İkinci komut $Jobs başarısız olan işlerin iş ayrıntılarını alır ve $JobDetails değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4f277-113">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>

<span data-ttu-id="4f277-114">Son komutu başarısız olan işlerin hata ayrıntılarını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="4f277-114">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="4f277-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f277-115">PARAMETERS</span></span>

### <span data-ttu-id="4f277-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f277-116">-DefaultProfile</span></span>
<span data-ttu-id="4f277-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4f277-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f277-118">-Job</span><span class="sxs-lookup"><span data-stu-id="4f277-118">-Job</span></span>
<span data-ttu-id="4f277-119">Alınacak işi belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f277-119">Specifies the job to get.</span></span>
<span data-ttu-id="4f277-120">**Backupjob** nesnesi edinmek için Get-AzureRmRecoveryServicesBackupJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4f277-120">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: JobBase
Parameter Sets: JobFilterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f277-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="4f277-121">-JobId</span></span>
<span data-ttu-id="4f277-122">Yedekleme işinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f277-122">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="4f277-123">ID, **Backupjob** nesnesinin InstanceId özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="4f277-123">The ID is the InstanceId property of a **BackupJob** object.</span></span>

```yaml
Type: String
Parameter Sets: IdFilterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f277-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f277-124">CommonParameters</span></span>
<span data-ttu-id="4f277-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f277-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f277-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f277-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f277-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f277-127">INPUTS</span></span>

### <span data-ttu-id="4f277-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4f277-128">None</span></span>
<span data-ttu-id="4f277-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="4f277-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4f277-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f277-130">OUTPUTS</span></span>

### <span data-ttu-id="4f277-131">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="4f277-131">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="4f277-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f277-132">NOTES</span></span>

## <span data-ttu-id="4f277-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f277-133">RELATED LINKS</span></span>

[<span data-ttu-id="4f277-134">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="4f277-134">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


