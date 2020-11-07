---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermautoscalesetting
schema: 2.0.0
ms.openlocfilehash: 93c51e71cf912a072daafd721d9e9626ccefbb06
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939371"
---
# <span data-ttu-id="845b5-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="845b5-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="845b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="845b5-102">SYNOPSIS</span></span>
<span data-ttu-id="845b5-103">Otomatik ölçeklendirme ayarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="845b5-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="845b5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="845b5-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="845b5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="845b5-105">DESCRIPTION</span></span>
<span data-ttu-id="845b5-106">**Remove-AzureRmAutoscaleSetting** cmdlet 'ı otomatik ölçeklendirme ayarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="845b5-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="845b5-107">Ayarın adını ve atandığı kaynak grubunun adını belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="845b5-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>
<span data-ttu-id="845b5-108">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="845b5-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="845b5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="845b5-109">EXAMPLES</span></span>

## <span data-ttu-id="845b5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="845b5-110">PARAMETERS</span></span>

### <span data-ttu-id="845b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="845b5-111">-DefaultProfile</span></span>
<span data-ttu-id="845b5-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="845b5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="845b5-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="845b5-113">-Name</span></span>
<span data-ttu-id="845b5-114">Kaldırılacak otomatik ölçeklendirme ayarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="845b5-114">Specifies the name of the Autoscale setting to remove.</span></span>

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

### <span data-ttu-id="845b5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="845b5-115">-ResourceGroupName</span></span>
<span data-ttu-id="845b5-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="845b5-116">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="845b5-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="845b5-117">-Confirm</span></span>
<span data-ttu-id="845b5-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="845b5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="845b5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="845b5-119">-WhatIf</span></span>
<span data-ttu-id="845b5-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="845b5-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="845b5-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="845b5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="845b5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="845b5-122">CommonParameters</span></span>
<span data-ttu-id="845b5-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="845b5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="845b5-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="845b5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="845b5-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="845b5-125">INPUTS</span></span>

### <span data-ttu-id="845b5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="845b5-126">System.String</span></span>

## <span data-ttu-id="845b5-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="845b5-127">OUTPUTS</span></span>

### <span data-ttu-id="845b5-128">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="845b5-128">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="845b5-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="845b5-129">NOTES</span></span>

## <span data-ttu-id="845b5-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="845b5-130">RELATED LINKS</span></span>

[<span data-ttu-id="845b5-131">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="845b5-131">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="845b5-132">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="845b5-132">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)


