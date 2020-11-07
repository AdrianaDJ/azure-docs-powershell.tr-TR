---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 88c17626da87608a1086331289cb99f8e7668e5a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935526"
---
# <span data-ttu-id="a72e0-101">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a72e0-101">Get-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="a72e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a72e0-102">SYNOPSIS</span></span>
<span data-ttu-id="a72e0-103">Yerel ağ geçidi alır</span><span class="sxs-lookup"><span data-stu-id="a72e0-103">Gets a Local Network Gateway</span></span>

## <span data-ttu-id="a72e0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a72e0-104">SYNTAX</span></span>

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a72e0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a72e0-105">DESCRIPTION</span></span>
<span data-ttu-id="a72e0-106">Yerel ağ geçidi, VPN cihazınızı şirket Içinde temsil eden bir nesnedir.</span><span class="sxs-lookup"><span data-stu-id="a72e0-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="a72e0-107">**Get-AzLocalNetworkGateway** cmdlet 'ı, ad ve kaynak grubu adına dayalı olarak şirket içi ağ geçidinizi temsil eden nesneyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="a72e0-107">The **Get-AzLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="a72e0-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a72e0-108">EXAMPLES</span></span>

### <span data-ttu-id="a72e0-109">1: yerel ağ ağ geçidi alın</span><span class="sxs-lookup"><span data-stu-id="a72e0-109">1: Get a Local Network Gateway</span></span>
```
Get-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="a72e0-110">Yerel ağ geçidinin "myLocalGW" adlı yerel ağ geçidinin nesnesini, "myRG" kaynak grubunda döndürür</span><span class="sxs-lookup"><span data-stu-id="a72e0-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="a72e0-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a72e0-111">PARAMETERS</span></span>

### <span data-ttu-id="a72e0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a72e0-112">-DefaultProfile</span></span>
<span data-ttu-id="a72e0-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a72e0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a72e0-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="a72e0-114">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a72e0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a72e0-115">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a72e0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a72e0-116">CommonParameters</span></span>
<span data-ttu-id="a72e0-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a72e0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a72e0-118">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a72e0-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a72e0-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a72e0-119">INPUTS</span></span>

## <span data-ttu-id="a72e0-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a72e0-120">OUTPUTS</span></span>

### <span data-ttu-id="a72e0-121">Microsoft. Azure. Commands. Network. model. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a72e0-121">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="a72e0-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a72e0-122">NOTES</span></span>

## <span data-ttu-id="a72e0-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a72e0-123">RELATED LINKS</span></span>

