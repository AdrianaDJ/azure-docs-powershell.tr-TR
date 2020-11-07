---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilter.md
ms.openlocfilehash: 5fcdbeee663873292b463bf774762c9de5418b75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764178"
---
# <span data-ttu-id="3ad1a-101">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3ad1a-101">Remove-AzureRmRouteFilter</span></span>

## <span data-ttu-id="3ad1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ad1a-102">SYNOPSIS</span></span>
<span data-ttu-id="3ad1a-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="3ad1a-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ad1a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3ad1a-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ad1a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3ad1a-105">DESCRIPTION</span></span>
<span data-ttu-id="3ad1a-106">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="3ad1a-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="3ad1a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3ad1a-107">EXAMPLES</span></span>

### <span data-ttu-id="3ad1a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3ad1a-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="3ad1a-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="3ad1a-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="3ad1a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3ad1a-110">PARAMETERS</span></span>

### <span data-ttu-id="3ad1a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ad1a-111">-DefaultProfile</span></span>
<span data-ttu-id="3ad1a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3ad1a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ad1a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3ad1a-113">-Force</span></span>
<span data-ttu-id="3ad1a-114">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="3ad1a-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3ad1a-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="3ad1a-115">-Name</span></span>
<span data-ttu-id="3ad1a-116">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="3ad1a-116">The resource name.</span></span>

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

### <span data-ttu-id="3ad1a-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3ad1a-117">-PassThru</span></span>
<span data-ttu-id="3ad1a-118">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="3ad1a-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3ad1a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ad1a-119">-ResourceGroupName</span></span>
<span data-ttu-id="3ad1a-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3ad1a-120">The resource group name.</span></span>

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

### <span data-ttu-id="3ad1a-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="3ad1a-121">-Confirm</span></span>
<span data-ttu-id="3ad1a-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3ad1a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ad1a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ad1a-123">-WhatIf</span></span>
<span data-ttu-id="3ad1a-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3ad1a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ad1a-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3ad1a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ad1a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ad1a-126">CommonParameters</span></span>
<span data-ttu-id="3ad1a-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3ad1a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ad1a-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ad1a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ad1a-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3ad1a-129">INPUTS</span></span>

### <span data-ttu-id="3ad1a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3ad1a-130">System.String</span></span>

## <span data-ttu-id="3ad1a-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3ad1a-131">OUTPUTS</span></span>

### <span data-ttu-id="3ad1a-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="3ad1a-132">System.Object</span></span>

## <span data-ttu-id="3ad1a-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3ad1a-133">NOTES</span></span>

## <span data-ttu-id="3ad1a-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3ad1a-134">RELATED LINKS</span></span>

