---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
ms.openlocfilehash: 764d26c2b0b95b74277fc74dab03fe55d12261f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592602"
---
# <span data-ttu-id="55d73-101">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="55d73-101">Get-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="55d73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55d73-102">SYNOPSIS</span></span>
<span data-ttu-id="55d73-103">Bir yük dengeleyici alır.</span><span class="sxs-lookup"><span data-stu-id="55d73-103">Gets a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55d73-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55d73-104">SYNTAX</span></span>

### <span data-ttu-id="55d73-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="55d73-105">NoExpand</span></span>
```
Get-AzureRmLoadBalancer [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55d73-106">Geniþ</span><span class="sxs-lookup"><span data-stu-id="55d73-106">Expand</span></span>
```
Get-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55d73-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="55d73-107">DESCRIPTION</span></span>
<span data-ttu-id="55d73-108">**Get-AzureRmLoadBalancer** cmdlet 'i, kaynak grubunda yer alan bir veya birden çok Azure Yük dengeleyicmasını alır.</span><span class="sxs-lookup"><span data-stu-id="55d73-108">The **Get-AzureRmLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="55d73-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55d73-109">EXAMPLES</span></span>

### <span data-ttu-id="55d73-110">Örnek 1: yük dengeleyici alma</span><span class="sxs-lookup"><span data-stu-id="55d73-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="55d73-111">Bu komut MyLoadBalancer adındaki yük dengeleyiciden alır.</span><span class="sxs-lookup"><span data-stu-id="55d73-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="55d73-112">Bu cmdlet 'i çalıştırabilmeniz için bir yük dengeleyici var olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="55d73-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="55d73-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55d73-113">PARAMETERS</span></span>

### <span data-ttu-id="55d73-114">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="55d73-114">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55d73-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="55d73-115">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55d73-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55d73-116">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55d73-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55d73-117">-DefaultProfile</span></span>
<span data-ttu-id="55d73-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="55d73-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55d73-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55d73-119">CommonParameters</span></span>
<span data-ttu-id="55d73-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55d73-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55d73-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55d73-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55d73-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55d73-122">INPUTS</span></span>

## <span data-ttu-id="55d73-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55d73-123">OUTPUTS</span></span>

### <span data-ttu-id="55d73-124">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="55d73-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="55d73-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55d73-125">NOTES</span></span>

## <span data-ttu-id="55d73-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55d73-126">RELATED LINKS</span></span>

[<span data-ttu-id="55d73-127">Yeni-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="55d73-127">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="55d73-128">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="55d73-128">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="55d73-129">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="55d73-129">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


