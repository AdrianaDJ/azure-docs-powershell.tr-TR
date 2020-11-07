---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
ms.openlocfilehash: ba7bda62d0d001f11ff729ca0ecce6327b659855
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918143"
---
# <span data-ttu-id="b01cd-101">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b01cd-101">Remove-AzApplicationGateway</span></span>

## <span data-ttu-id="b01cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b01cd-102">SYNOPSIS</span></span>
<span data-ttu-id="b01cd-103">Uygulama ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b01cd-103">Removes an application gateway.</span></span>

## <span data-ttu-id="b01cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b01cd-104">SYNTAX</span></span>

```
Remove-AzApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b01cd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b01cd-105">DESCRIPTION</span></span>
<span data-ttu-id="b01cd-106">**Remove-AzApplicationGateway** cmdlet 'i uygulama ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b01cd-106">The **Remove-AzApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="b01cd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b01cd-107">EXAMPLES</span></span>

### <span data-ttu-id="b01cd-108">Örnek 1: belirtilen uygulama ağ geçidini kaldırma</span><span class="sxs-lookup"><span data-stu-id="b01cd-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b01cd-109">Bu komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b01cd-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="b01cd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b01cd-110">PARAMETERS</span></span>

### <span data-ttu-id="b01cd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b01cd-111">-DefaultProfile</span></span>
<span data-ttu-id="b01cd-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b01cd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b01cd-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b01cd-113">-Force</span></span>
<span data-ttu-id="b01cd-114">, Uygulamanın atanmış olup olmadıklarına bakılmaksızın cmdlet 'in uygulama ağ geçidi silinmesini zorunlu hale gelir.</span><span class="sxs-lookup"><span data-stu-id="b01cd-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="b01cd-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="b01cd-115">-Name</span></span>
<span data-ttu-id="b01cd-116">Kaldırılacak uygulama ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b01cd-116">Specifies the name of the application gateway to be removed.</span></span>

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

### <span data-ttu-id="b01cd-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b01cd-117">-PassThru</span></span>
<span data-ttu-id="b01cd-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="b01cd-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b01cd-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="b01cd-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b01cd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b01cd-120">-ResourceGroupName</span></span>
<span data-ttu-id="b01cd-121">Uygulama ağ geçidinin ait olduğu kaynak grubu adının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b01cd-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="b01cd-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="b01cd-122">-Confirm</span></span>
<span data-ttu-id="b01cd-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b01cd-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b01cd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b01cd-124">-WhatIf</span></span>
<span data-ttu-id="b01cd-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b01cd-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b01cd-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b01cd-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b01cd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b01cd-127">CommonParameters</span></span>
<span data-ttu-id="b01cd-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b01cd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b01cd-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b01cd-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b01cd-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b01cd-130">INPUTS</span></span>

### <span data-ttu-id="b01cd-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b01cd-131">System.String</span></span>

### <span data-ttu-id="b01cd-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b01cd-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b01cd-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b01cd-133">OUTPUTS</span></span>

### <span data-ttu-id="b01cd-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b01cd-134">System.Boolean</span></span>

## <span data-ttu-id="b01cd-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b01cd-135">NOTES</span></span>

## <span data-ttu-id="b01cd-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b01cd-136">RELATED LINKS</span></span>

[<span data-ttu-id="b01cd-137">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b01cd-137">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)


