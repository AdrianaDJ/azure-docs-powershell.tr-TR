---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteTable.md
ms.openlocfilehash: 17cd4ab4e60156c1ab4d6dd4357e638ddaf2c5a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762562"
---
# <span data-ttu-id="778f9-101">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="778f9-101">Remove-AzureRmRouteTable</span></span>

## <span data-ttu-id="778f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="778f9-102">SYNOPSIS</span></span>
<span data-ttu-id="778f9-103">Yol tablosunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="778f9-103">Removes a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="778f9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="778f9-104">SYNTAX</span></span>

```
Remove-AzureRmRouteTable -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="778f9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="778f9-105">DESCRIPTION</span></span>
<span data-ttu-id="778f9-106">**Remove-AzureRmRouteTable** cmdlet 'ı bir Azure yol tablosunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="778f9-106">The **Remove-AzureRmRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="778f9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="778f9-107">EXAMPLES</span></span>

### <span data-ttu-id="778f9-108">Örnek 1: yol tablosunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="778f9-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzureRmRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="778f9-109">Bu komut, ResourceGroup11 adındaki kaynak grubundaki RouteTable01 adındaki yol tablosunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="778f9-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="778f9-110">Cmdlet tabloyu kaldırmadan önce onayınızı sorar.</span><span class="sxs-lookup"><span data-stu-id="778f9-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="778f9-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="778f9-111">PARAMETERS</span></span>

### <span data-ttu-id="778f9-112">-Force</span><span class="sxs-lookup"><span data-stu-id="778f9-112">-Force</span></span>
<span data-ttu-id="778f9-113">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="778f9-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="778f9-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="778f9-114">-Name</span></span>
<span data-ttu-id="778f9-115">Bu cmdlet 'in kaldırıldığı yol tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="778f9-115">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="778f9-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="778f9-116">-PassThru</span></span>
<span data-ttu-id="778f9-117">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="778f9-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="778f9-118">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="778f9-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="778f9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="778f9-119">-ResourceGroupName</span></span>
<span data-ttu-id="778f9-120">Bu cmdlet 'in kaldırdığı yol tablosunu içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="778f9-120">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="778f9-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="778f9-121">-Confirm</span></span>
<span data-ttu-id="778f9-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="778f9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="778f9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="778f9-123">-WhatIf</span></span>
<span data-ttu-id="778f9-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="778f9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="778f9-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="778f9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="778f9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="778f9-126">-DefaultProfile</span></span>
<span data-ttu-id="778f9-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="778f9-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="778f9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="778f9-128">CommonParameters</span></span>
<span data-ttu-id="778f9-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="778f9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="778f9-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="778f9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="778f9-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="778f9-131">INPUTS</span></span>

## <span data-ttu-id="778f9-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="778f9-132">OUTPUTS</span></span>

## <span data-ttu-id="778f9-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="778f9-133">NOTES</span></span>

## <span data-ttu-id="778f9-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="778f9-134">RELATED LINKS</span></span>

[<span data-ttu-id="778f9-135">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="778f9-135">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="778f9-136">Yeni-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="778f9-136">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="778f9-137">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="778f9-137">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


