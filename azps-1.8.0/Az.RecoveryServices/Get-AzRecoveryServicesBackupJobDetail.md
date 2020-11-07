---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: f38029a85cac1b6771a546b120714823f5b02927
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759704"
---
# <span data-ttu-id="168e2-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="168e2-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="168e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="168e2-102">SYNOPSIS</span></span>
<span data-ttu-id="168e2-103">Yedekleme işinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="168e2-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="168e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="168e2-104">SYNTAX</span></span>

### <span data-ttu-id="168e2-105">JobFilterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="168e2-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="168e2-106">Idfilterset</span><span class="sxs-lookup"><span data-stu-id="168e2-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="168e2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="168e2-107">DESCRIPTION</span></span>
<span data-ttu-id="168e2-108">**Get-AzRecoveryServicesBackupJobDetail** cmdlet 'i belirtilen Iş Için Azure yedekleme iş ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="168e2-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="168e2-109">Geçerli cmdlet 'i kullanmadan önce Set-AzRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="168e2-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="168e2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="168e2-110">EXAMPLES</span></span>

### <span data-ttu-id="168e2-111">Örnek 1: başarısız işler için yedekleme işi ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="168e2-111">Example 1: Get Backup job details for failed jobs</span></span>
```
PS C:\>$Jobs = Get-AzRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="168e2-112">İlk komut kasada başarısız olan işlerin dizisini alır ve bunları $Jobs dizisinde depolar.</span><span class="sxs-lookup"><span data-stu-id="168e2-112">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="168e2-113">İkinci komut $Jobs başarısız olan işlerin iş ayrıntılarını alır ve $JobDetails değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="168e2-113">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="168e2-114">Son komutu başarısız olan işlerin hata ayrıntılarını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="168e2-114">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="168e2-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="168e2-115">PARAMETERS</span></span>

### <span data-ttu-id="168e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="168e2-116">-DefaultProfile</span></span>
<span data-ttu-id="168e2-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="168e2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="168e2-118">-Job</span><span class="sxs-lookup"><span data-stu-id="168e2-118">-Job</span></span>
<span data-ttu-id="168e2-119">Alınacak işi belirtir.</span><span class="sxs-lookup"><span data-stu-id="168e2-119">Specifies the job to get.</span></span>
<span data-ttu-id="168e2-120">**Backupjob** nesnesi edinmek için Get-AzRecoveryServicesBackupJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="168e2-120">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="168e2-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="168e2-121">-JobId</span></span>
<span data-ttu-id="168e2-122">Yedekleme işinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="168e2-122">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="168e2-123">ID, **Backupjob** nesnesinin InstanceId özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="168e2-123">The ID is the InstanceId property of a **BackupJob** object.</span></span>

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

### <span data-ttu-id="168e2-124">-VaultId</span><span class="sxs-lookup"><span data-stu-id="168e2-124">-VaultId</span></span>
<span data-ttu-id="168e2-125">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="168e2-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="168e2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="168e2-126">CommonParameters</span></span>
<span data-ttu-id="168e2-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="168e2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="168e2-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="168e2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="168e2-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="168e2-129">INPUTS</span></span>

### <span data-ttu-id="168e2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="168e2-130">System.String</span></span>

## <span data-ttu-id="168e2-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="168e2-131">OUTPUTS</span></span>

### <span data-ttu-id="168e2-132">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="168e2-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="168e2-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="168e2-133">NOTES</span></span>

## <span data-ttu-id="168e2-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="168e2-134">RELATED LINKS</span></span>

[<span data-ttu-id="168e2-135">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="168e2-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)


