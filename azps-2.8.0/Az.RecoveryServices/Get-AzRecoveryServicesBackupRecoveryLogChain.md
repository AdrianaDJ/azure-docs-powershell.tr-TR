---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: d06cae4fc13151d8b1c5c2b0fb4dd7803606fe49
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933003"
---
# <span data-ttu-id="59864-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span><span class="sxs-lookup"><span data-stu-id="59864-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span></span>

## <span data-ttu-id="59864-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59864-102">SYNOPSIS</span></span>
<span data-ttu-id="59864-103">Bu komut, verilen yedekleme öğesinin kopuk olmayan günlük zincirinin başlangıç ve bitiş noktalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="59864-103">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="59864-104">Kullanıcının VERITABANıNA geri yüklenmesini istediğini, geçerli olup olmadığını belirlemek için bu uygulamayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="59864-104">Use it to determine whether the point-in-time, to which the user wants the DB to be restored, is valid or not.</span></span>

## <span data-ttu-id="59864-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59864-105">SYNTAX</span></span>

### <span data-ttu-id="59864-106">NoFilterParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="59864-106">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59864-107">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="59864-107">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59864-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="59864-108">DESCRIPTION</span></span>
<span data-ttu-id="59864-109">**Get-Azrecoveryservicesbackuprecoverylogzincirine** cmdlet 'i, yedeklenen bir Azure yedekleme öğesi için zaman aralığı kurtarma noktalarını alır.</span><span class="sxs-lookup"><span data-stu-id="59864-109">The **Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet gets the time range recovery points in time for a backed up Azure Backup item.</span></span>
<span data-ttu-id="59864-110">Bir öğe yedeklendikten sonra, bir **Azrecoveryservicesbackuprecoverylogzincirine** nesnesinin bir veya daha fazla kurtarma zamanı aralığı vardır.</span><span class="sxs-lookup"><span data-stu-id="59864-110">After an item has been backed up, an **AzRecoveryServicesBackupRecoveryLogChain** object has one or more recovery time ranges.</span></span>

## <span data-ttu-id="59864-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59864-111">EXAMPLES</span></span>

### <span data-ttu-id="59864-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="59864-112">Example 1</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="59864-113">İlk komut yedi günden önce tarihini alır ve $StartDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="59864-113">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="59864-114">İkinci komut bugünün tarihini alır ve $EndDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="59864-114">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="59864-115">Üçüncü komut AzureWorkload yedekleme kapsayıcılarını alır ve bunları $Containers değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="59864-115">The third command gets AzureWorkload backup containers, and stores them in the $Containers variable.</span></span>
<span data-ttu-id="59864-116">Dördüncü komut yedek öğeyi alır ve $BackupItem değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="59864-116">The fourth command gets the backup item, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="59864-117">Son komut $BackupItem öğesindeki öğenin kurtarma noktası zaman aralıklarının dizisini alır ve $RP değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="59864-117">The last command gets an array of recovery point time ranges for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="59864-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59864-118">PARAMETERS</span></span>

### <span data-ttu-id="59864-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59864-119">-DefaultProfile</span></span>
<span data-ttu-id="59864-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="59864-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59864-121">-EndDate</span><span class="sxs-lookup"><span data-stu-id="59864-121">-EndDate</span></span>
<span data-ttu-id="59864-122">Kurtarma noktasının getirilmesi gereken zaman aralığının bitiş zamanı</span><span class="sxs-lookup"><span data-stu-id="59864-122">End time of Time range for which recovery point need to be fetched</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59864-123">-Öğe</span><span class="sxs-lookup"><span data-stu-id="59864-123">-Item</span></span>
<span data-ttu-id="59864-124">Kurtarma noktasının getirilmesi gereken korumalı öğe nesnesi</span><span class="sxs-lookup"><span data-stu-id="59864-124">Protected Item object for which recovery point need to be fetched</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59864-125">-StartDate</span><span class="sxs-lookup"><span data-stu-id="59864-125">-StartDate</span></span>
<span data-ttu-id="59864-126">Kurtarma noktasının getirilmesi gereken zaman aralığının başlangıç saati</span><span class="sxs-lookup"><span data-stu-id="59864-126">Start time of Time range for which recovery point need to be fetched</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59864-127">-VaultId</span><span class="sxs-lookup"><span data-stu-id="59864-127">-VaultId</span></span>
<span data-ttu-id="59864-128">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="59864-128">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="59864-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59864-129">CommonParameters</span></span>
<span data-ttu-id="59864-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59864-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59864-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59864-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59864-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59864-132">INPUTS</span></span>

### <span data-ttu-id="59864-133">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Itembase</span><span class="sxs-lookup"><span data-stu-id="59864-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="59864-134">System. String</span><span class="sxs-lookup"><span data-stu-id="59864-134">System.String</span></span>

## <span data-ttu-id="59864-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59864-135">OUTPUTS</span></span>

### <span data-ttu-id="59864-136">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="59864-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="59864-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59864-137">NOTES</span></span>

## <span data-ttu-id="59864-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59864-138">RELATED LINKS</span></span>