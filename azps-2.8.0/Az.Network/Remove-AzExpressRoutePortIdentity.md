---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
ms.openlocfilehash: c7ffb86fa56a09fb0c5bbdd41e62bf8d47bee140
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918063"
---
# <span data-ttu-id="424dc-101">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="424dc-101">Remove-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="424dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="424dc-102">SYNOPSIS</span></span>
<span data-ttu-id="424dc-103">ExpressRoutePort 'tan bir kimliği kaldırır.</span><span class="sxs-lookup"><span data-stu-id="424dc-103">Removes a identity from an ExpressRoutePort.</span></span>

## <span data-ttu-id="424dc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="424dc-104">SYNTAX</span></span>

```
Remove-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="424dc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="424dc-105">DESCRIPTION</span></span>
<span data-ttu-id="424dc-106">**Remove-AzExpressRoutePortIdentity** cmdlet 'i yerel bir Azure ExpressRoutePort nesnesinden kimliği kaldırır.</span><span class="sxs-lookup"><span data-stu-id="424dc-106">The **Remove-AzExpressRoutePortIdentity** cmdlet removes identity from a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="424dc-107">ExpressRoutePort 'tan kaldırmak için **Remove-AzExpressRoutePort** kullanın.</span><span class="sxs-lookup"><span data-stu-id="424dc-107">Use **Remove-AzExpressRoutePort** to remove it to from ExpressRoutePort.</span></span>

## <span data-ttu-id="424dc-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="424dc-108">EXAMPLES</span></span>

### <span data-ttu-id="424dc-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="424dc-109">Example 1</span></span>
```powershell
PS C:\> $expressroutePort = Remove-AzExpressRoutePortIdentity -ExpressRoutePort $expressroutePort
```

## <span data-ttu-id="424dc-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="424dc-110">PARAMETERS</span></span>

### <span data-ttu-id="424dc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="424dc-111">-DefaultProfile</span></span>
<span data-ttu-id="424dc-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="424dc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="424dc-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="424dc-113">-ExpressRoutePort</span></span>
<span data-ttu-id="424dc-114">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="424dc-114">The ExpressRoutePort</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="424dc-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="424dc-115">-Confirm</span></span>
<span data-ttu-id="424dc-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="424dc-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="424dc-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="424dc-117">-WhatIf</span></span>
<span data-ttu-id="424dc-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="424dc-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="424dc-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="424dc-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="424dc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="424dc-120">CommonParameters</span></span>
<span data-ttu-id="424dc-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="424dc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="424dc-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="424dc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>


## <span data-ttu-id="424dc-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="424dc-123">INPUTS</span></span>

### <span data-ttu-id="424dc-124">Microsoft. Azure. Commands. Network. model. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="424dc-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="424dc-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="424dc-125">OUTPUTS</span></span>

### <span data-ttu-id="424dc-126">Microsoft. Azure. Commands. Network. model. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="424dc-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="424dc-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="424dc-127">NOTES</span></span>

## <span data-ttu-id="424dc-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="424dc-128">RELATED LINKS</span></span>
[<span data-ttu-id="424dc-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="424dc-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="424dc-130">Yeni-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="424dc-130">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="424dc-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="424dc-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)
