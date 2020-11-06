---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGateway.md
ms.openlocfilehash: b743c9b2fa0e8abff1a878b6cdb780c025300ba7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587527"
---
# <span data-ttu-id="1d40a-101">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1d40a-101">Remove-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="1d40a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d40a-102">SYNOPSIS</span></span>
<span data-ttu-id="1d40a-103">Uygulama ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1d40a-103">Removes an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d40a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1d40a-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d40a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1d40a-105">DESCRIPTION</span></span>
<span data-ttu-id="1d40a-106">**Remove-AzureRmApplicationGateway** cmdlet 'i uygulama ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1d40a-106">The **Remove-AzureRmApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="1d40a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1d40a-107">EXAMPLES</span></span>

### <span data-ttu-id="1d40a-108">Örnek 1: belirtilen uygulama ağ geçidini kaldırma</span><span class="sxs-lookup"><span data-stu-id="1d40a-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1d40a-109">Bu komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1d40a-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="1d40a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1d40a-110">PARAMETERS</span></span>

### <span data-ttu-id="1d40a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d40a-111">-DefaultProfile</span></span>
<span data-ttu-id="1d40a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1d40a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d40a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1d40a-113">-Force</span></span>
<span data-ttu-id="1d40a-114">, Uygulamanın atanmış olup olmadıklarına bakılmaksızın cmdlet 'in uygulama ağ geçidi silinmesini zorunlu hale gelir.</span><span class="sxs-lookup"><span data-stu-id="1d40a-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="1d40a-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="1d40a-115">-Name</span></span>
<span data-ttu-id="1d40a-116">Kaldırılacak uygulama ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d40a-116">Specifies the name of the application gateway to be removed.</span></span>

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

### <span data-ttu-id="1d40a-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1d40a-117">-PassThru</span></span>
<span data-ttu-id="1d40a-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="1d40a-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1d40a-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="1d40a-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1d40a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d40a-120">-ResourceGroupName</span></span>
<span data-ttu-id="1d40a-121">Uygulama ağ geçidinin ait olduğu kaynak grubu adının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d40a-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="1d40a-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="1d40a-122">-Confirm</span></span>
<span data-ttu-id="1d40a-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1d40a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d40a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d40a-124">-WhatIf</span></span>
<span data-ttu-id="1d40a-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1d40a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d40a-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1d40a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d40a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d40a-127">CommonParameters</span></span>
<span data-ttu-id="1d40a-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1d40a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d40a-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d40a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d40a-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1d40a-130">INPUTS</span></span>

### <span data-ttu-id="1d40a-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1d40a-131">None</span></span>
<span data-ttu-id="1d40a-132">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="1d40a-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1d40a-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1d40a-133">OUTPUTS</span></span>

### <span data-ttu-id="1d40a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1d40a-134">System.String</span></span>

## <span data-ttu-id="1d40a-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1d40a-135">NOTES</span></span>

## <span data-ttu-id="1d40a-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1d40a-136">RELATED LINKS</span></span>

[<span data-ttu-id="1d40a-137">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1d40a-137">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)


