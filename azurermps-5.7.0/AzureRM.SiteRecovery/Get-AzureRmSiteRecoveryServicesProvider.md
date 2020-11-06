---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: EB68FC6B-310F-41DB-B870-B907147F8513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 4e65636c732ede20487df0b80973172977c6c832
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593400"
---
# <span data-ttu-id="a12cc-101">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a12cc-101">Get-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="a12cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a12cc-102">SYNOPSIS</span></span>
<span data-ttu-id="a12cc-103">Kasadaki Azure Site Recovery sağlayıcılarından bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="a12cc-103">Gets information on the Azure Site Recovery providers in the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a12cc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a12cc-104">SYNTAX</span></span>

### <span data-ttu-id="a12cc-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a12cc-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a12cc-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a12cc-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a12cc-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="a12cc-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a12cc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a12cc-108">DESCRIPTION</span></span>
<span data-ttu-id="a12cc-109">**Get-AzureRmSiteRecoveryServicesProvider** cmdlet 'i, kasadaki Azure Site Recovery sağlayıcılarından bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="a12cc-109">The **Get-AzureRmSiteRecoveryServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="a12cc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a12cc-110">EXAMPLES</span></span>

## <span data-ttu-id="a12cc-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a12cc-111">PARAMETERS</span></span>

### <span data-ttu-id="a12cc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a12cc-112">-DefaultProfile</span></span>
<span data-ttu-id="a12cc-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a12cc-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a12cc-114">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="a12cc-114">-Fabric</span></span>
<span data-ttu-id="a12cc-115">Azure Site Recovery Fabric nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a12cc-115">Specifies the Azure Site Recovery Fabric object.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a12cc-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a12cc-116">-FriendlyName</span></span>
<span data-ttu-id="a12cc-117">Bu cmdlet 'in aldığı Azure Site Recovery sağlayıcısının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a12cc-117">Specifies the friendly name of the Azure Site Recovery Provider that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a12cc-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="a12cc-118">-Name</span></span>
<span data-ttu-id="a12cc-119">Bu cmdlet 'in aldığı Azure Site Recovery sağlayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a12cc-119">Specifies the name of the Azure Site Recovery Provider that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a12cc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a12cc-120">CommonParameters</span></span>
<span data-ttu-id="a12cc-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a12cc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a12cc-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a12cc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a12cc-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a12cc-123">INPUTS</span></span>

### <span data-ttu-id="a12cc-124">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="a12cc-124">ASRFabric</span></span>
<span data-ttu-id="a12cc-125">Parametre ' Fabric ', ardışık düzenin ' ASRFabric ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="a12cc-125">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="a12cc-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a12cc-126">OUTPUTS</span></span>

### <span data-ttu-id="a12cc-127">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRRecoveryServicesProvider, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a12cc-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a12cc-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a12cc-128">NOTES</span></span>

## <span data-ttu-id="a12cc-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a12cc-129">RELATED LINKS</span></span>

[<span data-ttu-id="a12cc-130">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a12cc-130">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="a12cc-131">Güncelleştirme-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a12cc-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)
