---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
ms.openlocfilehash: 704a8e0164361c338ac182eef3bf09758eec363b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104060"
---
# <span data-ttu-id="298ce-101">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="298ce-101">Remove-AzP2sVpnGateway</span></span>

## <span data-ttu-id="298ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="298ce-102">SYNOPSIS</span></span>
<span data-ttu-id="298ce-103">Var olan bir P2SVpnGateway kaldırır.</span><span class="sxs-lookup"><span data-stu-id="298ce-103">Removes an existing P2SVpnGateway.</span></span>

## <span data-ttu-id="298ce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="298ce-104">SYNTAX</span></span>

### <span data-ttu-id="298ce-105">ByP2SVpnGatewayName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="298ce-105">ByP2SVpnGatewayName (Default)</span></span>
```
Remove-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="298ce-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="298ce-106">ByP2SVpnGatewayObject</span></span>
```
Remove-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="298ce-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="298ce-107">ByP2SVpnGatewayResourceId</span></span>
```
Remove-AzP2sVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="298ce-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="298ce-108">DESCRIPTION</span></span>
<span data-ttu-id="298ce-109">**Remove-AzP2sVpnGateway** cmdlet 'ı virtualhub altındaki mevcut bir P2SVpnGateway kaldırmanıza imkan verir.</span><span class="sxs-lookup"><span data-stu-id="298ce-109">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span> <span data-ttu-id="298ce-110">P2SVpnGateway kaldırıldıktan sonra tüm site istemcileri için bağlantı başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="298ce-110">All the point to site clients connectivity will fail after P2SVpnGateway is removed.</span></span>

## <span data-ttu-id="298ce-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="298ce-111">EXAMPLES</span></span>

### <span data-ttu-id="298ce-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="298ce-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzP2sVpnGateway -Name 683482ade8564515aed4b8448c9757ea-westus-gw-ResourceGroupName P2SCortexGATesting -Force -PassThru
```

<span data-ttu-id="298ce-113">**Remove-AzP2sVpnGateway** cmdlet 'ı virtualhub altındaki mevcut bir P2SVpnGateway kaldırmanıza imkan verir.</span><span class="sxs-lookup"><span data-stu-id="298ce-113">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="298ce-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="298ce-114">PARAMETERS</span></span>

### <span data-ttu-id="298ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="298ce-115">-DefaultProfile</span></span>
<span data-ttu-id="298ce-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="298ce-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="298ce-117">-Force</span><span class="sxs-lookup"><span data-stu-id="298ce-117">-Force</span></span>
<span data-ttu-id="298ce-118">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="298ce-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="298ce-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="298ce-119">-InputObject</span></span>
<span data-ttu-id="298ce-120">Silinecek p2sVpnGateway nesnesi.</span><span class="sxs-lookup"><span data-stu-id="298ce-120">The p2sVpnGateway object to be deleted.</span></span>

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

### <span data-ttu-id="298ce-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="298ce-121">-Name</span></span>
<span data-ttu-id="298ce-122">P2SVpnGateway adı.</span><span class="sxs-lookup"><span data-stu-id="298ce-122">The P2SVpnGateway name.</span></span>

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

### <span data-ttu-id="298ce-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="298ce-123">-PassThru</span></span>
<span data-ttu-id="298ce-124">Bu işlemin gerçekleştirildiği öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="298ce-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="298ce-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="298ce-125">-ResourceGroupName</span></span>
<span data-ttu-id="298ce-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="298ce-126">The resource group name.</span></span>

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

### <span data-ttu-id="298ce-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="298ce-127">-ResourceId</span></span>
<span data-ttu-id="298ce-128">Silinecek p2sVpnGateway için Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="298ce-128">The Azure resource ID for the p2sVpnGateway to be deleted.</span></span>

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

### <span data-ttu-id="298ce-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="298ce-129">-Confirm</span></span>
<span data-ttu-id="298ce-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="298ce-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="298ce-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="298ce-131">-WhatIf</span></span>
<span data-ttu-id="298ce-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="298ce-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="298ce-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="298ce-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="298ce-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="298ce-134">CommonParameters</span></span>
<span data-ttu-id="298ce-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="298ce-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="298ce-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="298ce-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="298ce-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="298ce-137">INPUTS</span></span>

### <span data-ttu-id="298ce-138">Microsoft. Azure. Commands. Network. modeller. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="298ce-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="298ce-139">System. String</span><span class="sxs-lookup"><span data-stu-id="298ce-139">System.String</span></span>

## <span data-ttu-id="298ce-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="298ce-140">OUTPUTS</span></span>

### <span data-ttu-id="298ce-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="298ce-141">System.Boolean</span></span>

## <span data-ttu-id="298ce-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="298ce-142">NOTES</span></span>

## <span data-ttu-id="298ce-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="298ce-143">RELATED LINKS</span></span>
