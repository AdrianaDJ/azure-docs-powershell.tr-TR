---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4F71DC85-B2E0-4E0B-96F6-69D52C577B22
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
ms.openlocfilehash: 7dc64ea2bdbfb5dcbc648143dd094313eb765782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589060"
---
# <span data-ttu-id="ff4c8-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span><span class="sxs-lookup"><span data-stu-id="ff4c8-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span></span>

## <span data-ttu-id="ff4c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff4c8-102">SYNOPSIS</span></span>
<span data-ttu-id="ff4c8-103">Site kurtarma koruma konteyneriyle ilişkilendirilmiş bir çoğaltma ilkesinde ilişkilendirme işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="ff4c8-103">Starts a dissociation job on a replication policy associated with a Site Recovery protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff4c8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ff4c8-104">SYNTAX</span></span>

### <span data-ttu-id="ff4c8-105">EnterpriseToAzure (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ff4c8-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ff4c8-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="ff4c8-106">EnterpriseToEnterprise</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff4c8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ff4c8-107">DESCRIPTION</span></span>
<span data-ttu-id="ff4c8-108">**Start-AzureRmSiteRecoveryPolicyDissociationJob** cmdlet 'ı, Azure Site Recovery koruma kapsayıcısı ile ilişkilendirilen çoğaltma ilkesinde bir ilişkilendirme işi başlatır.</span><span class="sxs-lookup"><span data-stu-id="ff4c8-108">The **Start-AzureRmSiteRecoveryPolicyDissociationJob** cmdlet initiates a dissociation job on the replication policy associated with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="ff4c8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ff4c8-109">EXAMPLES</span></span>

## <span data-ttu-id="ff4c8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ff4c8-110">PARAMETERS</span></span>

### <span data-ttu-id="ff4c8-111">-İlke</span><span class="sxs-lookup"><span data-stu-id="ff4c8-111">-Policy</span></span>
<span data-ttu-id="ff4c8-112">Bir Azure Site kurtarma ilkesi nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="ff4c8-112">Specifies an Azure Site Recovery policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff4c8-113">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ff4c8-113">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="ff4c8-114">Birincil koruma kapsayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ff4c8-114">Specifies a primary protection container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff4c8-115">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ff4c8-115">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="ff4c8-116">Kurtarma koruma kapsayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ff4c8-116">Specifies a recovery protection container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff4c8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff4c8-117">-DefaultProfile</span></span>
<span data-ttu-id="ff4c8-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ff4c8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff4c8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff4c8-119">CommonParameters</span></span>
<span data-ttu-id="ff4c8-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ff4c8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff4c8-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff4c8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff4c8-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ff4c8-122">INPUTS</span></span>

### <span data-ttu-id="ff4c8-123">Asrilkesi</span><span class="sxs-lookup"><span data-stu-id="ff4c8-123">ASRPolicy</span></span>
<span data-ttu-id="ff4c8-124">Parametre ' Ilke ', ardışık düzenin ' ASRPolicy ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="ff4c8-124">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="ff4c8-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ff4c8-125">OUTPUTS</span></span>

### <span data-ttu-id="ff4c8-126">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ff4c8-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ff4c8-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ff4c8-127">NOTES</span></span>

## <span data-ttu-id="ff4c8-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ff4c8-128">RELATED LINKS</span></span>

