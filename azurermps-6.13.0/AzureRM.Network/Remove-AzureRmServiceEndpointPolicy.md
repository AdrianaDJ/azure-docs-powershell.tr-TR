---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: f3871e23c0d193ef2ea89c43e3a30c5597abbfe0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593954"
---
# <span data-ttu-id="cc93b-101">Remove-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="cc93b-101">Remove-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="cc93b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc93b-102">SYNOPSIS</span></span>
<span data-ttu-id="cc93b-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="cc93b-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc93b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cc93b-104">SYNTAX</span></span>

```
Remove-AzureRmServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc93b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cc93b-105">DESCRIPTION</span></span>
<span data-ttu-id="cc93b-106">**Remove-AzureRmServiceEndpointPolicy** cmdlet 'i, hizmet uç nokta ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cc93b-106">The **Remove-AzureRmServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="cc93b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cc93b-107">EXAMPLES</span></span>

### <span data-ttu-id="cc93b-108">Örnek 1: ad kullanan bir hizmet uç nokta ilkesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="cc93b-108">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzureRmServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="cc93b-109">Bu komut, "resourcegroup1" adıyla resourcegroup 'a ait olan Policy1 ad uç noktası ilkesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="cc93b-109">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="cc93b-110">Örnek 2: giriş nesnesini kullanarak hizmet uç nokta ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="cc93b-110">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzureRmServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="cc93b-111">Bu komut, "resourcegroup1" adıyla bir Policy1</span><span class="sxs-lookup"><span data-stu-id="cc93b-111">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="cc93b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cc93b-112">PARAMETERS</span></span>

### <span data-ttu-id="cc93b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc93b-113">-DefaultProfile</span></span>
<span data-ttu-id="cc93b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cc93b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc93b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cc93b-115">-Force</span></span>
<span data-ttu-id="cc93b-116">Kaynağın üzerine yazılsın mı?</span><span class="sxs-lookup"><span data-stu-id="cc93b-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="cc93b-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="cc93b-117">-Name</span></span>
<span data-ttu-id="cc93b-118">Hizmet uç noktası ilkesinin adı</span><span class="sxs-lookup"><span data-stu-id="cc93b-118">The name of the service endpoint policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc93b-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="cc93b-119">-PassThru</span></span>
<span data-ttu-id="cc93b-120">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="cc93b-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="cc93b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc93b-121">-ResourceGroupName</span></span>
<span data-ttu-id="cc93b-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="cc93b-122">The resource group name.</span></span>

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

### <span data-ttu-id="cc93b-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="cc93b-123">-Confirm</span></span>
<span data-ttu-id="cc93b-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cc93b-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc93b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc93b-125">-WhatIf</span></span>
<span data-ttu-id="cc93b-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cc93b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc93b-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cc93b-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc93b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc93b-128">CommonParameters</span></span>
<span data-ttu-id="cc93b-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cc93b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="cc93b-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc93b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc93b-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cc93b-131">INPUTS</span></span>

### <span data-ttu-id="cc93b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="cc93b-132">System.String</span></span>


## <span data-ttu-id="cc93b-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cc93b-133">OUTPUTS</span></span>

### <span data-ttu-id="cc93b-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="cc93b-134">System.Object</span></span>

## <span data-ttu-id="cc93b-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cc93b-135">NOTES</span></span>

## <span data-ttu-id="cc93b-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cc93b-136">RELATED LINKS</span></span>
