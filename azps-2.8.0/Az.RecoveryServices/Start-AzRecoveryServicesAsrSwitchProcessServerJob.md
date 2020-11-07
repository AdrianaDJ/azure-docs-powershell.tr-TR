---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: 4f926b88214a60cc05b6eb9666e10fa8ed7bf3ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933441"
---
# <span data-ttu-id="0893c-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="0893c-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="0893c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0893c-102">SYNOPSIS</span></span>
<span data-ttu-id="0893c-103">Yük Dengelemesi için bir Process sunucusundan diğerine çoğaltmayı değiştirin.</span><span class="sxs-lookup"><span data-stu-id="0893c-103">Switch replication from one Process server to another for load balancing.</span></span>

## <span data-ttu-id="0893c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0893c-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric> -SourceProcessServer <ASRProcessServer>
 -TargetProcessServer <ASRProcessServer> [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0893c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0893c-105">DESCRIPTION</span></span>
<span data-ttu-id="0893c-106">**Start-AzRecoveryServicesAsrSwitchProcessServerJob** belirtilen sanal makineler için çoğaltma veri hareketini veya belirtilen bir işlem sunucusunu belirtilen hedef işlem sunucusuna geçirir.</span><span class="sxs-lookup"><span data-stu-id="0893c-106">The **Start-AzRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="0893c-107">Yük Dengeleme veya süreç sunucuları arasında çoğaltmayı değiştirme için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0893c-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="0893c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0893c-108">EXAMPLES</span></span>

### <span data-ttu-id="0893c-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0893c-109">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="0893c-110">Kaynaktan hedef işlem sunucusuna olan tüm çoğaltma korumalı öğeler için geçiş işlem sunucusunu izlemeye iş.</span><span class="sxs-lookup"><span data-stu-id="0893c-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="0893c-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0893c-111">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="0893c-112">Çoğaltmanın korumalı öğesini kaynaktan hedef işlem sunucusuna geçirilmiş şekilde işleyen işleme sunucusu</span><span class="sxs-lookup"><span data-stu-id="0893c-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="0893c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0893c-113">PARAMETERS</span></span>

### <span data-ttu-id="0893c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0893c-114">-DefaultProfile</span></span>
<span data-ttu-id="0893c-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0893c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0893c-116">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="0893c-116">-Fabric</span></span>
<span data-ttu-id="0893c-117">Yapılandırma sunucusuna karşılık gelen site kurtarma yapısı.</span><span class="sxs-lookup"><span data-stu-id="0893c-117">Site recovery fabric corresponding to the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: ConfigServer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0893c-118">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="0893c-118">-ReplicationProtectedItem</span></span>
<span data-ttu-id="0893c-119">İşlemleri sunucusu değiştirilmiş çoğaltma korumalı öğesi listesi.</span><span class="sxs-lookup"><span data-stu-id="0893c-119">List of replication protected item whose process server to be switched.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: (All)
Aliases: ReplicatedItem

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0893c-120">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="0893c-120">-SourceProcessServer</span></span>
<span data-ttu-id="0893c-121">Çoğaltmayı dışarı geçirmek için Işlem sunucusu.</span><span class="sxs-lookup"><span data-stu-id="0893c-121">The Process server to switch replication out from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0893c-122">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="0893c-122">-TargetProcessServer</span></span>
<span data-ttu-id="0893c-123">Çoğaltmaya geçiş yapmak için Process Server.</span><span class="sxs-lookup"><span data-stu-id="0893c-123">The Process server to switch replication to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0893c-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="0893c-124">-Confirm</span></span>
<span data-ttu-id="0893c-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0893c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0893c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0893c-126">-WhatIf</span></span>
<span data-ttu-id="0893c-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0893c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0893c-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0893c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0893c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0893c-129">CommonParameters</span></span>
<span data-ttu-id="0893c-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0893c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0893c-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0893c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0893c-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0893c-132">INPUTS</span></span>

### <span data-ttu-id="0893c-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0893c-133">None</span></span>

## <span data-ttu-id="0893c-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0893c-134">OUTPUTS</span></span>

### <span data-ttu-id="0893c-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0893c-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0893c-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0893c-136">NOTES</span></span>

## <span data-ttu-id="0893c-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0893c-137">RELATED LINKS</span></span>
