---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
ms.openlocfilehash: 716606214bcd23bd51286fa3a7a0e4f8c0c4ff70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325810"
---
# <span data-ttu-id="2ea47-101">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2ea47-101">Remove-AzPrivateEndpoint</span></span>

## <span data-ttu-id="2ea47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ea47-102">SYNOPSIS</span></span>
<span data-ttu-id="2ea47-103">Özel uç noktayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2ea47-103">Removes a private endpoint.</span></span>

## <span data-ttu-id="2ea47-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ea47-104">SYNTAX</span></span>

```
Remove-AzPrivateEndpoint -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ea47-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ea47-105">DESCRIPTION</span></span>
<span data-ttu-id="2ea47-106">**Remove-AzPrivateEndpoint** cmdlet 'i özel uç noktayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2ea47-106">The **Remove-AzPrivateEndpoint** cmdlet removes a private endpoint.</span></span> 

## <span data-ttu-id="2ea47-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ea47-107">EXAMPLES</span></span>

### <span data-ttu-id="2ea47-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2ea47-108">Example 1</span></span>
```
Remove-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="2ea47-109">Bu örnekte MyPrivateEndpoint1 adlı özel bir uç nokta kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="2ea47-109">This example remove a private endpoint named MyPrivateEndpoint1.</span></span>

## <span data-ttu-id="2ea47-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ea47-110">PARAMETERS</span></span>

### <span data-ttu-id="2ea47-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="2ea47-111">-AsJob</span></span>
<span data-ttu-id="2ea47-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2ea47-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2ea47-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ea47-113">-DefaultProfile</span></span>
<span data-ttu-id="2ea47-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2ea47-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ea47-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2ea47-115">-Force</span></span>
<span data-ttu-id="2ea47-116">Kaynağı silmek istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="2ea47-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="2ea47-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="2ea47-117">-Name</span></span>
<span data-ttu-id="2ea47-118">Özel uç noktasının adı.</span><span class="sxs-lookup"><span data-stu-id="2ea47-118">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="2ea47-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2ea47-119">-PassThru</span></span>
<span data-ttu-id="2ea47-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="2ea47-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2ea47-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="2ea47-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2ea47-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ea47-122">-ResourceGroupName</span></span>
<span data-ttu-id="2ea47-123">Özel uç noktasının kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2ea47-123">The resource group name of the private endpoint.</span></span>

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

### <span data-ttu-id="2ea47-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="2ea47-124">-Confirm</span></span>
<span data-ttu-id="2ea47-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2ea47-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ea47-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ea47-126">-WhatIf</span></span>
<span data-ttu-id="2ea47-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ea47-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ea47-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2ea47-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ea47-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea47-129">CommonParameters</span></span>
<span data-ttu-id="2ea47-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ea47-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ea47-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2ea47-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea47-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ea47-132">INPUTS</span></span>

### <span data-ttu-id="2ea47-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2ea47-133">System.String</span></span>

## <span data-ttu-id="2ea47-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ea47-134">OUTPUTS</span></span>

### <span data-ttu-id="2ea47-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2ea47-135">System.Boolean</span></span>

## <span data-ttu-id="2ea47-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ea47-136">NOTES</span></span>

## <span data-ttu-id="2ea47-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ea47-137">RELATED LINKS</span></span>

[<span data-ttu-id="2ea47-138">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2ea47-138">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="2ea47-139">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2ea47-139">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)