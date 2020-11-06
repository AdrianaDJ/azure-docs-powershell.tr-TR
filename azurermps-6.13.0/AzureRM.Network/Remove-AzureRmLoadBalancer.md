---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
ms.openlocfilehash: d725735caf7806233688e6f0bcdddb4edb0f62b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589438"
---
# <span data-ttu-id="bfac9-101">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bfac9-101">Remove-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="bfac9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfac9-102">SYNOPSIS</span></span>
<span data-ttu-id="bfac9-103">Yük dengeleyiciden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bfac9-103">Removes a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfac9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bfac9-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancer -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfac9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bfac9-105">DESCRIPTION</span></span>
<span data-ttu-id="bfac9-106">**Remove-AzureRmLoadBalancer** cmdlet 'ı bir Azure Yük dengeleyicisinin kaldırılmasını göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="bfac9-106">The **Remove-AzureRmLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="bfac9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bfac9-107">EXAMPLES</span></span>

### <span data-ttu-id="bfac9-108">Örnek 1: yük dengeleyiciden kaldırma</span><span class="sxs-lookup"><span data-stu-id="bfac9-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="bfac9-109">Bu komut MyResourceGroup adlı kaynak grubunda MyLoadBalancer adlı bir yük dengeleyicisi siler.</span><span class="sxs-lookup"><span data-stu-id="bfac9-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="bfac9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bfac9-110">PARAMETERS</span></span>

### <span data-ttu-id="bfac9-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="bfac9-111">-AsJob</span></span>
<span data-ttu-id="bfac9-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="bfac9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bfac9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfac9-113">-DefaultProfile</span></span>
<span data-ttu-id="bfac9-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bfac9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfac9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bfac9-115">-Force</span></span>
<span data-ttu-id="bfac9-116">Bu cmdlet 'in, kaynağa atanmış olup olmadıklarına bakılmaksızın yük dengeleyiciden kaldırıldığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="bfac9-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="bfac9-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="bfac9-117">-Name</span></span>
<span data-ttu-id="bfac9-118">Kaldırılacak yük dengeleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfac9-118">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="bfac9-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bfac9-119">-PassThru</span></span>
<span data-ttu-id="bfac9-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="bfac9-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bfac9-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="bfac9-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bfac9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfac9-122">-ResourceGroupName</span></span>
<span data-ttu-id="bfac9-123">Kaldırılacak yük dengeleyicinin bulunduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfac9-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="bfac9-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="bfac9-124">-Confirm</span></span>
<span data-ttu-id="bfac9-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bfac9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfac9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfac9-126">-WhatIf</span></span>
<span data-ttu-id="bfac9-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bfac9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfac9-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bfac9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfac9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfac9-129">CommonParameters</span></span>
<span data-ttu-id="bfac9-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bfac9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfac9-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfac9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfac9-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bfac9-132">INPUTS</span></span>

### <span data-ttu-id="bfac9-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bfac9-133">System.String</span></span>

### <span data-ttu-id="bfac9-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bfac9-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bfac9-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bfac9-135">OUTPUTS</span></span>

### <span data-ttu-id="bfac9-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bfac9-136">System.Boolean</span></span>

## <span data-ttu-id="bfac9-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bfac9-137">NOTES</span></span>

## <span data-ttu-id="bfac9-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bfac9-138">RELATED LINKS</span></span>

[<span data-ttu-id="bfac9-139">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bfac9-139">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="bfac9-140">Yeni-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bfac9-140">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="bfac9-141">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bfac9-141">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


