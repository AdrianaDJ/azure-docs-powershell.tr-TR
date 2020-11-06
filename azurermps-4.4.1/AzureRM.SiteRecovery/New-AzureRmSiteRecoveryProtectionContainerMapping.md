---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 11CE6244-D287-4B99-9585-E3EA2D36A4F9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 44addca6ee4f658f4cc6f8081e0f7a0c39ba4a58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592545"
---
# <span data-ttu-id="d5e70-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d5e70-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="d5e70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5e70-102">SYNOPSIS</span></span>
<span data-ttu-id="d5e70-103">Bir ilkeyi bir koruma kapsayıcısına ilişkilendirerek Azure Site Recovery koruma kapsayıcısı eşlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d5e70-103">Creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5e70-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d5e70-104">SYNTAX</span></span>

### <span data-ttu-id="d5e70-105">EnterpriseToAzure (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d5e70-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d5e70-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="d5e70-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5e70-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d5e70-107">DESCRIPTION</span></span>
<span data-ttu-id="d5e70-108">**New-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet 'i bir Ilkeyi bir koruma kapsayıcısına Ilişkilendirerek bir Azure Site Recovery koruma kapsayıcısı eşlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d5e70-108">The **New-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

## <span data-ttu-id="d5e70-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d5e70-109">EXAMPLES</span></span>

## <span data-ttu-id="d5e70-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d5e70-110">PARAMETERS</span></span>

### <span data-ttu-id="d5e70-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="d5e70-111">-Name</span></span>
<span data-ttu-id="d5e70-112">Koruma kapsayıcısı eşlemesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5e70-112">Specifies the name of the Protection Container mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5e70-113">-İlke</span><span class="sxs-lookup"><span data-stu-id="d5e70-113">-Policy</span></span>
<span data-ttu-id="d5e70-114">Azure Site Recovery Ilke nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5e70-114">Specifies the Azure Site Recovery Policy object.</span></span>

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

### <span data-ttu-id="d5e70-115">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d5e70-115">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="d5e70-116">Birincil koruma kapsayıcısı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5e70-116">Specifies the primary Protection Container object.</span></span>

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

### <span data-ttu-id="d5e70-117">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d5e70-117">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="d5e70-118">Kurtarma koruması kapsayıcısı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5e70-118">Specifies the Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="d5e70-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5e70-119">-DefaultProfile</span></span>
<span data-ttu-id="d5e70-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d5e70-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5e70-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5e70-121">CommonParameters</span></span>
<span data-ttu-id="d5e70-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d5e70-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5e70-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5e70-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5e70-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d5e70-124">INPUTS</span></span>

### <span data-ttu-id="d5e70-125">Asrilkesi</span><span class="sxs-lookup"><span data-stu-id="d5e70-125">ASRPolicy</span></span>
<span data-ttu-id="d5e70-126">Parametre ' Ilke ', ardışık düzenin ' ASRPolicy ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d5e70-126">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="d5e70-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d5e70-127">OUTPUTS</span></span>

### <span data-ttu-id="d5e70-128">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d5e70-128">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d5e70-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d5e70-129">NOTES</span></span>

## <span data-ttu-id="d5e70-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d5e70-130">RELATED LINKS</span></span>

[<span data-ttu-id="d5e70-131">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d5e70-131">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="d5e70-132">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d5e70-132">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Remove-AzureRmSiteRecoveryProtectionContainerMapping.md)
