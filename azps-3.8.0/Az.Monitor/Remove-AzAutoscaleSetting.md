---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAutoscaleSetting.md
ms.openlocfilehash: 5b07928b78c8a6513e91c9e8ec21dbc27294552e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095852"
---
# <span data-ttu-id="9f618-101">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9f618-101">Remove-AzAutoscaleSetting</span></span>

## <span data-ttu-id="9f618-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f618-102">SYNOPSIS</span></span>
<span data-ttu-id="9f618-103">Otomatik ölçeklendirme ayarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9f618-103">Removes an Autoscale setting.</span></span>

## <span data-ttu-id="9f618-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9f618-104">SYNTAX</span></span>

```
Remove-AzAutoscaleSetting -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f618-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9f618-105">DESCRIPTION</span></span>
<span data-ttu-id="9f618-106">**Remove-AzAutoscaleSetting** cmdlet 'ı otomatik ölçeklendirme ayarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9f618-106">The **Remove-AzAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="9f618-107">Ayarın adını ve atandığı kaynak grubunun adını belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="9f618-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>
<span data-ttu-id="9f618-108">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="9f618-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="9f618-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9f618-109">EXAMPLES</span></span>

## <span data-ttu-id="9f618-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9f618-110">PARAMETERS</span></span>

### <span data-ttu-id="9f618-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f618-111">-DefaultProfile</span></span>
<span data-ttu-id="9f618-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9f618-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f618-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="9f618-113">-Name</span></span>
<span data-ttu-id="9f618-114">Kaldırılacak otomatik ölçeklendirme ayarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f618-114">Specifies the name of the Autoscale setting to remove.</span></span>

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

### <span data-ttu-id="9f618-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f618-115">-ResourceGroupName</span></span>
<span data-ttu-id="9f618-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f618-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9f618-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="9f618-117">-Confirm</span></span>
<span data-ttu-id="9f618-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9f618-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f618-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f618-119">-WhatIf</span></span>
<span data-ttu-id="9f618-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9f618-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9f618-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9f618-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f618-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f618-122">CommonParameters</span></span>
<span data-ttu-id="9f618-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9f618-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f618-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9f618-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f618-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9f618-125">INPUTS</span></span>

### <span data-ttu-id="9f618-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9f618-126">System.String</span></span>

## <span data-ttu-id="9f618-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9f618-127">OUTPUTS</span></span>

### <span data-ttu-id="9f618-128">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9f618-128">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="9f618-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9f618-129">NOTES</span></span>

## <span data-ttu-id="9f618-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9f618-130">RELATED LINKS</span></span>

[<span data-ttu-id="9f618-131">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9f618-131">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="9f618-132">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9f618-132">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)


