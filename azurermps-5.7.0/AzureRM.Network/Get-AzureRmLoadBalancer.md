---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
ms.openlocfilehash: b57d228ca6b31f84797baa7b2b41073edfa6c3ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588188"
---
# <span data-ttu-id="40ed8-101">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="40ed8-101">Get-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="40ed8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="40ed8-103">Bir yük dengeleyici alır.</span><span class="sxs-lookup"><span data-stu-id="40ed8-103">Gets a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40ed8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="40ed8-104">SYNTAX</span></span>

### <span data-ttu-id="40ed8-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="40ed8-105">NoExpand</span></span>
```
Get-AzureRmLoadBalancer [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40ed8-106">Geniþ</span><span class="sxs-lookup"><span data-stu-id="40ed8-106">Expand</span></span>
```
Get-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40ed8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="40ed8-107">DESCRIPTION</span></span>
<span data-ttu-id="40ed8-108">**Get-AzureRmLoadBalancer** cmdlet 'i, kaynak grubunda yer alan bir veya birden çok Azure Yük dengeleyicmasını alır.</span><span class="sxs-lookup"><span data-stu-id="40ed8-108">The **Get-AzureRmLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="40ed8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="40ed8-109">EXAMPLES</span></span>

### <span data-ttu-id="40ed8-110">Örnek 1: yük dengeleyici alma</span><span class="sxs-lookup"><span data-stu-id="40ed8-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="40ed8-111">Bu komut MyLoadBalancer adındaki yük dengeleyiciden alır.</span><span class="sxs-lookup"><span data-stu-id="40ed8-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="40ed8-112">Bu cmdlet 'i çalıştırabilmeniz için bir yük dengeleyici var olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="40ed8-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="40ed8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="40ed8-113">PARAMETERS</span></span>

### <span data-ttu-id="40ed8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40ed8-114">-DefaultProfile</span></span>
<span data-ttu-id="40ed8-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="40ed8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40ed8-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="40ed8-116">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40ed8-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="40ed8-117">-Name</span></span>
```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40ed8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40ed8-118">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40ed8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40ed8-119">CommonParameters</span></span>
<span data-ttu-id="40ed8-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="40ed8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40ed8-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40ed8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40ed8-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="40ed8-122">INPUTS</span></span>

### <span data-ttu-id="40ed8-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="40ed8-123">None</span></span>
<span data-ttu-id="40ed8-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="40ed8-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="40ed8-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="40ed8-125">OUTPUTS</span></span>

### <span data-ttu-id="40ed8-126">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="40ed8-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="40ed8-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="40ed8-127">NOTES</span></span>

## <span data-ttu-id="40ed8-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="40ed8-128">RELATED LINKS</span></span>

[<span data-ttu-id="40ed8-129">Yeni-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="40ed8-129">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="40ed8-130">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="40ed8-130">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="40ed8-131">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="40ed8-131">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


