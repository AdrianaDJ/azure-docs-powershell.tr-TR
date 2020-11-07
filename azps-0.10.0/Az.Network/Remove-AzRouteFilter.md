---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: 02f3e0a151fe8dc810e8530af88059371139f08c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936610"
---
# <span data-ttu-id="c6c46-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c6c46-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="c6c46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6c46-102">SYNOPSIS</span></span>
<span data-ttu-id="c6c46-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="c6c46-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="c6c46-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c6c46-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6c46-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c6c46-105">DESCRIPTION</span></span>
<span data-ttu-id="c6c46-106">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="c6c46-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="c6c46-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c6c46-107">EXAMPLES</span></span>

### <span data-ttu-id="c6c46-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c6c46-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="c6c46-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="c6c46-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="c6c46-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c6c46-110">PARAMETERS</span></span>

### <span data-ttu-id="c6c46-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6c46-111">-DefaultProfile</span></span>
<span data-ttu-id="c6c46-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c6c46-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6c46-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c6c46-113">-Force</span></span>
<span data-ttu-id="c6c46-114">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="c6c46-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c6c46-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="c6c46-115">-Name</span></span>
<span data-ttu-id="c6c46-116">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="c6c46-116">The resource name.</span></span>

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

### <span data-ttu-id="c6c46-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c6c46-117">-PassThru</span></span>
<span data-ttu-id="c6c46-118">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="c6c46-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c6c46-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6c46-119">-ResourceGroupName</span></span>
<span data-ttu-id="c6c46-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c6c46-120">The resource group name.</span></span>

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

### <span data-ttu-id="c6c46-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="c6c46-121">-Confirm</span></span>
<span data-ttu-id="c6c46-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c6c46-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6c46-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6c46-123">-WhatIf</span></span>
<span data-ttu-id="c6c46-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c6c46-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6c46-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c6c46-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6c46-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6c46-126">CommonParameters</span></span>
<span data-ttu-id="c6c46-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c6c46-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6c46-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6c46-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6c46-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c6c46-129">INPUTS</span></span>

### <span data-ttu-id="c6c46-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c6c46-130">System.String</span></span>

## <span data-ttu-id="c6c46-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c6c46-131">OUTPUTS</span></span>

### <span data-ttu-id="c6c46-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="c6c46-132">System.Object</span></span>

## <span data-ttu-id="c6c46-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c6c46-133">NOTES</span></span>

## <span data-ttu-id="c6c46-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c6c46-134">RELATED LINKS</span></span>

