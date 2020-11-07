---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 0429976c64ed6e7989208c28fea1ee0a008436c8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938205"
---
# <span data-ttu-id="27cb7-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="27cb7-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="27cb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27cb7-102">SYNOPSIS</span></span>
<span data-ttu-id="27cb7-103">Çoğaltma yeniden eşitlemeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="27cb7-103">Starts replication resynchronization.</span></span>

## <span data-ttu-id="27cb7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="27cb7-104">SYNTAX</span></span>

### <span data-ttu-id="27cb7-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="27cb7-105">Default (Default)</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27cb7-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="27cb7-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27cb7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="27cb7-107">DESCRIPTION</span></span>
<span data-ttu-id="27cb7-108">Protected **-AzRecoveryServicesAsrResynchronizeReplicationJob** cmdlet 'i, korumalı bir eşitleme gerekli durumundaysa, belirtilen korumalı öğe için çoğaltmanın yeniden eşitlenmesi başlatır.</span><span class="sxs-lookup"><span data-stu-id="27cb7-108">The **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="27cb7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="27cb7-109">EXAMPLES</span></span>

### <span data-ttu-id="27cb7-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="27cb7-110">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="27cb7-111">Geçirilen çoğaltma korumalı öğesindeki çoğaltmayı yeniden eşitlemek için işi başlatır.</span><span class="sxs-lookup"><span data-stu-id="27cb7-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="27cb7-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="27cb7-112">PARAMETERS</span></span>

### <span data-ttu-id="27cb7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27cb7-113">-DefaultProfile</span></span>
<span data-ttu-id="27cb7-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="27cb7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27cb7-115">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="27cb7-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="27cb7-116">Çoğaltmayı yeniden eşitlemek için ASR çoğaltması korumalı öğe.</span><span class="sxs-lookup"><span data-stu-id="27cb7-116">ASR replication protected item to resynchronize replication for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27cb7-117">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="27cb7-117">-ResourceId</span></span>
<span data-ttu-id="27cb7-118">Yeniden eşitlemek için çoğaltma korumalı öğenin kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="27cb7-118">Resource Id of replication protected item to resynchronize.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27cb7-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="27cb7-119">-Confirm</span></span>
<span data-ttu-id="27cb7-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="27cb7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27cb7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27cb7-121">-WhatIf</span></span>
<span data-ttu-id="27cb7-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="27cb7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27cb7-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="27cb7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27cb7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27cb7-124">CommonParameters</span></span>
<span data-ttu-id="27cb7-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="27cb7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27cb7-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="27cb7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27cb7-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="27cb7-127">INPUTS</span></span>

### <span data-ttu-id="27cb7-128">System. String</span><span class="sxs-lookup"><span data-stu-id="27cb7-128">System.String</span></span>

### <span data-ttu-id="27cb7-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="27cb7-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="27cb7-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="27cb7-130">OUTPUTS</span></span>

### <span data-ttu-id="27cb7-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="27cb7-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="27cb7-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="27cb7-132">NOTES</span></span>

## <span data-ttu-id="27cb7-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="27cb7-133">RELATED LINKS</span></span>
