---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3DDC8DD8-889C-4C76-B32E-3D2C2AD0AC79
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoverypolicyassociationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyAssociationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyAssociationJob.md
ms.openlocfilehash: 140bec7738d107574db5d0d157cc3f8cfac46583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763953"
---
# <span data-ttu-id="7ee64-101">Start-AzureRmSiteRecoveryPolicyAssociationJob</span><span class="sxs-lookup"><span data-stu-id="7ee64-101">Start-AzureRmSiteRecoveryPolicyAssociationJob</span></span>

## <span data-ttu-id="7ee64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ee64-102">SYNOPSIS</span></span>
<span data-ttu-id="7ee64-103">Site kurtarma çoğaltması ilkesi ilişki işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="7ee64-103">Starts a Site Recovery replication policy association job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ee64-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7ee64-104">SYNTAX</span></span>

### <span data-ttu-id="7ee64-105">EnterpriseToAzure (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7ee64-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureRmSiteRecoveryPolicyAssociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7ee64-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="7ee64-106">EnterpriseToEnterprise</span></span>
```
Start-AzureRmSiteRecoveryPolicyAssociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ee64-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7ee64-107">DESCRIPTION</span></span>
<span data-ttu-id="7ee64-108">**Start-AzureRmSiteRecoveryPolicyAssociationJob** cmdlet 'i bir çoğaltma Ilkesini Azure Site Recovery koruma konteyneriyle ilişkilendirmek için bir ilişkilendirme işi başlatır.</span><span class="sxs-lookup"><span data-stu-id="7ee64-108">The **Start-AzureRmSiteRecoveryPolicyAssociationJob** cmdlet initiates an association job to associate a replication policy with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="7ee64-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7ee64-109">EXAMPLES</span></span>

## <span data-ttu-id="7ee64-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7ee64-110">PARAMETERS</span></span>

### <span data-ttu-id="7ee64-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ee64-111">-DefaultProfile</span></span>
<span data-ttu-id="7ee64-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7ee64-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ee64-113">-İlke</span><span class="sxs-lookup"><span data-stu-id="7ee64-113">-Policy</span></span>
<span data-ttu-id="7ee64-114">Site kurtarma ilkesi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7ee64-114">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ee64-115">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7ee64-115">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="7ee64-116">Koruma profili ayarlarının uygulanacağı birincil koruma kapsayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7ee64-116">Specifies the primary protection container on which to apply the protection profile settings.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ee64-117">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7ee64-117">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="7ee64-118">Koruma profili ayarlarının uygulanacağı kurtarma koruması kapsayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7ee64-118">Specifies the recovery protection container on which to apply the protection profile settings.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ee64-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ee64-119">CommonParameters</span></span>
<span data-ttu-id="7ee64-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7ee64-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ee64-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ee64-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ee64-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7ee64-122">INPUTS</span></span>

### <span data-ttu-id="7ee64-123">Asrilkesi</span><span class="sxs-lookup"><span data-stu-id="7ee64-123">ASRPolicy</span></span>
<span data-ttu-id="7ee64-124">Parametre ' Ilke ', ardışık düzenin ' ASRPolicy ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="7ee64-124">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="7ee64-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7ee64-125">OUTPUTS</span></span>

### <span data-ttu-id="7ee64-126">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7ee64-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7ee64-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7ee64-127">NOTES</span></span>

## <span data-ttu-id="7ee64-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7ee64-128">RELATED LINKS</span></span>

