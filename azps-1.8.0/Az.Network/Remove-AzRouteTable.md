---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
ms.openlocfilehash: 161b97ffd032c8a6f7aca6b40c719a45b7e6a935
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760124"
---
# <span data-ttu-id="df35c-101">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="df35c-101">Remove-AzRouteTable</span></span>

## <span data-ttu-id="df35c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df35c-102">SYNOPSIS</span></span>
<span data-ttu-id="df35c-103">Yol tablosunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="df35c-103">Removes a route table.</span></span>

## <span data-ttu-id="df35c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="df35c-104">SYNTAX</span></span>

```
Remove-AzRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df35c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="df35c-105">DESCRIPTION</span></span>
<span data-ttu-id="df35c-106">**Remove-AzRouteTable** cmdlet 'ı bir Azure yol tablosunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="df35c-106">The **Remove-AzRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="df35c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="df35c-107">EXAMPLES</span></span>

### <span data-ttu-id="df35c-108">Örnek 1: yol tablosunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="df35c-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="df35c-109">Bu komut, ResourceGroup11 adındaki kaynak grubundaki RouteTable01 adındaki yol tablosunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="df35c-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="df35c-110">Cmdlet tabloyu kaldırmadan önce onayınızı sorar.</span><span class="sxs-lookup"><span data-stu-id="df35c-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="df35c-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="df35c-111">PARAMETERS</span></span>

### <span data-ttu-id="df35c-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="df35c-112">-AsJob</span></span>
<span data-ttu-id="df35c-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="df35c-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="df35c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df35c-114">-DefaultProfile</span></span>
<span data-ttu-id="df35c-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="df35c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df35c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="df35c-116">-Force</span></span>
<span data-ttu-id="df35c-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="df35c-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="df35c-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="df35c-118">-Name</span></span>
<span data-ttu-id="df35c-119">Bu cmdlet 'in kaldırıldığı yol tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="df35c-119">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="df35c-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="df35c-120">-PassThru</span></span>
<span data-ttu-id="df35c-121">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="df35c-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="df35c-122">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="df35c-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="df35c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df35c-123">-ResourceGroupName</span></span>
<span data-ttu-id="df35c-124">Bu cmdlet 'in kaldırdığı yol tablosunu içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="df35c-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="df35c-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="df35c-125">-Confirm</span></span>
<span data-ttu-id="df35c-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="df35c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df35c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df35c-127">-WhatIf</span></span>
<span data-ttu-id="df35c-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="df35c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df35c-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="df35c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df35c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df35c-130">CommonParameters</span></span>
<span data-ttu-id="df35c-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="df35c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df35c-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df35c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df35c-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="df35c-133">INPUTS</span></span>

### <span data-ttu-id="df35c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="df35c-134">System.String</span></span>

## <span data-ttu-id="df35c-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="df35c-135">OUTPUTS</span></span>

### <span data-ttu-id="df35c-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="df35c-136">System.Boolean</span></span>

## <span data-ttu-id="df35c-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="df35c-137">NOTES</span></span>

## <span data-ttu-id="df35c-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="df35c-138">RELATED LINKS</span></span>

[<span data-ttu-id="df35c-139">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="df35c-139">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="df35c-140">Yeni-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="df35c-140">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="df35c-141">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="df35c-141">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


