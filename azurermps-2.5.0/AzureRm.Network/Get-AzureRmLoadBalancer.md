---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancer
schema: 2.0.0
ms.openlocfilehash: 39bbf3a30f4334e35f58109da86b9b07208682af
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939329"
---
# <span data-ttu-id="f382a-101">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f382a-101">Get-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="f382a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f382a-102">SYNOPSIS</span></span>
<span data-ttu-id="f382a-103">Bir yük dengeleyici alır.</span><span class="sxs-lookup"><span data-stu-id="f382a-103">Gets a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f382a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f382a-104">SYNTAX</span></span>

### <span data-ttu-id="f382a-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="f382a-105">NoExpand</span></span>
```
Get-AzureRmLoadBalancer [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f382a-106">Geniþ</span><span class="sxs-lookup"><span data-stu-id="f382a-106">Expand</span></span>
```
Get-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f382a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f382a-107">DESCRIPTION</span></span>
<span data-ttu-id="f382a-108">**Get-AzureRmLoadBalancer** cmdlet 'i, kaynak grubunda yer alan bir veya birden çok Azure Yük dengeleyicmasını alır.</span><span class="sxs-lookup"><span data-stu-id="f382a-108">The **Get-AzureRmLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="f382a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f382a-109">EXAMPLES</span></span>

### <span data-ttu-id="f382a-110">Örnek 1: yük dengeleyici alma</span><span class="sxs-lookup"><span data-stu-id="f382a-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="f382a-111">Bu komut MyLoadBalancer adındaki yük dengeleyiciden alır.</span><span class="sxs-lookup"><span data-stu-id="f382a-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="f382a-112">Bu cmdlet 'i çalıştırabilmeniz için bir yük dengeleyici var olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f382a-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="f382a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f382a-113">PARAMETERS</span></span>

### <span data-ttu-id="f382a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f382a-114">-DefaultProfile</span></span>
<span data-ttu-id="f382a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f382a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f382a-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="f382a-116">-ExpandResource</span></span>
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

### <span data-ttu-id="f382a-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="f382a-117">-Name</span></span>
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

### <span data-ttu-id="f382a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f382a-118">-ResourceGroupName</span></span>
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

### <span data-ttu-id="f382a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f382a-119">CommonParameters</span></span>
<span data-ttu-id="f382a-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f382a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f382a-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f382a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f382a-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f382a-122">INPUTS</span></span>

## <span data-ttu-id="f382a-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f382a-123">OUTPUTS</span></span>

### <span data-ttu-id="f382a-124">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f382a-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f382a-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f382a-125">NOTES</span></span>

## <span data-ttu-id="f382a-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f382a-126">RELATED LINKS</span></span>

[<span data-ttu-id="f382a-127">Yeni-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f382a-127">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="f382a-128">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f382a-128">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="f382a-129">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f382a-129">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


