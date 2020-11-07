---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: f5f0ce9768226c79210db3a38c5c09303e94a852
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935543"
---
# <span data-ttu-id="c3d21-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c3d21-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="c3d21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3d21-102">SYNOPSIS</span></span>
<span data-ttu-id="c3d21-103">Bir yük dengeleyici alır.</span><span class="sxs-lookup"><span data-stu-id="c3d21-103">Gets a load balancer.</span></span>

## <span data-ttu-id="c3d21-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c3d21-104">SYNTAX</span></span>

### <span data-ttu-id="c3d21-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="c3d21-105">NoExpand</span></span>
```
Get-AzLoadBalancer [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3d21-106">Geniþ</span><span class="sxs-lookup"><span data-stu-id="c3d21-106">Expand</span></span>
```
Get-AzLoadBalancer -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3d21-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c3d21-107">DESCRIPTION</span></span>
<span data-ttu-id="c3d21-108">**Get-AzLoadBalancer** cmdlet 'i, kaynak grubunda yer alan bir veya birden çok Azure yük dengeleyici alır.</span><span class="sxs-lookup"><span data-stu-id="c3d21-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="c3d21-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c3d21-109">EXAMPLES</span></span>

### <span data-ttu-id="c3d21-110">Örnek 1: yük dengeleyici alma</span><span class="sxs-lookup"><span data-stu-id="c3d21-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="c3d21-111">Bu komut MyLoadBalancer adındaki yük dengeleyiciden alır.</span><span class="sxs-lookup"><span data-stu-id="c3d21-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="c3d21-112">Bu cmdlet 'i çalıştırabilmeniz için bir yük dengeleyici var olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c3d21-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="c3d21-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c3d21-113">PARAMETERS</span></span>

### <span data-ttu-id="c3d21-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3d21-114">-DefaultProfile</span></span>
<span data-ttu-id="c3d21-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c3d21-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3d21-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="c3d21-116">-ExpandResource</span></span>
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

### <span data-ttu-id="c3d21-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="c3d21-117">-Name</span></span>
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

### <span data-ttu-id="c3d21-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3d21-118">-ResourceGroupName</span></span>
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

### <span data-ttu-id="c3d21-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3d21-119">CommonParameters</span></span>
<span data-ttu-id="c3d21-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c3d21-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3d21-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3d21-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3d21-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c3d21-122">INPUTS</span></span>

## <span data-ttu-id="c3d21-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c3d21-123">OUTPUTS</span></span>

### <span data-ttu-id="c3d21-124">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c3d21-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c3d21-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c3d21-125">NOTES</span></span>

## <span data-ttu-id="c3d21-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c3d21-126">RELATED LINKS</span></span>

[<span data-ttu-id="c3d21-127">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c3d21-127">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="c3d21-128">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c3d21-128">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="c3d21-129">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c3d21-129">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


