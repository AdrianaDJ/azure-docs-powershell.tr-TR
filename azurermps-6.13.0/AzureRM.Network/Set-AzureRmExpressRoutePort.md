---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRoutePort.md
ms.openlocfilehash: 46f73d2a58fe5f1109de6a15a5cb39e3b568a4b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592282"
---
# <span data-ttu-id="6ebe7-101">Set-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="6ebe7-101">Set-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="6ebe7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ebe7-102">SYNOPSIS</span></span>
<span data-ttu-id="6ebe7-103">ExpressRoutePort değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6ebe7-103">Modifies an ExpressRoutePort.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ebe7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ebe7-104">SYNTAX</span></span>

```
Set-AzureRmExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ebe7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ebe7-105">DESCRIPTION</span></span>
<span data-ttu-id="6ebe7-106">**Set-AzureRmExpressRoutePort** cmdlet 'ı değiştirilmiş Expressrouteport öğesini Azure 'a kaydeder.</span><span class="sxs-lookup"><span data-stu-id="6ebe7-106">The **Set-AzureRmExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="6ebe7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ebe7-107">EXAMPLES</span></span>

### <span data-ttu-id="6ebe7-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6ebe7-108">Example 1</span></span>
```powershell
$erport = Get-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzureRmExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="6ebe7-109">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6ebe7-109">Example 2</span></span>
```powershell
$erport = Get-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzureRmExpressRoutePort -InputObject $erport
```

<span data-ttu-id="6ebe7-110">ExpressRoutePort bağlantısının yönetim durumunu değiştirir</span><span class="sxs-lookup"><span data-stu-id="6ebe7-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

## <span data-ttu-id="6ebe7-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ebe7-111">PARAMETERS</span></span>

### <span data-ttu-id="6ebe7-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="6ebe7-112">-AsJob</span></span>
<span data-ttu-id="6ebe7-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6ebe7-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ebe7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ebe7-114">-DefaultProfile</span></span>
<span data-ttu-id="6ebe7-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6ebe7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ebe7-116">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="6ebe7-116">-ExpressRoutePort</span></span>
<span data-ttu-id="6ebe7-117">ExpressRoutePort nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6ebe7-117">The ExpressRoutePort object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ebe7-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="6ebe7-118">-Confirm</span></span>
<span data-ttu-id="6ebe7-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6ebe7-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ebe7-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ebe7-120">-WhatIf</span></span>
<span data-ttu-id="6ebe7-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6ebe7-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ebe7-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6ebe7-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ebe7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ebe7-123">CommonParameters</span></span>
<span data-ttu-id="6ebe7-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ebe7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ebe7-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ebe7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ebe7-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ebe7-126">INPUTS</span></span>

### <span data-ttu-id="6ebe7-127">Microsoft. Azure. Commands. Network. model. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="6ebe7-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="6ebe7-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ebe7-128">OUTPUTS</span></span>

### <span data-ttu-id="6ebe7-129">Microsoft. Azure. Commands. Network. model. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="6ebe7-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="6ebe7-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ebe7-130">NOTES</span></span>

## <span data-ttu-id="6ebe7-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ebe7-131">RELATED LINKS</span></span>
