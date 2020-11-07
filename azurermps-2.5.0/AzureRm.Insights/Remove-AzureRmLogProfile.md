---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermlogprofile
schema: 2.0.0
ms.openlocfilehash: 78d2bff42382564bb07f680b5db8db39707ffb97
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938862"
---
# <span data-ttu-id="6bbd5-101">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="6bbd5-101">Remove-AzureRmLogProfile</span></span>

## <span data-ttu-id="6bbd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bbd5-102">SYNOPSIS</span></span>
<span data-ttu-id="6bbd5-103">Günlük profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6bbd5-103">Removes a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bbd5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6bbd5-104">SYNTAX</span></span>

```
Remove-AzureRmLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bbd5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6bbd5-105">DESCRIPTION</span></span>
<span data-ttu-id="6bbd5-106">**Remove-AzureRmLogProfile** cmdlet 'i, günlük profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6bbd5-106">The **Remove-AzureRmLogProfile** cmdlet removes a log profile.</span></span>
<span data-ttu-id="6bbd5-107">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="6bbd5-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="6bbd5-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6bbd5-108">EXAMPLES</span></span>

## <span data-ttu-id="6bbd5-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6bbd5-109">PARAMETERS</span></span>

### <span data-ttu-id="6bbd5-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bbd5-110">-DefaultProfile</span></span>
<span data-ttu-id="6bbd5-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6bbd5-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6bbd5-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="6bbd5-112">-Name</span></span>
<span data-ttu-id="6bbd5-113">Kaldırılacak günlük profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bbd5-113">Specifies the name of the log profile to remove.</span></span>

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

### <span data-ttu-id="6bbd5-114">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6bbd5-114">-PassThru</span></span>
<span data-ttu-id="6bbd5-115">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="6bbd5-115">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6bbd5-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="6bbd5-116">-Confirm</span></span>
<span data-ttu-id="6bbd5-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6bbd5-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bbd5-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bbd5-118">-WhatIf</span></span>
<span data-ttu-id="6bbd5-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6bbd5-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6bbd5-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6bbd5-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bbd5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bbd5-121">CommonParameters</span></span>
<span data-ttu-id="6bbd5-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6bbd5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bbd5-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bbd5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bbd5-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6bbd5-124">INPUTS</span></span>

### <span data-ttu-id="6bbd5-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6bbd5-125">System.String</span></span>

## <span data-ttu-id="6bbd5-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6bbd5-126">OUTPUTS</span></span>

### <span data-ttu-id="6bbd5-127">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6bbd5-127">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="6bbd5-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6bbd5-128">NOTES</span></span>

## <span data-ttu-id="6bbd5-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6bbd5-129">RELATED LINKS</span></span>

[<span data-ttu-id="6bbd5-130">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="6bbd5-130">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="6bbd5-131">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="6bbd5-131">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)


