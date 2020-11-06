---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
ms.openlocfilehash: 90cafc66857ee2ec94806628b41960eaafaf6e15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590175"
---
# <span data-ttu-id="be4b8-101">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="be4b8-101">Get-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="be4b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be4b8-102">SYNOPSIS</span></span>
<span data-ttu-id="be4b8-103">Bir yük dengeleyici alır.</span><span class="sxs-lookup"><span data-stu-id="be4b8-103">Gets a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be4b8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="be4b8-104">SYNTAX</span></span>

### <span data-ttu-id="be4b8-105">NoExpand (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="be4b8-105">NoExpand (Default)</span></span>
```
Get-AzureRmLoadBalancer [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be4b8-106">Geniþ</span><span class="sxs-lookup"><span data-stu-id="be4b8-106">Expand</span></span>
```
Get-AzureRmLoadBalancer -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be4b8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="be4b8-107">DESCRIPTION</span></span>
<span data-ttu-id="be4b8-108">**Get-AzureRmLoadBalancer** cmdlet 'i, kaynak grubunda yer alan bir veya birden çok Azure Yük dengeleyicmasını alır.</span><span class="sxs-lookup"><span data-stu-id="be4b8-108">The **Get-AzureRmLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="be4b8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="be4b8-109">EXAMPLES</span></span>

### <span data-ttu-id="be4b8-110">Örnek 1: yük dengeleyici alma</span><span class="sxs-lookup"><span data-stu-id="be4b8-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="be4b8-111">Bu komut MyLoadBalancer adındaki yük dengeleyiciden alır.</span><span class="sxs-lookup"><span data-stu-id="be4b8-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="be4b8-112">Bu cmdlet 'i çalıştırabilmeniz için bir yük dengeleyici var olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="be4b8-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="be4b8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="be4b8-113">PARAMETERS</span></span>

### <span data-ttu-id="be4b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be4b8-114">-DefaultProfile</span></span>
<span data-ttu-id="be4b8-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="be4b8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be4b8-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="be4b8-116">-ExpandResource</span></span>
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

### <span data-ttu-id="be4b8-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="be4b8-117">-Name</span></span>
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

### <span data-ttu-id="be4b8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be4b8-118">-ResourceGroupName</span></span>
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

### <span data-ttu-id="be4b8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be4b8-119">CommonParameters</span></span>
<span data-ttu-id="be4b8-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="be4b8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be4b8-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be4b8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be4b8-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="be4b8-122">INPUTS</span></span>

### <span data-ttu-id="be4b8-123">System. String</span><span class="sxs-lookup"><span data-stu-id="be4b8-123">System.String</span></span>

## <span data-ttu-id="be4b8-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="be4b8-124">OUTPUTS</span></span>

### <span data-ttu-id="be4b8-125">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="be4b8-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="be4b8-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="be4b8-126">NOTES</span></span>

## <span data-ttu-id="be4b8-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="be4b8-127">RELATED LINKS</span></span>

[<span data-ttu-id="be4b8-128">Yeni-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="be4b8-128">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="be4b8-129">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="be4b8-129">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="be4b8-130">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="be4b8-130">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


