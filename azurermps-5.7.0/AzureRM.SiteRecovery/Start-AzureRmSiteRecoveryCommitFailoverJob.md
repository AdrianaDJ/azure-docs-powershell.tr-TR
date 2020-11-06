---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 9FF78BE6-FF24-47E9-9F36-48E426097F45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoverycommitfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryCommitFailoverJob.md
ms.openlocfilehash: 839855b9b56e4ecc73552af310af7221c9b7b2d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593371"
---
# <span data-ttu-id="25168-101">Start-AzureRmSiteRecoveryCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="25168-101">Start-AzureRmSiteRecoveryCommitFailoverJob</span></span>

## <span data-ttu-id="25168-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25168-102">SYNOPSIS</span></span>
<span data-ttu-id="25168-103">Site kurtarma nesnesi için yük devretmeyi Yürüt eylemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="25168-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25168-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="25168-104">SYNTAX</span></span>

### <span data-ttu-id="25168-105">ByRPIObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="25168-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25168-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="25168-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25168-107">Btypeınfo</span><span class="sxs-lookup"><span data-stu-id="25168-107">ByPEObject</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -ProtectionEntity <ASRProtectionEntity>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25168-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="25168-108">DESCRIPTION</span></span>
<span data-ttu-id="25168-109">**Start-AzureRmSiteRecoveryCommitFailoverJob** cmdlet 'ı bir Azure Site Recovery nesnesi için yük devretme işlemi tamamlandıktan sonra işlemi tamamlama işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="25168-109">The **Start-AzureRmSiteRecoveryCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="25168-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="25168-110">EXAMPLES</span></span>

## <span data-ttu-id="25168-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="25168-111">PARAMETERS</span></span>

### <span data-ttu-id="25168-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25168-112">-DefaultProfile</span></span>
<span data-ttu-id="25168-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="25168-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25168-114">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="25168-114">-ProtectionEntity</span></span>
<span data-ttu-id="25168-115">Site Recovery koruması varlık nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="25168-115">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25168-116">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="25168-116">-RecoveryPlan</span></span>
<span data-ttu-id="25168-117">Kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="25168-117">Specifies a recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25168-118">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="25168-118">-ReplicationProtectedItem</span></span>
```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25168-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25168-119">CommonParameters</span></span>
<span data-ttu-id="25168-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="25168-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25168-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25168-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25168-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="25168-122">INPUTS</span></span>

### <span data-ttu-id="25168-123">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="25168-123">ASRProtectionEntity</span></span>
<span data-ttu-id="25168-124">' ProtectionEntity ' parametresi ardışık düzenin ' ASRProtectionEntity ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="25168-124">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="25168-125">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="25168-125">ASRRecoveryPlan</span></span>
<span data-ttu-id="25168-126">' RecoveryPlan ' parametresi ardışık düzenin ' ASRRecoveryPlan ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="25168-126">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="25168-127">Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="25168-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="25168-128">' Replicationkorunabilir ' parametresi, ardışık düzenin ' Asrreplicationkorunabilir ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="25168-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="25168-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="25168-129">OUTPUTS</span></span>

### <span data-ttu-id="25168-130">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="25168-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="25168-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="25168-131">NOTES</span></span>

## <span data-ttu-id="25168-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="25168-132">RELATED LINKS</span></span>

