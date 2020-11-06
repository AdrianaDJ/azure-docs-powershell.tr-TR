---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
ms.openlocfilehash: 7d39ce49a76d8519f2eacf0649c52051290274f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587222"
---
# <span data-ttu-id="b2d61-101">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="b2d61-101">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>

## <span data-ttu-id="b2d61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2d61-102">SYNOPSIS</span></span>
<span data-ttu-id="b2d61-103">Yedekleme işinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="b2d61-103">Gets details for a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2d61-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b2d61-104">SYNTAX</span></span>

### <span data-ttu-id="b2d61-105">JobFilterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b2d61-105">JobFilterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2d61-106">Idfilterset</span><span class="sxs-lookup"><span data-stu-id="b2d61-106">IdFilterSet</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2d61-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b2d61-107">DESCRIPTION</span></span>
<span data-ttu-id="b2d61-108">**Get-AzureRmRecoveryServicesBackupJobDetails** cmdlet 'i belirtilen Iş Için Azure yedekleme iş ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="b2d61-108">The **Get-AzureRmRecoveryServicesBackupJobDetails** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="b2d61-109">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b2d61-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="b2d61-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b2d61-110">EXAMPLES</span></span>

### <span data-ttu-id="b2d61-111">Örnek 1: başarısız işler için yedekleme işi ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="b2d61-111">Example 1: Get Backup job details for failed jobs</span></span>
```
PS C:\>$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzureRmRecoveryServicesBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="b2d61-112">İlk komut kasada başarısız olan işlerin dizisini alır ve bunları $Jobs dizisinde depolar.</span><span class="sxs-lookup"><span data-stu-id="b2d61-112">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="b2d61-113">İkinci komut $Jobs başarısız olan işlerin iş ayrıntılarını alır ve $JobDetails değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b2d61-113">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="b2d61-114">Son komutu başarısız olan işlerin hata ayrıntılarını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="b2d61-114">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="b2d61-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b2d61-115">PARAMETERS</span></span>

### <span data-ttu-id="b2d61-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2d61-116">-DefaultProfile</span></span>
<span data-ttu-id="b2d61-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b2d61-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2d61-118">-Job</span><span class="sxs-lookup"><span data-stu-id="b2d61-118">-Job</span></span>
<span data-ttu-id="b2d61-119">Alınacak işi belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2d61-119">Specifies the job to get.</span></span>
<span data-ttu-id="b2d61-120">**Backupjob** nesnesi edinmek için Get-AzureRmRecoveryServicesBackupJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b2d61-120">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="b2d61-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="b2d61-121">-JobId</span></span>
<span data-ttu-id="b2d61-122">Yedekleme işinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2d61-122">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="b2d61-123">ID, **Backupjob** nesnesinin InstanceId özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="b2d61-123">The ID is the InstanceId property of a **BackupJob** object.</span></span>

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

### <span data-ttu-id="b2d61-124">-VaultId</span><span class="sxs-lookup"><span data-stu-id="b2d61-124">-VaultId</span></span>
<span data-ttu-id="b2d61-125">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b2d61-125">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2d61-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2d61-126">CommonParameters</span></span>
<span data-ttu-id="b2d61-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b2d61-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2d61-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2d61-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2d61-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b2d61-129">INPUTS</span></span>

### <span data-ttu-id="b2d61-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b2d61-130">System.String</span></span>
<span data-ttu-id="b2d61-131">Parametreler: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b2d61-131">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="b2d61-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b2d61-132">OUTPUTS</span></span>

### <span data-ttu-id="b2d61-133">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="b2d61-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="b2d61-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b2d61-134">NOTES</span></span>

## <span data-ttu-id="b2d61-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b2d61-135">RELATED LINKS</span></span>

[<span data-ttu-id="b2d61-136">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="b2d61-136">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


