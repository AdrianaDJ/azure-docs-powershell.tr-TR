---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azo365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
ms.openlocfilehash: 2aeb26447c5684b57d966c403a256fe3d1361a41
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323776"
---
# <span data-ttu-id="ec35a-101">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="ec35a-101">New-AzO365PolicyProperty</span></span>

## <span data-ttu-id="ec35a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec35a-102">SYNOPSIS</span></span>
<span data-ttu-id="ec35a-103">Office 365 trafik ayırıcı ilke nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ec35a-103">Create an office 365 traffic breakout policy object.</span></span>

## <span data-ttu-id="ec35a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec35a-104">SYNTAX</span></span>

```
New-AzO365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec35a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec35a-105">DESCRIPTION</span></span>
<span data-ttu-id="ec35a-106">New-AzVpnSite ve Update-AzVpnSite cmdlet 'leriyle kullanılmak üzere Office 365 ayırıcı ilkesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ec35a-106">Create an office 365 breakout policy to be used with New-AzVpnSite and Update-AzVpnSite cmdlets.</span></span>
## <span data-ttu-id="ec35a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec35a-107">EXAMPLES</span></span>

### <span data-ttu-id="ec35a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ec35a-108">Example 1</span></span>
```powershell
PS C:\> $policy = New-AzO365PolicyProperty -Allow -Optimize
```

<span data-ttu-id="ec35a-109">Trafik için izin ver ve İyileştir için izin verilen bir Office 365 trafiği ilkesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ec35a-109">Create an office 365 traffic breakout policy with breakout allowed for allow and optimize category of traffic.</span></span>

## <span data-ttu-id="ec35a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec35a-110">PARAMETERS</span></span>

### <span data-ttu-id="ec35a-111">-İzin ver</span><span class="sxs-lookup"><span data-stu-id="ec35a-111">-Allow</span></span>
<span data-ttu-id="ec35a-112">Kategori trafiğine izin ver 'i işaretleme.</span><span class="sxs-lookup"><span data-stu-id="ec35a-112">Breakout the allow category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec35a-113">-Varsayılan</span><span class="sxs-lookup"><span data-stu-id="ec35a-113">-Default</span></span>
<span data-ttu-id="ec35a-114">Varsayılan kategori trafiğini ayırıcılar.</span><span class="sxs-lookup"><span data-stu-id="ec35a-114">Breakout the default category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec35a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec35a-115">-DefaultProfile</span></span>
<span data-ttu-id="ec35a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ec35a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec35a-117">-İyileştir</span><span class="sxs-lookup"><span data-stu-id="ec35a-117">-Optimize</span></span>
<span data-ttu-id="ec35a-118">En İyileştir kategorisi trafiğini ayırıcılar.</span><span class="sxs-lookup"><span data-stu-id="ec35a-118">Breakout the optimize category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec35a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec35a-119">CommonParameters</span></span>
<span data-ttu-id="ec35a-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec35a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec35a-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ec35a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec35a-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec35a-122">INPUTS</span></span>

### <span data-ttu-id="ec35a-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ec35a-123">None</span></span>

## <span data-ttu-id="ec35a-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec35a-124">OUTPUTS</span></span>

### <span data-ttu-id="ec35a-125">Microsoft. Azure. Commands. Network. modeller. PSO365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="ec35a-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span></span>

## <span data-ttu-id="ec35a-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec35a-126">NOTES</span></span>

## <span data-ttu-id="ec35a-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec35a-127">RELATED LINKS</span></span>
