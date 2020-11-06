---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 9c336602aebdb82e4860ee744fb99f3a6fbf5a98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587463"
---
# <span data-ttu-id="2b9c3-101">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="2b9c3-101">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="2b9c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b9c3-102">SYNOPSIS</span></span>
<span data-ttu-id="2b9c3-103">Çoğaltma yeniden eşitlemeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-103">Starts replication resynchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b9c3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2b9c3-104">SYNTAX</span></span>

### <span data-ttu-id="2b9c3-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2b9c3-105">Default (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b9c3-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="2b9c3-106">ByResourceId</span></span>
```
Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b9c3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2b9c3-107">DESCRIPTION</span></span>
<span data-ttu-id="2b9c3-108">Protected **-AzureRmRecoveryServicesAsrResynchronizeReplicationJob** cmdlet 'i, korumalı bir eşitleme gerekli durumundaysa, belirtilen korumalı öğe için çoğaltmanın yeniden eşitlenmesi başlatır.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-108">The **Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="2b9c3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2b9c3-109">EXAMPLES</span></span>

### <span data-ttu-id="2b9c3-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2b9c3-110">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="2b9c3-111">Geçirilen çoğaltma korumalı öğesindeki çoğaltmayı yeniden eşitlemek için işi başlatır.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="2b9c3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2b9c3-112">PARAMETERS</span></span>

### <span data-ttu-id="2b9c3-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="2b9c3-113">-Confirm</span></span>
<span data-ttu-id="2b9c3-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b9c3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b9c3-115">-DefaultProfile</span></span>
<span data-ttu-id="2b9c3-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b9c3-117">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="2b9c3-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="2b9c3-118">Çoğaltmayı yeniden eşitlemek için ASR çoğaltması korumalı öğe.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-118">ASR replication protected item to resynchronize replication for.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b9c3-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2b9c3-119">-ResourceId</span></span>
<span data-ttu-id="2b9c3-120">Yeniden eşitlemek için çoğaltma korumalı öğenin kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-120">Resource Id of replication protected item to resynchronize.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b9c3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b9c3-121">-WhatIf</span></span>
<span data-ttu-id="2b9c3-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b9c3-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b9c3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b9c3-124">CommonParameters</span></span>
<span data-ttu-id="2b9c3-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b9c3-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b9c3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b9c3-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2b9c3-127">INPUTS</span></span>

### <span data-ttu-id="2b9c3-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="2b9c3-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="2b9c3-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2b9c3-129">OUTPUTS</span></span>

### <span data-ttu-id="2b9c3-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2b9c3-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2b9c3-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2b9c3-131">NOTES</span></span>

## <span data-ttu-id="2b9c3-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2b9c3-132">RELATED LINKS</span></span>
