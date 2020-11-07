---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: 6301c621de4399509c70271eb318983e91ebd121
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933004"
---
# <span data-ttu-id="1aa66-101">Get-AzRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="1aa66-101">Get-AzRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="1aa66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1aa66-102">SYNOPSIS</span></span>
<span data-ttu-id="1aa66-103">Kurtarma noktasının tüm dosyalarını bağlamak için bir betik indirir.</span><span class="sxs-lookup"><span data-stu-id="1aa66-103">Downloads a script to mount all the files of the recovery point.</span></span>

## <span data-ttu-id="1aa66-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1aa66-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [[-Path] <String>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1aa66-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1aa66-105">DESCRIPTION</span></span>
<span data-ttu-id="1aa66-106">Get-AzRecoveryServicesBackupRPMountScript cmdlet 'i, çalıştırıldığı makinede kurtarma noktası birimlerini takar.</span><span class="sxs-lookup"><span data-stu-id="1aa66-106">The Get-AzRecoveryServicesBackupRPMountScript cmdlet downloads a script which mounts the volumes of the recovery point on the machine where it is run.</span></span>

## <span data-ttu-id="1aa66-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1aa66-107">EXAMPLES</span></span>

### <span data-ttu-id="1aa66-108">Örnek 1: kurtarma noktası bağlama</span><span class="sxs-lookup"><span data-stu-id="1aa66-108">Example 1: Mount a recovery point</span></span>
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
```

<span data-ttu-id="1aa66-109">Komut dosyası çalıştırıldığında, kurtarma noktasının \[ dosyalarını $RP\]</span><span class="sxs-lookup"><span data-stu-id="1aa66-109">When the script is run, it will mount the files of the recovery point $rp\[0\]</span></span>

## <span data-ttu-id="1aa66-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1aa66-110">PARAMETERS</span></span>

### <span data-ttu-id="1aa66-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aa66-111">-DefaultProfile</span></span>
<span data-ttu-id="1aa66-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1aa66-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1aa66-113">-Yol</span><span class="sxs-lookup"><span data-stu-id="1aa66-113">-Path</span></span>
<span data-ttu-id="1aa66-114">Dosya kurtarma durumunda dosyanın indirileceği konum.</span><span class="sxs-lookup"><span data-stu-id="1aa66-114">Location where the file should be downloaded in the case of file recovery.</span></span> <span data-ttu-id="1aa66-115">-Path sağlanmazsa, komut dosyası geçerli dizine indirilir.</span><span class="sxs-lookup"><span data-stu-id="1aa66-115">If -Path is not provided, the script file will be downloaded in the current directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aa66-116">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="1aa66-116">-RecoveryPoint</span></span>
<span data-ttu-id="1aa66-117">Geri yüklenecek kurtarma noktası nesnesi</span><span class="sxs-lookup"><span data-stu-id="1aa66-117">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="1aa66-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="1aa66-118">-VaultId</span></span>
<span data-ttu-id="1aa66-119">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1aa66-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="1aa66-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="1aa66-120">-Confirm</span></span>
<span data-ttu-id="1aa66-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1aa66-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1aa66-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1aa66-122">-WhatIf</span></span>
<span data-ttu-id="1aa66-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1aa66-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1aa66-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1aa66-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1aa66-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aa66-125">CommonParameters</span></span>
<span data-ttu-id="1aa66-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1aa66-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aa66-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1aa66-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aa66-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1aa66-128">INPUTS</span></span>

### <span data-ttu-id="1aa66-129">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="1aa66-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

### <span data-ttu-id="1aa66-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1aa66-130">System.String</span></span>

## <span data-ttu-id="1aa66-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1aa66-131">OUTPUTS</span></span>

### <span data-ttu-id="1aa66-132">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. RPMountScriptDetails</span><span class="sxs-lookup"><span data-stu-id="1aa66-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RPMountScriptDetails</span></span>

## <span data-ttu-id="1aa66-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1aa66-133">NOTES</span></span>

## <span data-ttu-id="1aa66-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1aa66-134">RELATED LINKS</span></span>
