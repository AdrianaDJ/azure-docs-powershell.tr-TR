---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: BDEA3F9D-AC23-402D-BA1F-AC617C7480A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverynetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 481d2d414cde32e9d0b99cedd5b942b7bed9b248
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593381"
---
# <span data-ttu-id="28ad6-101">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="28ad6-101">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="28ad6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28ad6-102">SYNOPSIS</span></span>
<span data-ttu-id="28ad6-103">Geçerli site kurtarma kasasından Ağ eşlemesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="28ad6-103">Removes a network mapping from the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28ad6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="28ad6-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28ad6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="28ad6-105">DESCRIPTION</span></span>
<span data-ttu-id="28ad6-106">**Remove-AzureRMSiteRecoveryNetworkMapping** cmdlet 'i, geçerli Azure Site Recovery kasasından bir ağ eşlemesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="28ad6-106">The **Remove-AzureRMSiteRecoveryNetworkMapping** cmdlet removes a network mapping from the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="28ad6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="28ad6-107">EXAMPLES</span></span>

## <span data-ttu-id="28ad6-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="28ad6-108">PARAMETERS</span></span>

### <span data-ttu-id="28ad6-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28ad6-109">-DefaultProfile</span></span>
<span data-ttu-id="28ad6-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="28ad6-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28ad6-111">-NetworkMapping</span><span class="sxs-lookup"><span data-stu-id="28ad6-111">-NetworkMapping</span></span>
<span data-ttu-id="28ad6-112">Ağ eşleme nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="28ad6-112">Specifies the network mapping object.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28ad6-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28ad6-113">CommonParameters</span></span>
<span data-ttu-id="28ad6-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="28ad6-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28ad6-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28ad6-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28ad6-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="28ad6-116">INPUTS</span></span>

### <span data-ttu-id="28ad6-117">ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="28ad6-117">ASRNetworkMapping</span></span>
<span data-ttu-id="28ad6-118">' NetworkMapping ' parametresi ardışık düzenin ' ASRNetworkMapping ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="28ad6-118">Parameter 'NetworkMapping' accepts value of type 'ASRNetworkMapping' from the pipeline</span></span>

## <span data-ttu-id="28ad6-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="28ad6-119">OUTPUTS</span></span>

### <span data-ttu-id="28ad6-120">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="28ad6-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="28ad6-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="28ad6-121">NOTES</span></span>

## <span data-ttu-id="28ad6-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="28ad6-122">RELATED LINKS</span></span>

[<span data-ttu-id="28ad6-123">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="28ad6-123">Get-AzureRmSiteRecoveryNetworkMapping</span></span>](./Get-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="28ad6-124">New-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="28ad6-124">New-AzureRmSiteRecoveryNetworkMapping</span></span>](./New-AzureRmSiteRecoveryNetworkMapping.md)
