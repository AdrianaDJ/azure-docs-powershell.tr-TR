---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: 490e61142bdbc0bcdd64f18aeeb2fa527e5180b9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935481"
---
# <span data-ttu-id="6d529-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6d529-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="6d529-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d529-102">SYNOPSIS</span></span>
<span data-ttu-id="6d529-103">Sanal ağ geçidi alır</span><span class="sxs-lookup"><span data-stu-id="6d529-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="6d529-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6d529-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d529-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6d529-105">DESCRIPTION</span></span>
<span data-ttu-id="6d529-106">Sanal ağ geçidi, Azure 'daki ağ geçidini temsil eden nesnedir.</span><span class="sxs-lookup"><span data-stu-id="6d529-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="6d529-107">**Get-AzVirtualNetworkGateway** cmdlet 'ı, ad ve kaynak grubu adına dayalı olarak Azure 'daki ağ geçidinizin nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="6d529-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="6d529-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6d529-108">EXAMPLES</span></span>

### <span data-ttu-id="6d529-109">1: sanal ağ geçidi alın</span><span class="sxs-lookup"><span data-stu-id="6d529-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="6d529-110">Sanal ağ geçidinin "myRG" adlı sanal ağ geçidinin nesnesini, "myRG"</span><span class="sxs-lookup"><span data-stu-id="6d529-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="6d529-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6d529-111">PARAMETERS</span></span>

### <span data-ttu-id="6d529-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d529-112">-DefaultProfile</span></span>
<span data-ttu-id="6d529-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6d529-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d529-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="6d529-114">-Name</span></span>
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

### <span data-ttu-id="6d529-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d529-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="6d529-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d529-116">CommonParameters</span></span>
<span data-ttu-id="6d529-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6d529-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d529-118">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d529-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d529-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6d529-119">INPUTS</span></span>

## <span data-ttu-id="6d529-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6d529-120">OUTPUTS</span></span>

### <span data-ttu-id="6d529-121">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6d529-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="6d529-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6d529-122">NOTES</span></span>

## <span data-ttu-id="6d529-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6d529-123">RELATED LINKS</span></span>

