---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: fe1182f165e347b312288d56604fddad6bad68da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760015"
---
# <span data-ttu-id="7767a-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7767a-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="7767a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7767a-102">SYNOPSIS</span></span>
<span data-ttu-id="7767a-103">ExpressRoutePort değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7767a-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="7767a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7767a-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7767a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7767a-105">DESCRIPTION</span></span>
<span data-ttu-id="7767a-106">**Set-AzExpressRoutePort** cmdlet 'ı değiştirilmiş Expressrouteport öğesini Azure 'a kaydeder.</span><span class="sxs-lookup"><span data-stu-id="7767a-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="7767a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7767a-107">EXAMPLES</span></span>

### <span data-ttu-id="7767a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7767a-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="7767a-109">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7767a-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="7767a-110">ExpressRoutePort bağlantısının yönetim durumunu değiştirir</span><span class="sxs-lookup"><span data-stu-id="7767a-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

## <span data-ttu-id="7767a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7767a-111">PARAMETERS</span></span>

### <span data-ttu-id="7767a-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="7767a-112">-AsJob</span></span>
<span data-ttu-id="7767a-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7767a-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7767a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7767a-114">-DefaultProfile</span></span>
<span data-ttu-id="7767a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7767a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7767a-116">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7767a-116">-ExpressRoutePort</span></span>
<span data-ttu-id="7767a-117">ExpressRoutePort nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7767a-117">The ExpressRoutePort object.</span></span>

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

### <span data-ttu-id="7767a-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="7767a-118">-Confirm</span></span>
<span data-ttu-id="7767a-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7767a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7767a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7767a-120">-WhatIf</span></span>
<span data-ttu-id="7767a-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7767a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7767a-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7767a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7767a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7767a-123">CommonParameters</span></span>
<span data-ttu-id="7767a-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7767a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7767a-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7767a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7767a-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7767a-126">INPUTS</span></span>

### <span data-ttu-id="7767a-127">Microsoft. Azure. Commands. Network. model. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7767a-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="7767a-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7767a-128">OUTPUTS</span></span>

### <span data-ttu-id="7767a-129">Microsoft. Azure. Commands. Network. model. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7767a-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="7767a-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7767a-130">NOTES</span></span>

## <span data-ttu-id="7767a-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7767a-131">RELATED LINKS</span></span>

[<span data-ttu-id="7767a-132">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7767a-132">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="7767a-133">Yeni-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7767a-133">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="7767a-134">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7767a-134">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)