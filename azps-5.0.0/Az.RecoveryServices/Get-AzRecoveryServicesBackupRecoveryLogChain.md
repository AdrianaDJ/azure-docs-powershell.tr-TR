---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: ba82e1ddf8385f74b271feb9119280d48fc1b859
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276858"
---
# <span data-ttu-id="aede1-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span><span class="sxs-lookup"><span data-stu-id="aede1-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span></span>

## <span data-ttu-id="aede1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aede1-102">SYNOPSIS</span></span>
<span data-ttu-id="aede1-103">Bu komut, verilen yedekleme öğesinin kopuk olmayan günlük zincirinin başlangıç ve bitiş noktalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="aede1-103">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="aede1-104">Kullanıcının VERITABANıNA geri yüklenmesini istediğini, geçerli olup olmadığını belirlemek için bu uygulamayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="aede1-104">Use it to determine whether the point-in-time, to which the user wants the DB to be restored, is valid or not.</span></span>

## <span data-ttu-id="aede1-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aede1-105">SYNTAX</span></span>

### <span data-ttu-id="aede1-106">NoFilterParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="aede1-106">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aede1-107">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="aede1-107">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aede1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="aede1-108">DESCRIPTION</span></span>
<span data-ttu-id="aede1-109">**Get-Azrecoveryservicesbackuprecoverylogzincirine** cmdlet 'i, yedeklenen bir Azure yedekleme öğesi için zaman aralığı kurtarma noktalarını alır.</span><span class="sxs-lookup"><span data-stu-id="aede1-109">The **Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet gets the time range recovery points in time for a backed up Azure Backup item.</span></span>
<span data-ttu-id="aede1-110">Bir öğe yedeklendikten sonra, bir **Azrecoveryservicesbackuprecoverylogzincirine** nesnesinin bir veya daha fazla kurtarma zamanı aralığı vardır.</span><span class="sxs-lookup"><span data-stu-id="aede1-110">After an item has been backed up, an **AzRecoveryServicesBackupRecoveryLogChain** object has one or more recovery time ranges.</span></span>

## <span data-ttu-id="aede1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aede1-111">EXAMPLES</span></span>

### <span data-ttu-id="aede1-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="aede1-112">Example 1</span></span>
```powershell
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="aede1-113">İlk komut yedi günden önce tarihini alır ve $StartDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="aede1-113">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="aede1-114">İkinci komut bugünün tarihini alır ve $EndDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="aede1-114">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="aede1-115">Üçüncü komut AzureWorkload yedekleme kapsayıcılarını alır ve bunları $Container değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="aede1-115">The third command gets AzureWorkload backup containers, and stores them in the $Container variable.</span></span>
<span data-ttu-id="aede1-116">Dördüncü komut yedek öğeyi alır ve ardından bunu bir yedekleme öğesi nesnesi olarak Piped cmdlet 'inde paylaşır.</span><span class="sxs-lookup"><span data-stu-id="aede1-116">The fourth command gets the backup item, and then shares it across the piped cmdlet as backup item object.</span></span>
<span data-ttu-id="aede1-117">Son komut $BackupItem öğesindeki öğenin kurtarma noktası zaman aralıklarının dizisini alır ve $RP değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="aede1-117">The last command gets an array of recovery point time ranges for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

### <span data-ttu-id="aede1-118">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="aede1-118">Example 2</span></span>

<span data-ttu-id="aede1-119">Bu komut, verilen yedekleme öğesinin kopuk olmayan günlük zincirinin başlangıç ve bitiş noktalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="aede1-119">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="aede1-120">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="aede1-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupRecoveryLogChain -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="aede1-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aede1-121">PARAMETERS</span></span>

### <span data-ttu-id="aede1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aede1-122">-DefaultProfile</span></span>
<span data-ttu-id="aede1-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aede1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aede1-124">-EndDate</span><span class="sxs-lookup"><span data-stu-id="aede1-124">-EndDate</span></span>
<span data-ttu-id="aede1-125">Kurtarma noktasının getirilmesi gereken zaman aralığının bitiş zamanı</span><span class="sxs-lookup"><span data-stu-id="aede1-125">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="aede1-126">-Öğe</span><span class="sxs-lookup"><span data-stu-id="aede1-126">-Item</span></span>
<span data-ttu-id="aede1-127">Kurtarma noktasının getirilmesi gereken korumalı öğe nesnesi</span><span class="sxs-lookup"><span data-stu-id="aede1-127">Protected Item object for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="aede1-128">-StartDate</span><span class="sxs-lookup"><span data-stu-id="aede1-128">-StartDate</span></span>
<span data-ttu-id="aede1-129">Kurtarma noktasının getirilmesi gereken zaman aralığının başlangıç saati</span><span class="sxs-lookup"><span data-stu-id="aede1-129">Start time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="aede1-130">-VaultId</span><span class="sxs-lookup"><span data-stu-id="aede1-130">-VaultId</span></span>
<span data-ttu-id="aede1-131">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="aede1-131">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="aede1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aede1-132">CommonParameters</span></span>
<span data-ttu-id="aede1-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aede1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aede1-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="aede1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aede1-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aede1-135">INPUTS</span></span>

### <span data-ttu-id="aede1-136">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Itembase</span><span class="sxs-lookup"><span data-stu-id="aede1-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="aede1-137">System. String</span><span class="sxs-lookup"><span data-stu-id="aede1-137">System.String</span></span>

## <span data-ttu-id="aede1-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aede1-138">OUTPUTS</span></span>

### <span data-ttu-id="aede1-139">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="aede1-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="aede1-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aede1-140">NOTES</span></span>

## <span data-ttu-id="aede1-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aede1-141">RELATED LINKS</span></span>
