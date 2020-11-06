---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkUsageList.md
ms.openlocfilehash: 618fdf2ebe32f365bce72353f6e148fa3059cf66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595148"
---
# <span data-ttu-id="618e9-101">Get-AzureRmVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="618e9-101">Get-AzureRmVirtualNetworkUsageList</span></span>

## <span data-ttu-id="618e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="618e9-102">SYNOPSIS</span></span>
<span data-ttu-id="618e9-103">Sanal ağ geçerli kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="618e9-103">Gets virtual network current usage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="618e9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="618e9-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="618e9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="618e9-105">DESCRIPTION</span></span>
<span data-ttu-id="618e9-106">**Get-AzureRmVirtualNetworkUsageList** cmdlet 'i belirtilen sanal ağın alt ağ kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="618e9-106">The **Get-AzureRmVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="618e9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="618e9-107">EXAMPLES</span></span>

### <span data-ttu-id="618e9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="618e9-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Get-AzureRmVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet
CurrentValue : 1
Limit        : 65531
Unit         : Count

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet11
CurrentValue : 0
Limit        : 251
Unit         : Count
```

<span data-ttu-id="618e9-109">Usage test sanal ağı için alt ağ başına geçerli değer değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="618e9-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="618e9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="618e9-110">PARAMETERS</span></span>

### <span data-ttu-id="618e9-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="618e9-111">-Name</span></span>
<span data-ttu-id="618e9-112">Kullanımları gösterilecek sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="618e9-112">Specifies the name of the virtual network to show usages for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="618e9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="618e9-113">-ResourceGroupName</span></span>
<span data-ttu-id="618e9-114">Sanal ağın ait olduğu kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="618e9-114">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="618e9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="618e9-115">-DefaultProfile</span></span>
<span data-ttu-id="618e9-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="618e9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="618e9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="618e9-117">CommonParameters</span></span>
<span data-ttu-id="618e9-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="618e9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="618e9-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="618e9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="618e9-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="618e9-120">INPUTS</span></span>

### <span data-ttu-id="618e9-121">System. String</span><span class="sxs-lookup"><span data-stu-id="618e9-121">System.String</span></span>

## <span data-ttu-id="618e9-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="618e9-122">OUTPUTS</span></span>

### <span data-ttu-id="618e9-123">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="618e9-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="618e9-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="618e9-124">NOTES</span></span>

## <span data-ttu-id="618e9-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="618e9-125">RELATED LINKS</span></span>

