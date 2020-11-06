---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: A8C7BA18-4C67-46BA-9CCE-FC22E41465AE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
ms.openlocfilehash: 6103e9a820a80df7e89130f269296cd073283947
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589056"
---
# <span data-ttu-id="aecee-101">Update-AzureRmSiteRecoveryProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="aecee-101">Update-AzureRmSiteRecoveryProtectionDirection</span></span>

## <span data-ttu-id="aecee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aecee-102">SYNOPSIS</span></span>
<span data-ttu-id="aecee-103">Site kurtarma nesnesinin korunması için kaynak ve hedef sunucuyu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="aecee-103">Updates the source and target server for the protection of a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aecee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aecee-104">SYNTAX</span></span>

### <span data-ttu-id="aecee-105">Btypeınfo (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="aecee-105">ByPEObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aecee-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="aecee-106">ByRPObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aecee-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="aecee-107">ByRPIObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aecee-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="aecee-108">DESCRIPTION</span></span>
<span data-ttu-id="aecee-109">**Update-AzureRmSiteRecoveryProtectionDirection** cmdlet 'i, bir Azure Site Recovery nesnesi yürütme işlemi tamamlama işlemi tamamlandıktan sonra kaynak ve hedef sunucuyu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="aecee-109">The **Update-AzureRmSiteRecoveryProtectionDirection** cmdlet updates the source and target server for the protection of an Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="aecee-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aecee-110">EXAMPLES</span></span>

## <span data-ttu-id="aecee-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aecee-111">PARAMETERS</span></span>

### <span data-ttu-id="aecee-112">-Yön</span><span class="sxs-lookup"><span data-stu-id="aecee-112">-Direction</span></span>
<span data-ttu-id="aecee-113">Kaydetmenin yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="aecee-113">Specifies the direction of the commit.</span></span>
<span data-ttu-id="aecee-114">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="aecee-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aecee-115">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="aecee-115">PrimaryToRecovery</span></span>
- <span data-ttu-id="aecee-116">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="aecee-116">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aecee-117">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="aecee-117">-ProtectionEntity</span></span>
<span data-ttu-id="aecee-118">Koruma varlık nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aecee-118">Specifies the protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aecee-119">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="aecee-119">-RecoveryPlan</span></span>
<span data-ttu-id="aecee-120">Kurtarma planı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aecee-120">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aecee-121">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="aecee-121">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aecee-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aecee-122">-DefaultProfile</span></span>
<span data-ttu-id="aecee-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aecee-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aecee-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aecee-124">CommonParameters</span></span>
<span data-ttu-id="aecee-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aecee-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aecee-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aecee-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aecee-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aecee-127">INPUTS</span></span>

### <span data-ttu-id="aecee-128">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="aecee-128">ASRProtectionEntity</span></span>
<span data-ttu-id="aecee-129">' ProtectionEntity ' parametresi ardışık düzenin ' ASRProtectionEntity ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="aecee-129">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="aecee-130">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="aecee-130">ASRRecoveryPlan</span></span>
<span data-ttu-id="aecee-131">' RecoveryPlan ' parametresi ardışık düzenin ' ASRRecoveryPlan ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="aecee-131">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="aecee-132">Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="aecee-132">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="aecee-133">' Replicationkorunabilir ' parametresi, ardışık düzenin ' Asrreplicationkorunabilir ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="aecee-133">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="aecee-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aecee-134">OUTPUTS</span></span>

### <span data-ttu-id="aecee-135">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="aecee-135">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="aecee-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aecee-136">NOTES</span></span>

## <span data-ttu-id="aecee-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aecee-137">RELATED LINKS</span></span>

