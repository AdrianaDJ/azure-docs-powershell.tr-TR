---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: be16ff2145a4442861fd985dfbb55da63f010e94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587458"
---
# <span data-ttu-id="864e4-101">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="864e4-101">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="864e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="864e4-102">SYNOPSIS</span></span>
<span data-ttu-id="864e4-103">Yük Dengelemesi için bir Process sunucusundan diğerine çoğaltmayı değiştirin.</span><span class="sxs-lookup"><span data-stu-id="864e4-103">Switch replication from one Process server to another for load balancing.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="864e4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="864e4-104">SYNTAX</span></span>

```
Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric>
 -SourceProcessServer <ASRProcessServer> -TargetProcessServer <ASRProcessServer>
 [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="864e4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="864e4-105">DESCRIPTION</span></span>
<span data-ttu-id="864e4-106">**Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob** belirtilen sanal makineler için çoğaltma veri hareketini veya belirtilen bir işlem sunucusunu belirtilen hedef işlem sunucusuna geçirir.</span><span class="sxs-lookup"><span data-stu-id="864e4-106">The **Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="864e4-107">Yük Dengeleme veya süreç sunucuları arasında çoğaltmayı değiştirme için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="864e4-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="864e4-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="864e4-108">EXAMPLES</span></span>

### <span data-ttu-id="864e4-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="864e4-109">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="864e4-110">Kaynaktan hedef işlem sunucusuna olan tüm çoğaltma korumalı öğeler için geçiş işlem sunucusunu izlemeye iş.</span><span class="sxs-lookup"><span data-stu-id="864e4-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="864e4-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="864e4-111">Example 2</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="864e4-112">Çoğaltmanın korumalı öğesini kaynaktan hedef işlem sunucusuna geçirilmiş şekilde işleyen işleme sunucusu</span><span class="sxs-lookup"><span data-stu-id="864e4-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="864e4-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="864e4-113">PARAMETERS</span></span>

### <span data-ttu-id="864e4-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="864e4-114">-Confirm</span></span>
<span data-ttu-id="864e4-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="864e4-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="864e4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="864e4-116">-DefaultProfile</span></span>
<span data-ttu-id="864e4-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="864e4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="864e4-118">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="864e4-118">-Fabric</span></span>
<span data-ttu-id="864e4-119">Yapılandırma sunucusuna karşılık gelen site kurtarma yapısı.</span><span class="sxs-lookup"><span data-stu-id="864e4-119">Site recovery fabric corresponding to the Configuration Server.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: ConfigServer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="864e4-120">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="864e4-120">-ReplicationProtectedItem</span></span>
<span data-ttu-id="864e4-121">İşlemleri sunucusu değiştirilmiş çoğaltma korumalı öğesi listesi.</span><span class="sxs-lookup"><span data-stu-id="864e4-121">List of replication protected item whose process server to be switched.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: (All)
Aliases: ReplicatedItem

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="864e4-122">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="864e4-122">-SourceProcessServer</span></span>
<span data-ttu-id="864e4-123">Çoğaltmayı dışarı geçirmek için Işlem sunucusu.</span><span class="sxs-lookup"><span data-stu-id="864e4-123">The Process server to switch replication out from.</span></span>

```yaml
Type: ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="864e4-124">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="864e4-124">-TargetProcessServer</span></span>
<span data-ttu-id="864e4-125">Çoğaltmaya geçiş yapmak için Process Server.</span><span class="sxs-lookup"><span data-stu-id="864e4-125">The Process server to switch replication to.</span></span>

```yaml
Type: ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="864e4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="864e4-126">-WhatIf</span></span>
<span data-ttu-id="864e4-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="864e4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="864e4-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="864e4-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="864e4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="864e4-129">CommonParameters</span></span>
<span data-ttu-id="864e4-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="864e4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="864e4-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="864e4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="864e4-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="864e4-132">INPUTS</span></span>

### <span data-ttu-id="864e4-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="864e4-133">None</span></span>

## <span data-ttu-id="864e4-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="864e4-134">OUTPUTS</span></span>

### <span data-ttu-id="864e4-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="864e4-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="864e4-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="864e4-136">NOTES</span></span>

## <span data-ttu-id="864e4-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="864e4-137">RELATED LINKS</span></span>
