---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: 0f3f0292b4f348207bf80d5e04c63dc45be69fa3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587496"
---
# <span data-ttu-id="b11af-101">Get-AzureRmRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="b11af-101">Get-AzureRmRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="b11af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b11af-102">SYNOPSIS</span></span>
<span data-ttu-id="b11af-103">Kurtarma noktasının tüm dosyalarını bağlamak için bir betik indirir.</span><span class="sxs-lookup"><span data-stu-id="b11af-103">Downloads a script to mount all the files of the recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b11af-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b11af-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b11af-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b11af-105">DESCRIPTION</span></span>
<span data-ttu-id="b11af-106">Get-AzureRmRecoveryServicesBackupRPMountScript cmdlet 'i, çalıştırıldığı makinede kurtarma noktası birimlerini takar.</span><span class="sxs-lookup"><span data-stu-id="b11af-106">The Get-AzureRmRecoveryServicesBackupRPMountScript cmdlet downloads a script which mounts the volumes of the recovery point on the machine where it is run.</span></span>

## <span data-ttu-id="b11af-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b11af-107">EXAMPLES</span></span>

### <span data-ttu-id="b11af-108">Örnek 1: kurtarma noktası bağlama</span><span class="sxs-lookup"><span data-stu-id="b11af-108">Example 1: Mount a recovery point</span></span>
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

<span data-ttu-id="b11af-109">Komut dosyası çalıştırıldığında, kurtarma noktasının \[ dosyalarını $RP\]</span><span class="sxs-lookup"><span data-stu-id="b11af-109">When the script is run, it will mount the files of the recovery point $rp\[0\]</span></span>

## <span data-ttu-id="b11af-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b11af-110">PARAMETERS</span></span>

### <span data-ttu-id="b11af-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b11af-111">-DefaultProfile</span></span>
<span data-ttu-id="b11af-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b11af-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b11af-113">-Yol</span><span class="sxs-lookup"><span data-stu-id="b11af-113">-Path</span></span>
<span data-ttu-id="b11af-114">Dosya kurtarma durumunda dosyanın indirileceği konum.</span><span class="sxs-lookup"><span data-stu-id="b11af-114">Location where the file should be downloaded in the case of file recovery.</span></span> <span data-ttu-id="b11af-115">-Path sağlanmazsa, komut dosyası geçerli dizine indirilir.</span><span class="sxs-lookup"><span data-stu-id="b11af-115">If -Path is not provided, the script file will be downloaded in the current directory.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b11af-116">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="b11af-116">-RecoveryPoint</span></span>
<span data-ttu-id="b11af-117">Geri yüklenecek kurtarma noktası nesnesi</span><span class="sxs-lookup"><span data-stu-id="b11af-117">Recovery point object to be restored</span></span>

```yaml
Type: RecoveryPointBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b11af-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="b11af-118">-Confirm</span></span>
<span data-ttu-id="b11af-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b11af-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b11af-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b11af-120">-WhatIf</span></span>
<span data-ttu-id="b11af-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b11af-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b11af-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b11af-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b11af-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b11af-123">CommonParameters</span></span>
<span data-ttu-id="b11af-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b11af-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b11af-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b11af-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b11af-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b11af-126">INPUTS</span></span>

### <span data-ttu-id="b11af-127">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="b11af-127">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="b11af-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b11af-128">OUTPUTS</span></span>

### <span data-ttu-id="b11af-129">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. RPMountScriptDetails</span><span class="sxs-lookup"><span data-stu-id="b11af-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RPMountScriptDetails</span></span>

## <span data-ttu-id="b11af-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b11af-130">NOTES</span></span>

## <span data-ttu-id="b11af-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b11af-131">RELATED LINKS</span></span>

