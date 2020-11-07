---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
ms.openlocfilehash: 03df484687d4f26612bbb3af4f10da7bfa1352e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752811"
---
# <span data-ttu-id="776b8-101">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="776b8-101">Remove-AzContainerService</span></span>

## <span data-ttu-id="776b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="776b8-102">SYNOPSIS</span></span>
<span data-ttu-id="776b8-103">Kapsayıcı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="776b8-103">Removes a container service.</span></span>

## <span data-ttu-id="776b8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="776b8-104">SYNTAX</span></span>

```
Remove-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="776b8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="776b8-105">DESCRIPTION</span></span>
<span data-ttu-id="776b8-106">**Remove-AzContainerService** cmdlet 'i Azure hesabınızdan bir kapsayıcı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="776b8-106">The **Remove-AzContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="776b8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="776b8-107">EXAMPLES</span></span>

### <span data-ttu-id="776b8-108">Örnek 1: kapsayıcı hizmeti kaldırma</span><span class="sxs-lookup"><span data-stu-id="776b8-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="776b8-109">Bu komut, CSResourceGroup17 adlı kapsayıcı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="776b8-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="776b8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="776b8-110">PARAMETERS</span></span>

### <span data-ttu-id="776b8-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="776b8-111">-AsJob</span></span>
<span data-ttu-id="776b8-112">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="776b8-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="776b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="776b8-113">-DefaultProfile</span></span>
<span data-ttu-id="776b8-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="776b8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="776b8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="776b8-115">-Force</span></span>
<span data-ttu-id="776b8-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="776b8-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="776b8-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="776b8-117">-Name</span></span>
<span data-ttu-id="776b8-118">Bu cmdlet 'in kaldırdığı kapsayıcı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="776b8-118">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="776b8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="776b8-119">-ResourceGroupName</span></span>
<span data-ttu-id="776b8-120">Bu cmdlet 'in kaldırdığı kapsayıcı hizmetin kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="776b8-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="776b8-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="776b8-121">-Confirm</span></span>
<span data-ttu-id="776b8-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="776b8-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="776b8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="776b8-123">-WhatIf</span></span>
<span data-ttu-id="776b8-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="776b8-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="776b8-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="776b8-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="776b8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="776b8-126">CommonParameters</span></span>
<span data-ttu-id="776b8-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="776b8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="776b8-128">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="776b8-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="776b8-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="776b8-129">INPUTS</span></span>

### <span data-ttu-id="776b8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="776b8-130">System.String</span></span>

## <span data-ttu-id="776b8-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="776b8-131">OUTPUTS</span></span>

### <span data-ttu-id="776b8-132">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="776b8-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="776b8-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="776b8-133">NOTES</span></span>

## <span data-ttu-id="776b8-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="776b8-134">RELATED LINKS</span></span>

[<span data-ttu-id="776b8-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="776b8-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="776b8-136">Yeni-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="776b8-136">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="776b8-137">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="776b8-137">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


