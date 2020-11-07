---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 96a170d302d66ed2fa27d2cd7bdb17fc23cefcd3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760643"
---
# <span data-ttu-id="50598-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="50598-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="50598-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50598-102">SYNOPSIS</span></span>
<span data-ttu-id="50598-103">Uygulama ağ geçidine atanan kimliği alma.</span><span class="sxs-lookup"><span data-stu-id="50598-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="50598-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="50598-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50598-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="50598-105">DESCRIPTION</span></span>
<span data-ttu-id="50598-106">**Get-Azapplicationgatewayıdentity** cmdlet 'i uygulama ağ geçidine atanan kimliği alır.</span><span class="sxs-lookup"><span data-stu-id="50598-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="50598-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="50598-107">EXAMPLES</span></span>

### <span data-ttu-id="50598-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="50598-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="50598-109">Bu örneklerde uygulama ağ geçidinden uygulama ağ geçidi kimliği nasıl alınır.</span><span class="sxs-lookup"><span data-stu-id="50598-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="50598-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="50598-110">PARAMETERS</span></span>

### <span data-ttu-id="50598-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="50598-111">-ApplicationGateway</span></span>
<span data-ttu-id="50598-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="50598-112">The applicationGateway</span></span>

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

### <span data-ttu-id="50598-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50598-113">-DefaultProfile</span></span>
<span data-ttu-id="50598-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="50598-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50598-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50598-115">CommonParameters</span></span>
<span data-ttu-id="50598-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="50598-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50598-117">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="50598-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50598-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="50598-118">INPUTS</span></span>

### <span data-ttu-id="50598-119">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="50598-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="50598-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="50598-120">OUTPUTS</span></span>

### <span data-ttu-id="50598-121">Microsoft. Azure. Commands. Network. model. Psmanagedserviceıdentity</span><span class="sxs-lookup"><span data-stu-id="50598-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="50598-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="50598-122">NOTES</span></span>

## <span data-ttu-id="50598-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="50598-123">RELATED LINKS</span></span>
