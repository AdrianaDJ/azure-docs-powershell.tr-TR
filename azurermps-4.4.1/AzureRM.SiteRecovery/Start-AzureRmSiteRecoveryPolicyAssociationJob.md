---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3DDC8DD8-889C-4C76-B32E-3D2C2AD0AC79
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyAssociationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyAssociationJob.md
ms.openlocfilehash: 477f31ea84c5cb3e9c06b79e1ae70f5ae8a93925
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593001"
---
# <span data-ttu-id="307a1-101">Start-AzureRmSiteRecoveryPolicyAssociationJob</span><span class="sxs-lookup"><span data-stu-id="307a1-101">Start-AzureRmSiteRecoveryPolicyAssociationJob</span></span>

## <span data-ttu-id="307a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="307a1-102">SYNOPSIS</span></span>
<span data-ttu-id="307a1-103">Site kurtarma çoğaltması ilkesi ilişki işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="307a1-103">Starts a Site Recovery replication policy association job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="307a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="307a1-104">SYNTAX</span></span>

### <span data-ttu-id="307a1-105">EnterpriseToAzure (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="307a1-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureRmSiteRecoveryPolicyAssociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="307a1-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="307a1-106">EnterpriseToEnterprise</span></span>
```
Start-AzureRmSiteRecoveryPolicyAssociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="307a1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="307a1-107">DESCRIPTION</span></span>
<span data-ttu-id="307a1-108">**Start-AzureRmSiteRecoveryPolicyAssociationJob** cmdlet 'i bir çoğaltma Ilkesini Azure Site Recovery koruma konteyneriyle ilişkilendirmek için bir ilişkilendirme işi başlatır.</span><span class="sxs-lookup"><span data-stu-id="307a1-108">The **Start-AzureRmSiteRecoveryPolicyAssociationJob** cmdlet initiates an association job to associate a replication policy with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="307a1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="307a1-109">EXAMPLES</span></span>

## <span data-ttu-id="307a1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="307a1-110">PARAMETERS</span></span>

### <span data-ttu-id="307a1-111">-İlke</span><span class="sxs-lookup"><span data-stu-id="307a1-111">-Policy</span></span>
<span data-ttu-id="307a1-112">Site kurtarma ilkesi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="307a1-112">Specifies the Site Recovery policy object.</span></span>

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

### <span data-ttu-id="307a1-113">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="307a1-113">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="307a1-114">Koruma profili ayarlarının uygulanacağı birincil koruma kapsayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="307a1-114">Specifies the primary protection container on which to apply the protection profile settings.</span></span>

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

### <span data-ttu-id="307a1-115">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="307a1-115">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="307a1-116">Koruma profili ayarlarının uygulanacağı kurtarma koruması kapsayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="307a1-116">Specifies the recovery protection container on which to apply the protection profile settings.</span></span>

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

### <span data-ttu-id="307a1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="307a1-117">-DefaultProfile</span></span>
<span data-ttu-id="307a1-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="307a1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="307a1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="307a1-119">CommonParameters</span></span>
<span data-ttu-id="307a1-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="307a1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="307a1-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="307a1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="307a1-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="307a1-122">INPUTS</span></span>

### <span data-ttu-id="307a1-123">Asrilkesi</span><span class="sxs-lookup"><span data-stu-id="307a1-123">ASRPolicy</span></span>
<span data-ttu-id="307a1-124">Parametre ' Ilke ', ardışık düzenin ' ASRPolicy ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="307a1-124">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="307a1-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="307a1-125">OUTPUTS</span></span>

### <span data-ttu-id="307a1-126">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="307a1-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="307a1-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="307a1-127">NOTES</span></span>

## <span data-ttu-id="307a1-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="307a1-128">RELATED LINKS</span></span>

