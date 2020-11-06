---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
ms.openlocfilehash: 13ece8d5bb6ec42e59f6a44910d3a3d46dd9d844
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588154"
---
# <span data-ttu-id="b472c-101">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b472c-101">Remove-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="b472c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b472c-102">SYNOPSIS</span></span>
<span data-ttu-id="b472c-103">Yük dengeleyiciden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b472c-103">Removes a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b472c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b472c-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b472c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b472c-105">DESCRIPTION</span></span>
<span data-ttu-id="b472c-106">**Remove-AzureRmLoadBalancer** cmdlet 'ı bir Azure Yük dengeleyicisinin kaldırılmasını göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="b472c-106">The **Remove-AzureRmLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="b472c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b472c-107">EXAMPLES</span></span>

### <span data-ttu-id="b472c-108">Örnek 1: yük dengeleyiciden kaldırma</span><span class="sxs-lookup"><span data-stu-id="b472c-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="b472c-109">Bu komut MyResourceGroup adlı kaynak grubunda MyLoadBalancer adlı bir yük dengeleyicisi siler.</span><span class="sxs-lookup"><span data-stu-id="b472c-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="b472c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b472c-110">PARAMETERS</span></span>

### <span data-ttu-id="b472c-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="b472c-111">-AsJob</span></span>
<span data-ttu-id="b472c-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b472c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b472c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b472c-113">-DefaultProfile</span></span>
<span data-ttu-id="b472c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b472c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b472c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b472c-115">-Force</span></span>
<span data-ttu-id="b472c-116">Bu cmdlet 'in, kaynağa atanmış olup olmadıklarına bakılmaksızın yük dengeleyiciden kaldırıldığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="b472c-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b472c-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="b472c-117">-Name</span></span>
<span data-ttu-id="b472c-118">Kaldırılacak yük dengeleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b472c-118">Specifies the name of the load balancer to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b472c-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b472c-119">-PassThru</span></span>
<span data-ttu-id="b472c-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="b472c-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b472c-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="b472c-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b472c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b472c-122">-ResourceGroupName</span></span>
<span data-ttu-id="b472c-123">Kaldırılacak yük dengeleyicinin bulunduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b472c-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b472c-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="b472c-124">-Confirm</span></span>
<span data-ttu-id="b472c-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b472c-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b472c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b472c-126">-WhatIf</span></span>
<span data-ttu-id="b472c-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b472c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b472c-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b472c-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b472c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b472c-129">CommonParameters</span></span>
<span data-ttu-id="b472c-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b472c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b472c-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b472c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b472c-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b472c-132">INPUTS</span></span>

### <span data-ttu-id="b472c-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b472c-133">None</span></span>
<span data-ttu-id="b472c-134">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b472c-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b472c-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b472c-135">OUTPUTS</span></span>

## <span data-ttu-id="b472c-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b472c-136">NOTES</span></span>

## <span data-ttu-id="b472c-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b472c-137">RELATED LINKS</span></span>

[<span data-ttu-id="b472c-138">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b472c-138">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="b472c-139">Yeni-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b472c-139">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="b472c-140">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b472c-140">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


