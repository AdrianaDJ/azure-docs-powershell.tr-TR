---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 11CE6244-D287-4B99-9585-E3EA2D36A4F9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 950c5c8e2007568add1aba1122356de670884c07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593388"
---
# <span data-ttu-id="0e096-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="0e096-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="0e096-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e096-102">SYNOPSIS</span></span>
<span data-ttu-id="0e096-103">Bir ilkeyi bir koruma kapsayıcısına ilişkilendirerek Azure Site Recovery koruma kapsayıcısı eşlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0e096-103">Creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e096-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0e096-104">SYNTAX</span></span>

### <span data-ttu-id="0e096-105">EnterpriseToAzure (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0e096-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e096-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="0e096-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e096-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0e096-107">DESCRIPTION</span></span>
<span data-ttu-id="0e096-108">**New-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet 'i bir Ilkeyi bir koruma kapsayıcısına Ilişkilendirerek bir Azure Site Recovery koruma kapsayıcısı eşlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0e096-108">The **New-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

## <span data-ttu-id="0e096-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0e096-109">EXAMPLES</span></span>

## <span data-ttu-id="0e096-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0e096-110">PARAMETERS</span></span>

### <span data-ttu-id="0e096-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e096-111">-DefaultProfile</span></span>
<span data-ttu-id="0e096-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0e096-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e096-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="0e096-113">-Name</span></span>
<span data-ttu-id="0e096-114">Koruma kapsayıcısı eşlemesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e096-114">Specifies the name of the Protection Container mapping.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e096-115">-İlke</span><span class="sxs-lookup"><span data-stu-id="0e096-115">-Policy</span></span>
<span data-ttu-id="0e096-116">Azure Site Recovery Ilke nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e096-116">Specifies the Azure Site Recovery Policy object.</span></span>

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

### <span data-ttu-id="0e096-117">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0e096-117">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="0e096-118">Birincil koruma kapsayıcısı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e096-118">Specifies the primary Protection Container object.</span></span>

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

### <span data-ttu-id="0e096-119">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0e096-119">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="0e096-120">Kurtarma koruması kapsayıcısı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e096-120">Specifies the Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="0e096-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e096-121">CommonParameters</span></span>
<span data-ttu-id="0e096-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0e096-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e096-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e096-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e096-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0e096-124">INPUTS</span></span>

### <span data-ttu-id="0e096-125">Asrilkesi</span><span class="sxs-lookup"><span data-stu-id="0e096-125">ASRPolicy</span></span>
<span data-ttu-id="0e096-126">Parametre ' Ilke ', ardışık düzenin ' ASRPolicy ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="0e096-126">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="0e096-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0e096-127">OUTPUTS</span></span>

### <span data-ttu-id="0e096-128">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0e096-128">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0e096-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0e096-129">NOTES</span></span>

## <span data-ttu-id="0e096-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0e096-130">RELATED LINKS</span></span>

[<span data-ttu-id="0e096-131">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="0e096-131">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="0e096-132">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="0e096-132">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Remove-AzureRmSiteRecoveryProtectionContainerMapping.md)
