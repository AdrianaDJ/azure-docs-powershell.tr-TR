---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
ms.openlocfilehash: b7b01ec1b301741c07a0667931a63287cc503434
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096184"
---
# <span data-ttu-id="15d29-101">Remove-AzFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="15d29-101">Remove-AzFrontDoorContent</span></span>

## <span data-ttu-id="15d29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15d29-102">SYNOPSIS</span></span>
<span data-ttu-id="15d29-103">Ön kapıda içeriği kaldır</span><span class="sxs-lookup"><span data-stu-id="15d29-103">Remove contents in Front Door</span></span>

## <span data-ttu-id="15d29-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15d29-104">SYNTAX</span></span>

```
Remove-AzFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15d29-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="15d29-105">DESCRIPTION</span></span>
<span data-ttu-id="15d29-106">Remove-AzFrontDoorContent ön kapıda önbellekteki içeriği temizler</span><span class="sxs-lookup"><span data-stu-id="15d29-106">Remove-AzFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="15d29-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15d29-107">EXAMPLES</span></span>

### <span data-ttu-id="15d29-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="15d29-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="15d29-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15d29-109">PARAMETERS</span></span>

### <span data-ttu-id="15d29-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="15d29-110">-ContentPath</span></span>
<span data-ttu-id="15d29-111">Temizlenecek içeriğin yolları.</span><span class="sxs-lookup"><span data-stu-id="15d29-111">The paths to the content to be purged.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15d29-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15d29-112">-DefaultProfile</span></span>
<span data-ttu-id="15d29-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="15d29-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15d29-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="15d29-114">-Name</span></span>
<span data-ttu-id="15d29-115">Ön kapı adı.</span><span class="sxs-lookup"><span data-stu-id="15d29-115">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15d29-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="15d29-116">-PassThru</span></span>
<span data-ttu-id="15d29-117">Return Object (belirtilmişse).</span><span class="sxs-lookup"><span data-stu-id="15d29-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="15d29-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15d29-118">-ResourceGroupName</span></span>
<span data-ttu-id="15d29-119">Ön kapı kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="15d29-119">The resource group name of the Front Door</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15d29-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="15d29-120">-Confirm</span></span>
<span data-ttu-id="15d29-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="15d29-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15d29-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15d29-122">-WhatIf</span></span>
<span data-ttu-id="15d29-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="15d29-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15d29-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="15d29-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15d29-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15d29-125">CommonParameters</span></span>
<span data-ttu-id="15d29-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15d29-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15d29-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="15d29-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15d29-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15d29-128">INPUTS</span></span>

### <span data-ttu-id="15d29-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="15d29-129">None</span></span>

## <span data-ttu-id="15d29-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15d29-130">OUTPUTS</span></span>

### <span data-ttu-id="15d29-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="15d29-131">System.Boolean</span></span>

## <span data-ttu-id="15d29-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15d29-132">NOTES</span></span>

## <span data-ttu-id="15d29-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15d29-133">RELATED LINKS</span></span>
