---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 99ac8e367c42cd59b3f055aa4a86a3efd4f297a0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939285"
---
# <span data-ttu-id="d544e-101">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d544e-101">Remove-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="d544e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d544e-102">SYNOPSIS</span></span>
<span data-ttu-id="d544e-103">Uygulama ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d544e-103">Removes an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d544e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d544e-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d544e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d544e-105">DESCRIPTION</span></span>
<span data-ttu-id="d544e-106">**Remove-AzureRmApplicationGateway** cmdlet 'i uygulama ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d544e-106">The **Remove-AzureRmApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="d544e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d544e-107">EXAMPLES</span></span>

### <span data-ttu-id="d544e-108">Örnek 1: belirtilen uygulama ağ geçidini kaldırma</span><span class="sxs-lookup"><span data-stu-id="d544e-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d544e-109">Bu komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d544e-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="d544e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d544e-110">PARAMETERS</span></span>

### <span data-ttu-id="d544e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d544e-111">-DefaultProfile</span></span>
<span data-ttu-id="d544e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d544e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d544e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d544e-113">-Force</span></span>
<span data-ttu-id="d544e-114">, Uygulamanın atanmış olup olmadıklarına bakılmaksızın cmdlet 'in uygulama ağ geçidi silinmesini zorunlu hale gelir.</span><span class="sxs-lookup"><span data-stu-id="d544e-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="d544e-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="d544e-115">-Name</span></span>
<span data-ttu-id="d544e-116">Kaldırılacak uygulama ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d544e-116">Specifies the name of the application gateway to be removed.</span></span>

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

### <span data-ttu-id="d544e-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d544e-117">-PassThru</span></span>
<span data-ttu-id="d544e-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="d544e-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d544e-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="d544e-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d544e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d544e-120">-ResourceGroupName</span></span>
<span data-ttu-id="d544e-121">Uygulama ağ geçidinin ait olduğu kaynak grubu adının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d544e-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="d544e-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="d544e-122">-Confirm</span></span>
<span data-ttu-id="d544e-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d544e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d544e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d544e-124">-WhatIf</span></span>
<span data-ttu-id="d544e-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d544e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d544e-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d544e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d544e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d544e-127">CommonParameters</span></span>
<span data-ttu-id="d544e-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d544e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d544e-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d544e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d544e-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d544e-130">INPUTS</span></span>

## <span data-ttu-id="d544e-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d544e-131">OUTPUTS</span></span>

### <span data-ttu-id="d544e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d544e-132">System.String</span></span>

## <span data-ttu-id="d544e-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d544e-133">NOTES</span></span>

## <span data-ttu-id="d544e-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d544e-134">RELATED LINKS</span></span>

[<span data-ttu-id="d544e-135">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d544e-135">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)


