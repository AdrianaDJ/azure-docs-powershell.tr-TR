---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 22ace3fb8c2b6b8f620a90cc2f53533ba4a42ff5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760209"
---
# <span data-ttu-id="2f597-101">Remove-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="2f597-101">Remove-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="2f597-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f597-102">SYNOPSIS</span></span>
<span data-ttu-id="2f597-103">Uygulama ağ geçidinden kimlik kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2f597-103">Removes a identity from an application gateway.</span></span>

## <span data-ttu-id="2f597-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2f597-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f597-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2f597-105">DESCRIPTION</span></span>
<span data-ttu-id="2f597-106">**Remove-Azapplicationgatewayıdentity** cmdlet 'i uygulama ağ geçidinden kimliği kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2f597-106">**Remove-AzApplicationGatewayIdentity** cmdlet removes identity from an application gateway.</span></span>

## <span data-ttu-id="2f597-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2f597-107">EXAMPLES</span></span>

### <span data-ttu-id="2f597-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2f597-108">Example 1</span></span>
```powershell
PS C:\> $appgw = Remove-AzApplicationGatewayIdentity -ApplicationGateway $appgw
PS C:\> $updatedgateway = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="2f597-109">Bu örnekte, kimliği varolan bir uygulama ağ geçidinden kaldırdık.</span><span class="sxs-lookup"><span data-stu-id="2f597-109">In this example, we remove identity from an existing application gateway.</span></span>
<span data-ttu-id="2f597-110">Not: ağ geçidi bir keykasa gizliliğine başvuruyorsa, bu işlem boyunca bu SSL sertifikası başvurularını kaldırmak da önemlidir.</span><span class="sxs-lookup"><span data-stu-id="2f597-110">Note: If the gateway is referencing a keyvault secret, then it is also important to remove those ssl certificate references along this operation.</span></span>

## <span data-ttu-id="2f597-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2f597-111">PARAMETERS</span></span>

### <span data-ttu-id="2f597-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2f597-112">-ApplicationGateway</span></span>
<span data-ttu-id="2f597-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2f597-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f597-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f597-114">-DefaultProfile</span></span>
<span data-ttu-id="2f597-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2f597-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f597-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="2f597-116">-Confirm</span></span>
<span data-ttu-id="2f597-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2f597-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f597-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f597-118">-WhatIf</span></span>
<span data-ttu-id="2f597-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2f597-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f597-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2f597-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f597-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f597-121">CommonParameters</span></span>
<span data-ttu-id="2f597-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2f597-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f597-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f597-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f597-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2f597-124">INPUTS</span></span>

### <span data-ttu-id="2f597-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2f597-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2f597-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2f597-126">OUTPUTS</span></span>

### <span data-ttu-id="2f597-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2f597-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2f597-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2f597-128">NOTES</span></span>

## <span data-ttu-id="2f597-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2f597-129">RELATED LINKS</span></span>
