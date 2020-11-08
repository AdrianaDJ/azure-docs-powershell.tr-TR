---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteTable.md
ms.openlocfilehash: 434d70cbdce08750e69865e59197ebba5fb6e6fb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936608"
---
# <span data-ttu-id="bc510-101">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="bc510-101">Remove-AzRouteTable</span></span>

## <span data-ttu-id="bc510-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc510-102">SYNOPSIS</span></span>
<span data-ttu-id="bc510-103">Yol tablosunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bc510-103">Removes a route table.</span></span>

## <span data-ttu-id="bc510-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bc510-104">SYNTAX</span></span>

```
Remove-AzRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc510-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc510-105">DESCRIPTION</span></span>
<span data-ttu-id="bc510-106">**Remove-AzRouteTable** cmdlet 'ı bir Azure yol tablosunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bc510-106">The **Remove-AzRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="bc510-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bc510-107">EXAMPLES</span></span>

### <span data-ttu-id="bc510-108">Örnek 1: yol tablosunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="bc510-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="bc510-109">Bu komut, ResourceGroup11 adındaki kaynak grubundaki RouteTable01 adındaki yol tablosunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bc510-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="bc510-110">Cmdlet tabloyu kaldırmadan önce onayınızı sorar.</span><span class="sxs-lookup"><span data-stu-id="bc510-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="bc510-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bc510-111">PARAMETERS</span></span>

### <span data-ttu-id="bc510-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="bc510-112">-AsJob</span></span>
<span data-ttu-id="bc510-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="bc510-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc510-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc510-114">-DefaultProfile</span></span>
<span data-ttu-id="bc510-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bc510-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc510-116">-Force</span><span class="sxs-lookup"><span data-stu-id="bc510-116">-Force</span></span>
<span data-ttu-id="bc510-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="bc510-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bc510-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="bc510-118">-Name</span></span>
<span data-ttu-id="bc510-119">Bu cmdlet 'in kaldırıldığı yol tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc510-119">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bc510-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bc510-120">-PassThru</span></span>
<span data-ttu-id="bc510-121">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="bc510-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bc510-122">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="bc510-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bc510-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc510-123">-ResourceGroupName</span></span>
<span data-ttu-id="bc510-124">Bu cmdlet 'in kaldırdığı yol tablosunu içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc510-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bc510-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="bc510-125">-Confirm</span></span>
<span data-ttu-id="bc510-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bc510-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc510-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc510-127">-WhatIf</span></span>
<span data-ttu-id="bc510-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bc510-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc510-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bc510-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc510-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc510-130">CommonParameters</span></span>
<span data-ttu-id="bc510-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bc510-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc510-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc510-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc510-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bc510-133">INPUTS</span></span>

## <span data-ttu-id="bc510-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bc510-134">OUTPUTS</span></span>

## <span data-ttu-id="bc510-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bc510-135">NOTES</span></span>

## <span data-ttu-id="bc510-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bc510-136">RELATED LINKS</span></span>

[<span data-ttu-id="bc510-137">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="bc510-137">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="bc510-138">Yeni-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="bc510-138">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="bc510-139">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="bc510-139">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)

