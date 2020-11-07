---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
ms.openlocfilehash: 91658fc0772dfa2752d7f12f93efc62d57330891
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763337"
---
# <span data-ttu-id="fb7b2-101">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="fb7b2-101">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>

## <span data-ttu-id="fb7b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb7b2-102">SYNOPSIS</span></span>
<span data-ttu-id="fb7b2-103">Yedekleme işinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="fb7b2-103">Gets details for a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb7b2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb7b2-104">SYNTAX</span></span>

### <span data-ttu-id="fb7b2-105">JobFilterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fb7b2-105">JobFilterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-Job] <JobBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb7b2-106">Idfilterset</span><span class="sxs-lookup"><span data-stu-id="fb7b2-106">IdFilterSet</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-JobId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb7b2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb7b2-107">DESCRIPTION</span></span>
<span data-ttu-id="fb7b2-108">**Get-AzureRmRecoveryServicesBackupJobDetails** cmdlet 'i belirtilen Iş Için Azure yedekleme iş ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="fb7b2-108">The **Get-AzureRmRecoveryServicesBackupJobDetails** cmdlet gets Azure Backup job details for a specified job.</span></span>

<span data-ttu-id="fb7b2-109">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="fb7b2-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="fb7b2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb7b2-110">EXAMPLES</span></span>

### <span data-ttu-id="fb7b2-111">Örnek 1: başarısız işler için yedekleme işi ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="fb7b2-111">Example 1: Get Backup job details for failed jobs</span></span>
```
PS C:\>$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzureRmRecoveryServicesBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="fb7b2-112">İlk komut kasada başarısız olan işlerin dizisini alır ve bunları $Jobs dizisinde depolar.</span><span class="sxs-lookup"><span data-stu-id="fb7b2-112">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>

<span data-ttu-id="fb7b2-113">İkinci komut $Jobs başarısız olan işlerin iş ayrıntılarını alır ve $JobDetails değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="fb7b2-113">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>

<span data-ttu-id="fb7b2-114">Son komutu başarısız olan işlerin hata ayrıntılarını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="fb7b2-114">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="fb7b2-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb7b2-115">PARAMETERS</span></span>

### <span data-ttu-id="fb7b2-116">-Job</span><span class="sxs-lookup"><span data-stu-id="fb7b2-116">-Job</span></span>
<span data-ttu-id="fb7b2-117">Alınacak işi belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb7b2-117">Specifies the job to get.</span></span>
<span data-ttu-id="fb7b2-118">**Backupjob** nesnesi edinmek için Get-AzureRmRecoveryServicesBackupJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fb7b2-118">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: JobFilterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb7b2-119">-JobId</span><span class="sxs-lookup"><span data-stu-id="fb7b2-119">-JobId</span></span>
<span data-ttu-id="fb7b2-120">Yedekleme işinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb7b2-120">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="fb7b2-121">ID, **Backupjob** nesnesinin InstanceId özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="fb7b2-121">The ID is the InstanceId property of a **BackupJob** object.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFilterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb7b2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb7b2-122">-DefaultProfile</span></span>
<span data-ttu-id="fb7b2-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fb7b2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb7b2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb7b2-124">CommonParameters</span></span>
<span data-ttu-id="fb7b2-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb7b2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb7b2-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb7b2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb7b2-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb7b2-127">INPUTS</span></span>

## <span data-ttu-id="fb7b2-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb7b2-128">OUTPUTS</span></span>

### <span data-ttu-id="fb7b2-129">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="fb7b2-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="fb7b2-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb7b2-130">NOTES</span></span>

## <span data-ttu-id="fb7b2-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb7b2-131">RELATED LINKS</span></span>

[<span data-ttu-id="fb7b2-132">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="fb7b2-132">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


