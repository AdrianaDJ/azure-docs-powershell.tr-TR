---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: 6caf37bf8e9b4bc11969ff4f1e0e55e7e0d6880c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591299"
---
# <span data-ttu-id="8fc55-101">Get-AzureRmRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="8fc55-101">Get-AzureRmRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="8fc55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fc55-102">SYNOPSIS</span></span>
<span data-ttu-id="8fc55-103">Kurtarma noktasının tüm dosyalarını bağlamak için bir betik indirir.</span><span class="sxs-lookup"><span data-stu-id="8fc55-103">Downloads a script to mount all the files of the recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fc55-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8fc55-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [[-Path] <String>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fc55-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8fc55-105">DESCRIPTION</span></span>
<span data-ttu-id="8fc55-106">Get-AzureRmRecoveryServicesBackupRPMountScript cmdlet 'i, çalıştırıldığı makinede kurtarma noktası birimlerini takar.</span><span class="sxs-lookup"><span data-stu-id="8fc55-106">The Get-AzureRmRecoveryServicesBackupRPMountScript cmdlet downloads a script which mounts the volumes of the recovery point on the machine where it is run.</span></span>

## <span data-ttu-id="8fc55-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8fc55-107">EXAMPLES</span></span>

### <span data-ttu-id="8fc55-108">Örnek 1: kurtarma noktası bağlama</span><span class="sxs-lookup"><span data-stu-id="8fc55-108">Example 1: Mount a recovery point</span></span>
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
```

<span data-ttu-id="8fc55-109">Komut dosyası çalıştırıldığında, kurtarma noktasının \[ dosyalarını $RP\]</span><span class="sxs-lookup"><span data-stu-id="8fc55-109">When the script is run, it will mount the files of the recovery point $rp\[0\]</span></span>

## <span data-ttu-id="8fc55-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8fc55-110">PARAMETERS</span></span>

### <span data-ttu-id="8fc55-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fc55-111">-DefaultProfile</span></span>
<span data-ttu-id="8fc55-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8fc55-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fc55-113">-Yol</span><span class="sxs-lookup"><span data-stu-id="8fc55-113">-Path</span></span>
<span data-ttu-id="8fc55-114">Dosya kurtarma durumunda dosyanın indirileceği konum.</span><span class="sxs-lookup"><span data-stu-id="8fc55-114">Location where the file should be downloaded in the case of file recovery.</span></span> <span data-ttu-id="8fc55-115">-Path sağlanmazsa, komut dosyası geçerli dizine indirilir.</span><span class="sxs-lookup"><span data-stu-id="8fc55-115">If -Path is not provided, the script file will be downloaded in the current directory.</span></span>

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

### <span data-ttu-id="8fc55-116">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="8fc55-116">-RecoveryPoint</span></span>
<span data-ttu-id="8fc55-117">Geri yüklenecek kurtarma noktası nesnesi</span><span class="sxs-lookup"><span data-stu-id="8fc55-117">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="8fc55-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="8fc55-118">-VaultId</span></span>
<span data-ttu-id="8fc55-119">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8fc55-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8fc55-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="8fc55-120">-Confirm</span></span>
<span data-ttu-id="8fc55-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8fc55-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fc55-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fc55-122">-WhatIf</span></span>
<span data-ttu-id="8fc55-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8fc55-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fc55-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8fc55-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fc55-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fc55-125">CommonParameters</span></span>
<span data-ttu-id="8fc55-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8fc55-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fc55-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fc55-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fc55-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8fc55-128">INPUTS</span></span>

### <span data-ttu-id="8fc55-129">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="8fc55-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="8fc55-130">Parametreler: RecoveryPoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8fc55-130">Parameters: RecoveryPoint (ByValue)</span></span>

### <span data-ttu-id="8fc55-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8fc55-131">System.String</span></span>
<span data-ttu-id="8fc55-132">Parametreler: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8fc55-132">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="8fc55-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8fc55-133">OUTPUTS</span></span>

### <span data-ttu-id="8fc55-134">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. RPMountScriptDetails</span><span class="sxs-lookup"><span data-stu-id="8fc55-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RPMountScriptDetails</span></span>

## <span data-ttu-id="8fc55-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8fc55-135">NOTES</span></span>

## <span data-ttu-id="8fc55-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8fc55-136">RELATED LINKS</span></span>
