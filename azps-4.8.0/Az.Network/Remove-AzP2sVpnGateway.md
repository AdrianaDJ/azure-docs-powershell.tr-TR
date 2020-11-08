---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
ms.openlocfilehash: 704a8e0164361c338ac182eef3bf09758eec363b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265921"
---
# <span data-ttu-id="2625d-101">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2625d-101">Remove-AzP2sVpnGateway</span></span>

## <span data-ttu-id="2625d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2625d-102">SYNOPSIS</span></span>
<span data-ttu-id="2625d-103">Var olan bir P2SVpnGateway kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2625d-103">Removes an existing P2SVpnGateway.</span></span>

## <span data-ttu-id="2625d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2625d-104">SYNTAX</span></span>

### <span data-ttu-id="2625d-105">ByP2SVpnGatewayName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2625d-105">ByP2SVpnGatewayName (Default)</span></span>
```
Remove-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2625d-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="2625d-106">ByP2SVpnGatewayObject</span></span>
```
Remove-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2625d-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="2625d-107">ByP2SVpnGatewayResourceId</span></span>
```
Remove-AzP2sVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2625d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2625d-108">DESCRIPTION</span></span>
<span data-ttu-id="2625d-109">**Remove-AzP2sVpnGateway** cmdlet 'ı virtualhub altındaki mevcut bir P2SVpnGateway kaldırmanıza imkan verir.</span><span class="sxs-lookup"><span data-stu-id="2625d-109">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span> <span data-ttu-id="2625d-110">P2SVpnGateway kaldırıldıktan sonra tüm site istemcileri için bağlantı başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="2625d-110">All the point to site clients connectivity will fail after P2SVpnGateway is removed.</span></span>

## <span data-ttu-id="2625d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2625d-111">EXAMPLES</span></span>

### <span data-ttu-id="2625d-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2625d-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzP2sVpnGateway -Name 683482ade8564515aed4b8448c9757ea-westus-gw-ResourceGroupName P2SCortexGATesting -Force -PassThru
```

<span data-ttu-id="2625d-113">**Remove-AzP2sVpnGateway** cmdlet 'ı virtualhub altındaki mevcut bir P2SVpnGateway kaldırmanıza imkan verir.</span><span class="sxs-lookup"><span data-stu-id="2625d-113">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="2625d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2625d-114">PARAMETERS</span></span>

### <span data-ttu-id="2625d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2625d-115">-DefaultProfile</span></span>
<span data-ttu-id="2625d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2625d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2625d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2625d-117">-Force</span></span>
<span data-ttu-id="2625d-118">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="2625d-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2625d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2625d-119">-InputObject</span></span>
<span data-ttu-id="2625d-120">Silinecek p2sVpnGateway nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2625d-120">The p2sVpnGateway object to be deleted.</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2625d-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="2625d-121">-Name</span></span>
<span data-ttu-id="2625d-122">P2SVpnGateway adı.</span><span class="sxs-lookup"><span data-stu-id="2625d-122">The P2SVpnGateway name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName, P2SVpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2625d-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2625d-123">-PassThru</span></span>
<span data-ttu-id="2625d-124">Bu işlemin gerçekleştirildiği öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="2625d-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="2625d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2625d-125">-ResourceGroupName</span></span>
<span data-ttu-id="2625d-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2625d-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2625d-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2625d-127">-ResourceId</span></span>
<span data-ttu-id="2625d-128">Silinecek p2sVpnGateway için Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="2625d-128">The Azure resource ID for the p2sVpnGateway to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases: p2sVpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2625d-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="2625d-129">-Confirm</span></span>
<span data-ttu-id="2625d-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2625d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2625d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2625d-131">-WhatIf</span></span>
<span data-ttu-id="2625d-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2625d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2625d-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2625d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2625d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2625d-134">CommonParameters</span></span>
<span data-ttu-id="2625d-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2625d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2625d-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2625d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2625d-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2625d-137">INPUTS</span></span>

### <span data-ttu-id="2625d-138">Microsoft. Azure. Commands. Network. modeller. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2625d-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="2625d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2625d-139">System.String</span></span>

## <span data-ttu-id="2625d-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2625d-140">OUTPUTS</span></span>

### <span data-ttu-id="2625d-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2625d-141">System.Boolean</span></span>

## <span data-ttu-id="2625d-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2625d-142">NOTES</span></span>

## <span data-ttu-id="2625d-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2625d-143">RELATED LINKS</span></span>
