---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/disable-azurermrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: bcb3da6f7425f759ab8d4142e5c62a8aa68e85e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762297"
---
# <span data-ttu-id="1ceff-101">Disable-AzureRmRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="1ceff-101">Disable-AzureRmRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="1ceff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ceff-102">SYNOPSIS</span></span>
<span data-ttu-id="1ceff-103">Kurtarma noktasının tüm dosyalarını çıkarır.</span><span class="sxs-lookup"><span data-stu-id="1ceff-103">Dismounts all the files of the recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ceff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1ceff-104">SYNTAX</span></span>

```
Disable-AzureRmRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [-PassThru]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ceff-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1ceff-105">DESCRIPTION</span></span>
<span data-ttu-id="1ceff-106">Disable-AzureRmRecoveryServicesBackupRPMountScript cmdlet 'i, daha önce Get-AzureRmRecoveryServicesBackupRPMountScript cmdlet 'i kullanılarak bağlanmış olan kurtarma noktası dosyalarını çıkarır.</span><span class="sxs-lookup"><span data-stu-id="1ceff-106">The Disable-AzureRmRecoveryServicesBackupRPMountScript cmdlet dismounts the files of the recovery point which were mounted earlier using the Get-AzureRmRecoveryServicesBackupRPMountScript cmdlet.</span></span>

## <span data-ttu-id="1ceff-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1ceff-107">EXAMPLES</span></span>

### <span data-ttu-id="1ceff-108">Örnek 1: kurtarma noktasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="1ceff-108">Example 1: Dismount a recovery point</span></span>
```
PS C:\> $namedContainer = Get-AzureRmRecoveryServicesBackupContainer  -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM"
PS C:\> $backupitem = Get-AzureRmRecoveryServicesBackupItem -Container $namedContainer  -WorkloadType "AzureVM"
PS C:\> $startDate = (Get-Date).AddDays(-7)
PS C:\> $endDate = Get-Date
PS C:\> $rp = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $backupitem -StartDate $startdate.ToUniversalTime() -EndDate $enddate.ToUniversalTime()

To mount files of the latest recovery point, obtain the script by

PS C:\> Get-AzureRmRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]

OsType  Password        Filename
------  --------        --------
Windows e3632984e51f496 V2VM_wus2_8287309959960546283_451516692429_cbd6061f7fc543c489f1974d33659fed07a6e0c2e08740.exe

When the script is run, it will mount the files of the recovery point $rp[0]

After the relevant files are copied, then you remove the files of the recovery point by running the disable cmdlet

PS C:\> Disable-AzureRmRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]
```

## <span data-ttu-id="1ceff-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1ceff-109">PARAMETERS</span></span>

### <span data-ttu-id="1ceff-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ceff-110">-DefaultProfile</span></span>
<span data-ttu-id="1ceff-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1ceff-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ceff-112">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1ceff-112">-PassThru</span></span>
<span data-ttu-id="1ceff-113">Kurtarma noktasını döndür.</span><span class="sxs-lookup"><span data-stu-id="1ceff-113">Return the recovery point.</span></span>

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

### <span data-ttu-id="1ceff-114">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="1ceff-114">-RecoveryPoint</span></span>
<span data-ttu-id="1ceff-115">Geri yüklenecek kurtarma noktası nesnesi</span><span class="sxs-lookup"><span data-stu-id="1ceff-115">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="1ceff-116">-VaultId</span><span class="sxs-lookup"><span data-stu-id="1ceff-116">-VaultId</span></span>
<span data-ttu-id="1ceff-117">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1ceff-117">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="1ceff-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="1ceff-118">-Confirm</span></span>
<span data-ttu-id="1ceff-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1ceff-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ceff-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ceff-120">-WhatIf</span></span>
<span data-ttu-id="1ceff-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1ceff-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ceff-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1ceff-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ceff-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ceff-123">CommonParameters</span></span>
<span data-ttu-id="1ceff-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1ceff-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ceff-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ceff-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ceff-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1ceff-126">INPUTS</span></span>

### <span data-ttu-id="1ceff-127">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="1ceff-127">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="1ceff-128">Parametreler: RecoveryPoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1ceff-128">Parameters: RecoveryPoint (ByValue)</span></span>

### <span data-ttu-id="1ceff-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1ceff-129">System.String</span></span>
<span data-ttu-id="1ceff-130">Parametreler: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1ceff-130">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="1ceff-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1ceff-131">OUTPUTS</span></span>

### <span data-ttu-id="1ceff-132">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="1ceff-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="1ceff-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1ceff-133">NOTES</span></span>

## <span data-ttu-id="1ceff-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1ceff-134">RELATED LINKS</span></span>
