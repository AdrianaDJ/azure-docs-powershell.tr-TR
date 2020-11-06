---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorContent.md
ms.openlocfilehash: c75d8bca528c954cf0612af3392fc79f3cd3b4a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572750"
---
# <span data-ttu-id="5fb88-101">Remove-AzureRmFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="5fb88-101">Remove-AzureRmFrontDoorContent</span></span>

## <span data-ttu-id="5fb88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fb88-102">SYNOPSIS</span></span>
<span data-ttu-id="5fb88-103">Ön kapıda içeriği kaldır</span><span class="sxs-lookup"><span data-stu-id="5fb88-103">Remove contents in Front Door</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fb88-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5fb88-104">SYNTAX</span></span>

```
Remove-AzureRmFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fb88-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5fb88-105">DESCRIPTION</span></span>
<span data-ttu-id="5fb88-106">Remove-AzureRmFrontDoorContent ön kapıda önbellekteki içeriği temizler</span><span class="sxs-lookup"><span data-stu-id="5fb88-106">Remove-AzureRmFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="5fb88-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5fb88-107">EXAMPLES</span></span>

### <span data-ttu-id="5fb88-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5fb88-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="5fb88-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5fb88-109">PARAMETERS</span></span>

### <span data-ttu-id="5fb88-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="5fb88-110">-ContentPath</span></span>
<span data-ttu-id="5fb88-111">Temizlenecek içeriğin yolları.</span><span class="sxs-lookup"><span data-stu-id="5fb88-111">The paths to the content to be purged.</span></span>

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

### <span data-ttu-id="5fb88-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fb88-112">-DefaultProfile</span></span>
<span data-ttu-id="5fb88-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5fb88-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fb88-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="5fb88-114">-Name</span></span>
<span data-ttu-id="5fb88-115">Ön kapı adı.</span><span class="sxs-lookup"><span data-stu-id="5fb88-115">Front Door name.</span></span>

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

### <span data-ttu-id="5fb88-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5fb88-116">-PassThru</span></span>
<span data-ttu-id="5fb88-117">Return Object (belirtilmişse).</span><span class="sxs-lookup"><span data-stu-id="5fb88-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="5fb88-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fb88-118">-ResourceGroupName</span></span>
<span data-ttu-id="5fb88-119">Ön kapı kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="5fb88-119">The resource group name of the Front Door</span></span>

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

### <span data-ttu-id="5fb88-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="5fb88-120">-Confirm</span></span>
<span data-ttu-id="5fb88-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5fb88-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fb88-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fb88-122">-WhatIf</span></span>
<span data-ttu-id="5fb88-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5fb88-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fb88-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5fb88-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fb88-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fb88-125">CommonParameters</span></span>
<span data-ttu-id="5fb88-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5fb88-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fb88-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fb88-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fb88-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5fb88-128">INPUTS</span></span>

### <span data-ttu-id="5fb88-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5fb88-129">None</span></span>

## <span data-ttu-id="5fb88-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5fb88-130">OUTPUTS</span></span>

### <span data-ttu-id="5fb88-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5fb88-131">System.Boolean</span></span>

## <span data-ttu-id="5fb88-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5fb88-132">NOTES</span></span>

## <span data-ttu-id="5fb88-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5fb88-133">RELATED LINKS</span></span>
