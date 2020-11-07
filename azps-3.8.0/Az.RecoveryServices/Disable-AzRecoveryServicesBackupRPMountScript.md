---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: 5796abe47efd1ca6d68aee3663d1bbb810e80ba7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938221"
---
# <span data-ttu-id="e69ff-101">Disable-AzRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="e69ff-101">Disable-AzRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="e69ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e69ff-102">SYNOPSIS</span></span>
<span data-ttu-id="e69ff-103">Kurtarma noktasının tüm dosyalarını çıkarır.</span><span class="sxs-lookup"><span data-stu-id="e69ff-103">Dismounts all the files of the recovery point.</span></span>

## <span data-ttu-id="e69ff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e69ff-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [-PassThru]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e69ff-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e69ff-105">DESCRIPTION</span></span>
<span data-ttu-id="e69ff-106">Disable-AzRecoveryServicesBackupRPMountScript cmdlet 'i, daha önce Get-AzRecoveryServicesBackupRPMountScript cmdlet 'i kullanılarak bağlanmış olan kurtarma noktası dosyalarını çıkarır.</span><span class="sxs-lookup"><span data-stu-id="e69ff-106">The Disable-AzRecoveryServicesBackupRPMountScript cmdlet dismounts the files of the recovery point which were mounted earlier using the Get-AzRecoveryServicesBackupRPMountScript cmdlet.</span></span>

## <span data-ttu-id="e69ff-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e69ff-107">EXAMPLES</span></span>

### <span data-ttu-id="e69ff-108">Örnek 1: kurtarma noktasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="e69ff-108">Example 1: Dismount a recovery point</span></span>
```
PS C:\> $namedContainer = Get-AzRecoveryServicesBackupContainer  -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM"
PS C:\> $backupitem = Get-AzRecoveryServicesBackupItem -Container $namedContainer  -WorkloadType "AzureVM"
PS C:\> $startDate = (Get-Date).AddDays(-7)
PS C:\> $endDate = Get-Date
PS C:\> $rp = Get-AzRecoveryServicesBackupRecoveryPoint -Item $backupitem -StartDate $startdate.ToUniversalTime() -EndDate $enddate.ToUniversalTime()

To mount files of the latest recovery point, obtain the script by

PS C:\> Get-AzRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]

OsType  Password        Filename
------  --------        --------
Windows e3632984e51f496 V2VM_wus2_8287309959960546283_451516692429_cbd6061f7fc543c489f1974d33659fed07a6e0c2e08740.exe

When the script is run, it will mount the files of the recovery point $rp[0]

After the relevant files are copied, then you remove the files of the recovery point by running the disable cmdlet

PS C:\> Disable-AzRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]
```

## <span data-ttu-id="e69ff-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e69ff-109">PARAMETERS</span></span>

### <span data-ttu-id="e69ff-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e69ff-110">-DefaultProfile</span></span>
<span data-ttu-id="e69ff-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e69ff-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e69ff-112">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e69ff-112">-PassThru</span></span>
<span data-ttu-id="e69ff-113">Kurtarma noktasını döndür.</span><span class="sxs-lookup"><span data-stu-id="e69ff-113">Return the recovery point.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e69ff-114">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="e69ff-114">-RecoveryPoint</span></span>
<span data-ttu-id="e69ff-115">Geri yüklenecek kurtarma noktası nesnesi</span><span class="sxs-lookup"><span data-stu-id="e69ff-115">Recovery point object to be restored</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e69ff-116">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e69ff-116">-VaultId</span></span>
<span data-ttu-id="e69ff-117">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e69ff-117">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e69ff-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="e69ff-118">-Confirm</span></span>
<span data-ttu-id="e69ff-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e69ff-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e69ff-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e69ff-120">-WhatIf</span></span>
<span data-ttu-id="e69ff-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e69ff-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e69ff-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e69ff-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e69ff-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e69ff-123">CommonParameters</span></span>
<span data-ttu-id="e69ff-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e69ff-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e69ff-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e69ff-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e69ff-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e69ff-126">INPUTS</span></span>

### <span data-ttu-id="e69ff-127">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="e69ff-127">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

### <span data-ttu-id="e69ff-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e69ff-128">System.String</span></span>

## <span data-ttu-id="e69ff-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e69ff-129">OUTPUTS</span></span>

### <span data-ttu-id="e69ff-130">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="e69ff-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="e69ff-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e69ff-131">NOTES</span></span>

## <span data-ttu-id="e69ff-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e69ff-132">RELATED LINKS</span></span>
