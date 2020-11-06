---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: 49e775fcb4dce90989bb03673319a8cd1bd1683a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587205"
---
# <span data-ttu-id="b77db-101">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="b77db-101">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="b77db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b77db-102">SYNOPSIS</span></span>
<span data-ttu-id="b77db-103">Yük Dengelemesi için bir Process sunucusundan diğerine çoğaltmayı değiştirin.</span><span class="sxs-lookup"><span data-stu-id="b77db-103">Switch replication from one Process server to another for load balancing.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b77db-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b77db-104">SYNTAX</span></span>

```
Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric>
 -SourceProcessServer <ASRProcessServer> -TargetProcessServer <ASRProcessServer>
 [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b77db-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b77db-105">DESCRIPTION</span></span>
<span data-ttu-id="b77db-106">**Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob** belirtilen sanal makineler için çoğaltma veri hareketini veya belirtilen bir işlem sunucusunu belirtilen hedef işlem sunucusuna geçirir.</span><span class="sxs-lookup"><span data-stu-id="b77db-106">The **Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="b77db-107">Yük Dengeleme veya süreç sunucuları arasında çoğaltmayı değiştirme için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b77db-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="b77db-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b77db-108">EXAMPLES</span></span>

### <span data-ttu-id="b77db-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b77db-109">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="b77db-110">Kaynaktan hedef işlem sunucusuna olan tüm çoğaltma korumalı öğeler için geçiş işlem sunucusunu izlemeye iş.</span><span class="sxs-lookup"><span data-stu-id="b77db-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="b77db-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b77db-111">Example 2</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="b77db-112">Çoğaltmanın korumalı öğesini kaynaktan hedef işlem sunucusuna geçirilmiş şekilde işleyen işleme sunucusu</span><span class="sxs-lookup"><span data-stu-id="b77db-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="b77db-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b77db-113">PARAMETERS</span></span>

### <span data-ttu-id="b77db-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b77db-114">-DefaultProfile</span></span>
<span data-ttu-id="b77db-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b77db-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b77db-116">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="b77db-116">-Fabric</span></span>
<span data-ttu-id="b77db-117">Yapılandırma sunucusuna karşılık gelen site kurtarma yapısı.</span><span class="sxs-lookup"><span data-stu-id="b77db-117">Site recovery fabric corresponding to the Configuration Server.</span></span>

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

### <span data-ttu-id="b77db-118">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="b77db-118">-ReplicationProtectedItem</span></span>
<span data-ttu-id="b77db-119">İşlemleri sunucusu değiştirilmiş çoğaltma korumalı öğesi listesi.</span><span class="sxs-lookup"><span data-stu-id="b77db-119">List of replication protected item whose process server to be switched.</span></span>

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

### <span data-ttu-id="b77db-120">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="b77db-120">-SourceProcessServer</span></span>
<span data-ttu-id="b77db-121">Çoğaltmayı dışarı geçirmek için Işlem sunucusu.</span><span class="sxs-lookup"><span data-stu-id="b77db-121">The Process server to switch replication out from.</span></span>

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

### <span data-ttu-id="b77db-122">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="b77db-122">-TargetProcessServer</span></span>
<span data-ttu-id="b77db-123">Çoğaltmaya geçiş yapmak için Process Server.</span><span class="sxs-lookup"><span data-stu-id="b77db-123">The Process server to switch replication to.</span></span>

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

### <span data-ttu-id="b77db-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="b77db-124">-Confirm</span></span>
<span data-ttu-id="b77db-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b77db-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b77db-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b77db-126">-WhatIf</span></span>
<span data-ttu-id="b77db-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b77db-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b77db-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b77db-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b77db-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b77db-129">CommonParameters</span></span>
<span data-ttu-id="b77db-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b77db-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b77db-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b77db-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b77db-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b77db-132">INPUTS</span></span>

### <span data-ttu-id="b77db-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b77db-133">None</span></span>

## <span data-ttu-id="b77db-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b77db-134">OUTPUTS</span></span>

### <span data-ttu-id="b77db-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b77db-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b77db-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b77db-136">NOTES</span></span>

## <span data-ttu-id="b77db-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b77db-137">RELATED LINKS</span></span>
