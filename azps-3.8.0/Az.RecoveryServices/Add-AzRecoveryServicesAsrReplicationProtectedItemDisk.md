---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/add-azrecoveryservicesasrreplicationprotecteditemdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: ab8c2bb74f381be898dc243ddd010462f8158ed2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096479"
---
# <span data-ttu-id="29f29-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="29f29-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="29f29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29f29-102">SYNOPSIS</span></span>
<span data-ttu-id="29f29-103">Korunan Azure sanal makinesi için korumayı diskete ekleyin.</span><span class="sxs-lookup"><span data-stu-id="29f29-103">Add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="29f29-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="29f29-104">SYNTAX</span></span>

```
Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29f29-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="29f29-105">DESCRIPTION</span></span>
<span data-ttu-id="29f29-106">**Add-Azrecoveryservicesasrreplicationkorunabilir Koruyucutemdisk** cmdlet 'i, korunan Azure sanal makinesi için diski ekler.</span><span class="sxs-lookup"><span data-stu-id="29f29-106">The **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="29f29-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="29f29-107">EXAMPLES</span></span>

### <span data-ttu-id="29f29-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="29f29-108">Example 1</span></span>
```powershell
PS C:> Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="29f29-109">Koruma için belirtilen disk yapılandırmasını eklemek için işlemi başlatın.</span><span class="sxs-lookup"><span data-stu-id="29f29-109">Start the operation to add specified disk configuration for protection.</span></span>

### <span data-ttu-id="29f29-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="29f29-110">Example 2</span></span>
```powershell
PS C:> $ReplicationProtectedItem |Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="29f29-111">Koruma için belirtilen disk yapılandırmasını eklemek için işlemi başlatın. Giriş çoğaltması korumalı öğeyi boru.</span><span class="sxs-lookup"><span data-stu-id="29f29-111">Start the operation to add specified disk configuration for protection.Piping input replication protected item.</span></span>

## <span data-ttu-id="29f29-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="29f29-112">PARAMETERS</span></span>

### <span data-ttu-id="29f29-113">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="29f29-113">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="29f29-114">Azure için disk koruması için kullanılan disk yapılandırmasını Azure 'tan Azure olağanüstü durum kurtarma senaryosuna belirtir.</span><span class="sxs-lookup"><span data-stu-id="29f29-114">Specifies the disk configuration to used for disk protection for Azure to Azure disaster recovery scenario.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f29-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29f29-115">-DefaultProfile</span></span>
<span data-ttu-id="29f29-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="29f29-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29f29-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29f29-117">-InputObject</span></span>
<span data-ttu-id="29f29-118">Cmdlet 'e giriş nesnesi: yeni diske karşılık gelen ASR çoğaltması korumalı öğe nesnesi.</span><span class="sxs-lookup"><span data-stu-id="29f29-118">The input object to the cmdlet: The ASR replication protected item object corresponding to which new disk should be protected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29f29-119">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="29f29-119">-WaitForCompletion</span></span>
<span data-ttu-id="29f29-120">Tamamlanması Için bekle</span><span class="sxs-lookup"><span data-stu-id="29f29-120">Wait For Completion</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f29-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="29f29-121">-Confirm</span></span>
<span data-ttu-id="29f29-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="29f29-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f29-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29f29-123">-WhatIf</span></span>
<span data-ttu-id="29f29-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="29f29-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29f29-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="29f29-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f29-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29f29-126">CommonParameters</span></span>
<span data-ttu-id="29f29-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="29f29-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29f29-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="29f29-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29f29-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="29f29-129">INPUTS</span></span>

### <span data-ttu-id="29f29-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="29f29-130">None</span></span>

## <span data-ttu-id="29f29-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="29f29-131">OUTPUTS</span></span>

### <span data-ttu-id="29f29-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="29f29-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="29f29-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="29f29-133">NOTES</span></span>

## <span data-ttu-id="29f29-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="29f29-134">RELATED LINKS</span></span>
