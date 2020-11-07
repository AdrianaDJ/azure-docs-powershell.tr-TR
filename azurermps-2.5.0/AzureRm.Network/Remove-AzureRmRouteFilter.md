---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilter
schema: 2.0.0
ms.openlocfilehash: 3622b7ad87658091d4b54af62678d12a324ef56a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940032"
---
# <span data-ttu-id="ffc54-101">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ffc54-101">Remove-AzureRmRouteFilter</span></span>

## <span data-ttu-id="ffc54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffc54-102">SYNOPSIS</span></span>
<span data-ttu-id="ffc54-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="ffc54-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffc54-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ffc54-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffc54-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ffc54-105">DESCRIPTION</span></span>
<span data-ttu-id="ffc54-106">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="ffc54-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="ffc54-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ffc54-107">EXAMPLES</span></span>

### <span data-ttu-id="ffc54-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ffc54-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ffc54-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="ffc54-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="ffc54-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ffc54-110">PARAMETERS</span></span>

### <span data-ttu-id="ffc54-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffc54-111">-DefaultProfile</span></span>
<span data-ttu-id="ffc54-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ffc54-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffc54-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ffc54-113">-Force</span></span>
<span data-ttu-id="ffc54-114">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="ffc54-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ffc54-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="ffc54-115">-Name</span></span>
<span data-ttu-id="ffc54-116">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="ffc54-116">The resource name.</span></span>

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

### <span data-ttu-id="ffc54-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ffc54-117">-PassThru</span></span>
<span data-ttu-id="ffc54-118">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="ffc54-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ffc54-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffc54-119">-ResourceGroupName</span></span>
<span data-ttu-id="ffc54-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ffc54-120">The resource group name.</span></span>

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

### <span data-ttu-id="ffc54-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="ffc54-121">-Confirm</span></span>
<span data-ttu-id="ffc54-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ffc54-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffc54-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffc54-123">-WhatIf</span></span>
<span data-ttu-id="ffc54-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ffc54-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffc54-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ffc54-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffc54-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffc54-126">CommonParameters</span></span>
<span data-ttu-id="ffc54-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ffc54-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffc54-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffc54-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffc54-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ffc54-129">INPUTS</span></span>

### <span data-ttu-id="ffc54-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ffc54-130">System.String</span></span>

## <span data-ttu-id="ffc54-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ffc54-131">OUTPUTS</span></span>

### <span data-ttu-id="ffc54-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="ffc54-132">System.Object</span></span>

## <span data-ttu-id="ffc54-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ffc54-133">NOTES</span></span>

## <span data-ttu-id="ffc54-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ffc54-134">RELATED LINKS</span></span>

