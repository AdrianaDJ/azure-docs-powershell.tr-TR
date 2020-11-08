---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
ms.openlocfilehash: d701e563e05f33b3cb0ed99a2e62fbcd54935987
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278092"
---
# <span data-ttu-id="5e648-101">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e648-101">Set-AzApplicationGateway</span></span>

## <span data-ttu-id="5e648-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e648-102">SYNOPSIS</span></span>
<span data-ttu-id="5e648-103">Uygulama ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5e648-103">Updates an application gateway.</span></span>

## <span data-ttu-id="5e648-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e648-104">SYNTAX</span></span>

```
Set-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e648-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e648-105">DESCRIPTION</span></span>
<span data-ttu-id="5e648-106">**Set-AzApplicationGateway** cmdlet 'ı bir Azure Application Gateway 'i güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5e648-106">The **Set-AzApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="5e648-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e648-107">EXAMPLES</span></span>

### <span data-ttu-id="5e648-108">Örnek 1: uygulama ağ geçidini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="5e648-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name Test -ResourceGroupName Appgwtest
PS C:\>$AppGw.Tag = @{"key"="value"}
PS C:\>$UpdatedAppGw = Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="5e648-109">Bu komutlar, uygulama ağ geçidini $AppGw değişkeninde ayarlarla güncelleştirir ve güncelleştirilmiş ağ geçidini $UpdatedAppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5e648-109">These commands update the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="5e648-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e648-110">PARAMETERS</span></span>

### <span data-ttu-id="5e648-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e648-111">-ApplicationGateway</span></span>
<span data-ttu-id="5e648-112">Uygulama ağ geçidinin ayarlanması gereken durumu temsil eden bir uygulama ağ geçidi nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e648-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e648-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="5e648-113">-AsJob</span></span>
<span data-ttu-id="5e648-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="5e648-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e648-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e648-115">-DefaultProfile</span></span>
<span data-ttu-id="5e648-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5e648-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e648-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e648-117">CommonParameters</span></span>
<span data-ttu-id="5e648-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e648-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e648-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5e648-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e648-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e648-120">INPUTS</span></span>

### <span data-ttu-id="5e648-121">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e648-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5e648-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e648-122">OUTPUTS</span></span>

### <span data-ttu-id="5e648-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e648-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5e648-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e648-124">NOTES</span></span>

## <span data-ttu-id="5e648-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e648-125">RELATED LINKS</span></span>

[<span data-ttu-id="5e648-126">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e648-126">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


