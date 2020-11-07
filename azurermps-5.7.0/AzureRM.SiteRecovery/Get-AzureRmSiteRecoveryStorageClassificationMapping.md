---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: D19488C1-9E87-4F1A-94E3-8AFDE6AFC982
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverystorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: e04f5b71fe0cc5d6872c3bdf9cd18790f4e09f7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763973"
---
# <span data-ttu-id="5f625-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="5f625-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="5f625-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f625-102">SYNOPSIS</span></span>
<span data-ttu-id="5f625-103">Site kurtarmada bir depolama sınıflandırması eşlemesi alır.</span><span class="sxs-lookup"><span data-stu-id="5f625-103">Gets a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f625-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5f625-104">SYNTAX</span></span>

### <span data-ttu-id="5f625-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5f625-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5f625-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5f625-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f625-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5f625-107">DESCRIPTION</span></span>
<span data-ttu-id="5f625-108">**Get-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet 'ı Azure Site Recovery 'de bir depolama sınıflandırması eşlemesi alır.</span><span class="sxs-lookup"><span data-stu-id="5f625-108">The **Get-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet gets a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="5f625-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5f625-109">EXAMPLES</span></span>

## <span data-ttu-id="5f625-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5f625-110">PARAMETERS</span></span>

### <span data-ttu-id="5f625-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f625-111">-DefaultProfile</span></span>
<span data-ttu-id="5f625-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5f625-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f625-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="5f625-113">-Name</span></span>
<span data-ttu-id="5f625-114">Bu cmdlet 'in aldığı depolama sınıflandırması eşlemesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5f625-114">Specifies the name of the storage classification mapping that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5f625-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f625-115">CommonParameters</span></span>
<span data-ttu-id="5f625-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5f625-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f625-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f625-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f625-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5f625-118">INPUTS</span></span>

### <span data-ttu-id="5f625-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5f625-119">None</span></span>
<span data-ttu-id="5f625-120">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="5f625-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5f625-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5f625-121">OUTPUTS</span></span>

### <span data-ttu-id="5f625-122">System. Koleksiyonlar. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. Asrstorageclassıficationmapping]</span><span class="sxs-lookup"><span data-stu-id="5f625-122">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassificationMapping]</span></span>

## <span data-ttu-id="5f625-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5f625-123">NOTES</span></span>

## <span data-ttu-id="5f625-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5f625-124">RELATED LINKS</span></span>

[<span data-ttu-id="5f625-125">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="5f625-125">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="5f625-126">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="5f625-126">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)
