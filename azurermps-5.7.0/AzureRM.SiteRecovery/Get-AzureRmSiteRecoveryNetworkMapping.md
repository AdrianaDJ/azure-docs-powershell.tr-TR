---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 01AE09A8-B779-475A-9E86-776E0774E89E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverynetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 1e7e53d4f14649ac5cb8691a1e3d938809658771
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763989"
---
# <span data-ttu-id="fd7c5-101">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="fd7c5-101">Get-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="fd7c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd7c5-102">SYNOPSIS</span></span>
<span data-ttu-id="fd7c5-103">Geçerli kasa için site kurtarma ağ eşlemeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="fd7c5-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd7c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd7c5-104">SYNTAX</span></span>

### <span data-ttu-id="fd7c5-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fd7c5-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd7c5-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="fd7c5-106">EnterpriseToEnterprise</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd7c5-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="fd7c5-107">EnterpriseToAzure</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryFabric <ASRFabric> [-Azure]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd7c5-108">EnterpriseToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="fd7c5-108">EnterpriseToAzureLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping [-Azure] -PrimaryServer <ASRServer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd7c5-109">EnterpriseToEnterpriseLegacy</span><span class="sxs-lookup"><span data-stu-id="fd7c5-109">EnterpriseToEnterpriseLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd7c5-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd7c5-110">DESCRIPTION</span></span>
<span data-ttu-id="fd7c5-111">**Get-AzureRmSiteRecoveryNetworkMapping** cmdlet 'i, geçerli site kurtarma Kasası Için Azure Site Recovery ağ eşlemeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="fd7c5-111">The **Get-AzureRmSiteRecoveryNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the current Site Recovery vault.</span></span>

## <span data-ttu-id="fd7c5-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd7c5-112">EXAMPLES</span></span>

## <span data-ttu-id="fd7c5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd7c5-113">PARAMETERS</span></span>

### <span data-ttu-id="fd7c5-114">-Azure</span><span class="sxs-lookup"><span data-stu-id="fd7c5-114">-Azure</span></span>
<span data-ttu-id="fd7c5-115">Komutun, Azure sanal ağlarına eşlenmiş birincil sunucudaki ağlar için ağ eşlemelerinin listesini aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fd7c5-115">Indicates that the command gets a list of network mappings for networks on the primary server mapped to Azure virtual networks.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd7c5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd7c5-116">-DefaultProfile</span></span>
<span data-ttu-id="fd7c5-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fd7c5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd7c5-118">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="fd7c5-118">-PrimaryFabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd7c5-119">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="fd7c5-119">-PrimaryServer</span></span>
```yaml
Type: ASRServer
Parameter Sets: EnterpriseToAzureLegacy, EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd7c5-120">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="fd7c5-120">-RecoveryFabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd7c5-121">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="fd7c5-121">-RecoveryServer</span></span>
```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd7c5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd7c5-122">CommonParameters</span></span>
<span data-ttu-id="fd7c5-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd7c5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd7c5-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd7c5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd7c5-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd7c5-125">INPUTS</span></span>

### <span data-ttu-id="fd7c5-126">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="fd7c5-126">ASRFabric</span></span>
<span data-ttu-id="fd7c5-127">' PrimaryFabric ' parametresi ardışık düzenin ' ASRFabric ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="fd7c5-127">Parameter 'PrimaryFabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="fd7c5-128">ASRServer</span><span class="sxs-lookup"><span data-stu-id="fd7c5-128">ASRServer</span></span>
<span data-ttu-id="fd7c5-129">' PrimaryServer ' parametresi ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="fd7c5-129">Parameter 'PrimaryServer' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="fd7c5-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd7c5-130">OUTPUTS</span></span>

### <span data-ttu-id="fd7c5-131">System. Koleksiyonlar. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRNetworkMapping]</span><span class="sxs-lookup"><span data-stu-id="fd7c5-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRNetworkMapping]</span></span>

## <span data-ttu-id="fd7c5-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd7c5-132">NOTES</span></span>

## <span data-ttu-id="fd7c5-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd7c5-133">RELATED LINKS</span></span>

[<span data-ttu-id="fd7c5-134">New-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="fd7c5-134">New-AzureRmSiteRecoveryNetworkMapping</span></span>](./New-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="fd7c5-135">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="fd7c5-135">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>](./Remove-AzureRmSiteRecoveryNetworkMapping.md)
