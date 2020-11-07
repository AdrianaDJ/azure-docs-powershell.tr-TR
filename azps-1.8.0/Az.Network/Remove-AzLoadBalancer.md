---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
ms.openlocfilehash: b91a807d5499236d45e84a9a064e7f64daa1fb57
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760165"
---
# <span data-ttu-id="83776-101">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="83776-101">Remove-AzLoadBalancer</span></span>

## <span data-ttu-id="83776-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83776-102">SYNOPSIS</span></span>
<span data-ttu-id="83776-103">Yük dengeleyiciden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="83776-103">Removes a load balancer.</span></span>

## <span data-ttu-id="83776-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="83776-104">SYNTAX</span></span>

```
Remove-AzLoadBalancer -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83776-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="83776-105">DESCRIPTION</span></span>
<span data-ttu-id="83776-106">**Remove-AzLoadBalancer** cmdlet 'ı bir Azure Yük dengeleyicisinin kaldırılmasını göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="83776-106">The **Remove-AzLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="83776-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="83776-107">EXAMPLES</span></span>

### <span data-ttu-id="83776-108">Örnek 1: yük dengeleyiciden kaldırma</span><span class="sxs-lookup"><span data-stu-id="83776-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="83776-109">Bu komut MyResourceGroup adlı kaynak grubunda MyLoadBalancer adlı bir yük dengeleyicisi siler.</span><span class="sxs-lookup"><span data-stu-id="83776-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="83776-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="83776-110">PARAMETERS</span></span>

### <span data-ttu-id="83776-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="83776-111">-AsJob</span></span>
<span data-ttu-id="83776-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="83776-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="83776-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83776-113">-DefaultProfile</span></span>
<span data-ttu-id="83776-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="83776-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83776-115">-Force</span><span class="sxs-lookup"><span data-stu-id="83776-115">-Force</span></span>
<span data-ttu-id="83776-116">Bu cmdlet 'in, kaynağa atanmış olup olmadıklarına bakılmaksızın yük dengeleyiciden kaldırıldığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="83776-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="83776-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="83776-117">-Name</span></span>
<span data-ttu-id="83776-118">Kaldırılacak yük dengeleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="83776-118">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="83776-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="83776-119">-PassThru</span></span>
<span data-ttu-id="83776-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="83776-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="83776-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="83776-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="83776-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83776-122">-ResourceGroupName</span></span>
<span data-ttu-id="83776-123">Kaldırılacak yük dengeleyicinin bulunduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="83776-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="83776-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="83776-124">-Confirm</span></span>
<span data-ttu-id="83776-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="83776-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83776-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83776-126">-WhatIf</span></span>
<span data-ttu-id="83776-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="83776-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83776-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="83776-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83776-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83776-129">CommonParameters</span></span>
<span data-ttu-id="83776-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="83776-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83776-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83776-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83776-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="83776-132">INPUTS</span></span>

### <span data-ttu-id="83776-133">System. String</span><span class="sxs-lookup"><span data-stu-id="83776-133">System.String</span></span>

## <span data-ttu-id="83776-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="83776-134">OUTPUTS</span></span>

### <span data-ttu-id="83776-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="83776-135">System.Boolean</span></span>

## <span data-ttu-id="83776-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="83776-136">NOTES</span></span>

## <span data-ttu-id="83776-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="83776-137">RELATED LINKS</span></span>

[<span data-ttu-id="83776-138">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="83776-138">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="83776-139">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="83776-139">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="83776-140">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="83776-140">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


