---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
ms.openlocfilehash: c4bc5e9fcc7d0ca405a8031af29d16283f963ad2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278261"
---
# <span data-ttu-id="5e167-101">New-AzFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5e167-101">New-AzFirewallPublicIpAddress</span></span>

## <span data-ttu-id="5e167-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e167-102">SYNOPSIS</span></span>
<span data-ttu-id="5e167-103">Bu, Azure Güvenlik duvarında Çoklu nokta için kullanılabilecek IP adresi yer tutucudur.</span><span class="sxs-lookup"><span data-stu-id="5e167-103">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="5e167-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e167-104">SYNTAX</span></span>

```
New-AzFirewallPublicIpAddress [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e167-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e167-105">DESCRIPTION</span></span>
<span data-ttu-id="5e167-106">Bu, Azure Güvenlik duvarında Çoklu nokta için kullanılabilecek IP adresi yer tutucudur.</span><span class="sxs-lookup"><span data-stu-id="5e167-106">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="5e167-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e167-107">EXAMPLES</span></span>

### <span data-ttu-id="5e167-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5e167-108">Example 1</span></span>
```powershell
PS C:\> $publicIp = New-AzFirewallPublicIpAddress -Address 20.2.3.4
```

<span data-ttu-id="5e167-109">$publicIp, IP adresi için yer tutucu 20.2.3.4</span><span class="sxs-lookup"><span data-stu-id="5e167-109">$publicIp will be the placeholder for the ip address 20.2.3.4</span></span>

## <span data-ttu-id="5e167-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e167-110">PARAMETERS</span></span>

### <span data-ttu-id="5e167-111">-Adres</span><span class="sxs-lookup"><span data-stu-id="5e167-111">-Address</span></span>
<span data-ttu-id="5e167-112">Hub 'a bağlı güvenlik duvarının IP adresleri</span><span class="sxs-lookup"><span data-stu-id="5e167-112">The IP Addresses of the Firewall attached to a hub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e167-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e167-113">-DefaultProfile</span></span>
<span data-ttu-id="5e167-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5e167-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e167-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="5e167-115">-Confirm</span></span>
<span data-ttu-id="5e167-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5e167-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e167-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e167-117">-WhatIf</span></span>
<span data-ttu-id="5e167-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5e167-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e167-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5e167-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e167-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e167-120">CommonParameters</span></span>
<span data-ttu-id="5e167-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e167-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e167-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5e167-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e167-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e167-123">INPUTS</span></span>

### <span data-ttu-id="5e167-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5e167-124">None</span></span>

## <span data-ttu-id="5e167-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e167-125">OUTPUTS</span></span>

### <span data-ttu-id="5e167-126">Microsoft. Azure. Commands. Network. model. Psazurefirewallpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="5e167-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span></span>

## <span data-ttu-id="5e167-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e167-127">NOTES</span></span>

## <span data-ttu-id="5e167-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e167-128">RELATED LINKS</span></span>
