---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
ms.openlocfilehash: 07a29a17a1a7c17a0bbf7b202b019e7d833a5050
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265897"
---
# <span data-ttu-id="3e3eb-101">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3e3eb-101">Set-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="3e3eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e3eb-102">SYNOPSIS</span></span>
<span data-ttu-id="3e3eb-103">Değiştirilmiş bir Azure SecurityPartnerProvider kaydeder.</span><span class="sxs-lookup"><span data-stu-id="3e3eb-103">Saves a modified Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="3e3eb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3e3eb-104">SYNTAX</span></span>

```
Set-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e3eb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3e3eb-105">DESCRIPTION</span></span>
<span data-ttu-id="3e3eb-106">**Set-AzSecurityPartnerProvider** cmdlet 'i, bir Azure securitypartnersağlayıcısını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="3e3eb-106">The **Set-AzSecurityPartnerProvider** cmdlet updates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="3e3eb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3e3eb-107">EXAMPLES</span></span>

### <span data-ttu-id="3e3eb-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3e3eb-108">Example 1</span></span>
```powershell
$securityPartnerProvider = Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
Set-AzSecurityPartnerProvider -SecurityPartnerProvider $securityPartnerProvider
```


## <span data-ttu-id="3e3eb-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3e3eb-109">PARAMETERS</span></span>

### <span data-ttu-id="3e3eb-110">-Iş</span><span class="sxs-lookup"><span data-stu-id="3e3eb-110">-AsJob</span></span>
<span data-ttu-id="3e3eb-111">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3e3eb-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e3eb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e3eb-112">-DefaultProfile</span></span>
<span data-ttu-id="3e3eb-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3e3eb-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e3eb-114">-Securitypartnersağlayıcı</span><span class="sxs-lookup"><span data-stu-id="3e3eb-114">-SecurityPartnerProvider</span></span>
<span data-ttu-id="3e3eb-115">Securitypartnersağlayıcı</span><span class="sxs-lookup"><span data-stu-id="3e3eb-115">The SecurityPartnerProvider</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e3eb-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="3e3eb-116">-Confirm</span></span>
<span data-ttu-id="3e3eb-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3e3eb-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e3eb-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e3eb-118">-WhatIf</span></span>
<span data-ttu-id="3e3eb-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3e3eb-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e3eb-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3e3eb-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e3eb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e3eb-121">CommonParameters</span></span>
<span data-ttu-id="3e3eb-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3e3eb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e3eb-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3e3eb-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e3eb-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3e3eb-124">INPUTS</span></span>

### <span data-ttu-id="3e3eb-125">Microsoft. Azure. Commands. Network. model. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3e3eb-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="3e3eb-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3e3eb-126">OUTPUTS</span></span>

### <span data-ttu-id="3e3eb-127">Microsoft. Azure. Commands. Network. model. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3e3eb-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="3e3eb-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3e3eb-128">NOTES</span></span>

## <span data-ttu-id="3e3eb-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3e3eb-129">RELATED LINKS</span></span>
