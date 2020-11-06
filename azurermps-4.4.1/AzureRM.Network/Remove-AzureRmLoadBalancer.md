---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
ms.openlocfilehash: 6757c9c0b9eeb0b3408a07713c62812d361d814a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594612"
---
# <span data-ttu-id="ad749-101">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ad749-101">Remove-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="ad749-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad749-102">SYNOPSIS</span></span>
<span data-ttu-id="ad749-103">Yük dengeleyiciden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ad749-103">Removes a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad749-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad749-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad749-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad749-105">DESCRIPTION</span></span>
<span data-ttu-id="ad749-106">**Remove-AzureRmLoadBalancer** cmdlet 'ı bir Azure Yük dengeleyicisinin kaldırılmasını göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="ad749-106">The **Remove-AzureRmLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="ad749-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad749-107">EXAMPLES</span></span>

### <span data-ttu-id="ad749-108">Örnek 1: yük dengeleyiciden kaldırma</span><span class="sxs-lookup"><span data-stu-id="ad749-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="ad749-109">Bu komut MyResourceGroup adlı kaynak grubunda MyLoadBalancer adlı bir yük dengeleyicisi siler.</span><span class="sxs-lookup"><span data-stu-id="ad749-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="ad749-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad749-110">PARAMETERS</span></span>

### <span data-ttu-id="ad749-111">-Force</span><span class="sxs-lookup"><span data-stu-id="ad749-111">-Force</span></span>
<span data-ttu-id="ad749-112">Bu cmdlet 'in, kaynağa atanmış olup olmadıklarına bakılmaksızın yük dengeleyiciden kaldırıldığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="ad749-112">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad749-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="ad749-113">-Name</span></span>
<span data-ttu-id="ad749-114">Kaldırılacak yük dengeleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad749-114">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="ad749-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ad749-115">-PassThru</span></span>
<span data-ttu-id="ad749-116">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="ad749-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ad749-117">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="ad749-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ad749-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad749-118">-ResourceGroupName</span></span>
<span data-ttu-id="ad749-119">Kaldırılacak yük dengeleyicinin bulunduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad749-119">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="ad749-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="ad749-120">-Confirm</span></span>
<span data-ttu-id="ad749-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ad749-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad749-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad749-122">-WhatIf</span></span>
<span data-ttu-id="ad749-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ad749-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad749-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ad749-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad749-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad749-125">-DefaultProfile</span></span>
<span data-ttu-id="ad749-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ad749-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad749-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad749-127">CommonParameters</span></span>
<span data-ttu-id="ad749-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad749-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad749-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad749-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad749-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad749-130">INPUTS</span></span>

## <span data-ttu-id="ad749-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad749-131">OUTPUTS</span></span>

## <span data-ttu-id="ad749-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad749-132">NOTES</span></span>

## <span data-ttu-id="ad749-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad749-133">RELATED LINKS</span></span>

[<span data-ttu-id="ad749-134">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ad749-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="ad749-135">Yeni-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ad749-135">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="ad749-136">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ad749-136">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


