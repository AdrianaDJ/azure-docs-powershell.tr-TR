---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 65540c331074b5c140bafe9e87d625dfaec2f252
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595143"
---
# <span data-ttu-id="ce289-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="ce289-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="ce289-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce289-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce289-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ce289-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce289-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="ce289-104">DESCRIPTION</span></span>

## <span data-ttu-id="ce289-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ce289-105">EXAMPLES</span></span>

## <span data-ttu-id="ce289-106">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ce289-106">PARAMETERS</span></span>

### <span data-ttu-id="ce289-107">-Force</span><span class="sxs-lookup"><span data-stu-id="ce289-107">-Force</span></span>
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

### <span data-ttu-id="ce289-108">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="ce289-108">-KeyLength</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce289-109">-Ad</span><span class="sxs-lookup"><span data-stu-id="ce289-109">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce289-110">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce289-110">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce289-111">-Onay</span><span class="sxs-lookup"><span data-stu-id="ce289-111">-Confirm</span></span>
<span data-ttu-id="ce289-112">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ce289-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce289-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce289-113">-WhatIf</span></span>
<span data-ttu-id="ce289-114">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce289-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce289-115">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ce289-115">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce289-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce289-116">-DefaultProfile</span></span>
<span data-ttu-id="ce289-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ce289-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce289-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce289-118">CommonParameters</span></span>
<span data-ttu-id="ce289-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ce289-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce289-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce289-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce289-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ce289-121">INPUTS</span></span>

## <span data-ttu-id="ce289-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ce289-122">OUTPUTS</span></span>

### <span data-ttu-id="ce289-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ce289-123">System.String</span></span>

## <span data-ttu-id="ce289-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ce289-124">NOTES</span></span>

## <span data-ttu-id="ce289-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ce289-125">RELATED LINKS</span></span>

[<span data-ttu-id="ce289-126">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="ce289-126">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="ce289-127">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="ce289-127">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


