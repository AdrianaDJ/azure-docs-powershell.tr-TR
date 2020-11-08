---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
ms.openlocfilehash: 2d78e7136fe42187cbabc2345e2ad2314af1d9c5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277595"
---
# <span data-ttu-id="45c71-101">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="45c71-101">Set-AzIpGroup</span></span>

## <span data-ttu-id="45c71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45c71-102">SYNOPSIS</span></span>
<span data-ttu-id="45c71-103">Değiştirilmiş Güvenlik duvarını kaydeder.</span><span class="sxs-lookup"><span data-stu-id="45c71-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="45c71-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="45c71-104">SYNTAX</span></span>

```
Set-AzIpGroup -IpGroup <PSIpGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45c71-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="45c71-105">DESCRIPTION</span></span>
<span data-ttu-id="45c71-106">**Set-Azıpgroup** cmdlet 'ı bir Azure ıpgroup 'u güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="45c71-106">The **Set-AzIpGroup** cmdlet updates an Azure IpGroup</span></span>

## <span data-ttu-id="45c71-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="45c71-107">EXAMPLES</span></span>

### <span data-ttu-id="45c71-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="45c71-108">Example 1</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
$ipGroup.IpAddresses.Add("11.11.0.0/24")
Set-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="45c71-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="45c71-109">PARAMETERS</span></span>

### <span data-ttu-id="45c71-110">-Iş</span><span class="sxs-lookup"><span data-stu-id="45c71-110">-AsJob</span></span>
<span data-ttu-id="45c71-111">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="45c71-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c71-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45c71-112">-DefaultProfile</span></span>
<span data-ttu-id="45c71-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="45c71-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c71-114">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="45c71-114">-IpGroup</span></span>
<span data-ttu-id="45c71-115">Ipgroup</span><span class="sxs-lookup"><span data-stu-id="45c71-115">The IpGroup</span></span>

```yaml
Type: PSIpGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45c71-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="45c71-116">-Confirm</span></span>
<span data-ttu-id="45c71-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="45c71-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c71-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45c71-118">-WhatIf</span></span>
<span data-ttu-id="45c71-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="45c71-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45c71-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="45c71-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c71-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45c71-121">CommonParameters</span></span>
<span data-ttu-id="45c71-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="45c71-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45c71-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="45c71-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45c71-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="45c71-124">INPUTS</span></span>

### <span data-ttu-id="45c71-125">Microsoft. Azure. Commands. Network. model. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="45c71-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="45c71-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="45c71-126">OUTPUTS</span></span>

### <span data-ttu-id="45c71-127">Microsoft. Azure. Commands. Network. model. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="45c71-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="45c71-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="45c71-128">NOTES</span></span>

## <span data-ttu-id="45c71-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="45c71-129">RELATED LINKS</span></span>
