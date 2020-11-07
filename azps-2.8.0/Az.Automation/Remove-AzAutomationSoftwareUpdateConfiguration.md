---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: 3b608feb9ed496be72d1d74f4a5a2be0569714de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753236"
---
# <span data-ttu-id="9bb74-101">Remove-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="9bb74-101">Remove-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="9bb74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bb74-102">SYNOPSIS</span></span>
<span data-ttu-id="9bb74-103">Azure Otomasyonu yazılım güncelleştirme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9bb74-103">Removes an azure automation software update configuration.</span></span>

## <span data-ttu-id="9bb74-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9bb74-104">SYNTAX</span></span>

### <span data-ttu-id="9bb74-105">BySucName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9bb74-105">BySucName (Default)</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9bb74-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="9bb74-106">BySuc</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bb74-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9bb74-107">DESCRIPTION</span></span>
<span data-ttu-id="9bb74-108">Bu cmdlet bir Azure Otomasyonu yazılım güncelleştirme yapılandırmasını kaldırdı.</span><span class="sxs-lookup"><span data-stu-id="9bb74-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="9bb74-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9bb74-109">EXAMPLES</span></span>

### <span data-ttu-id="9bb74-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9bb74-110">Example 1</span></span>
<span data-ttu-id="9bb74-111">Bu örnekte, ' MyUpdateConfiguration ' öğesinin Otomasyon hesabından kaldırılması gösterilmektedir</span><span class="sxs-lookup"><span data-stu-id="9bb74-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="9bb74-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9bb74-112">PARAMETERS</span></span>

### <span data-ttu-id="9bb74-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9bb74-113">-AutomationAccountName</span></span>
<span data-ttu-id="9bb74-114">Otomasyon hesap adı.</span><span class="sxs-lookup"><span data-stu-id="9bb74-114">The automation account name.</span></span>

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

### <span data-ttu-id="9bb74-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bb74-115">-DefaultProfile</span></span>
<span data-ttu-id="9bb74-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9bb74-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bb74-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="9bb74-117">-Name</span></span>
<span data-ttu-id="9bb74-118">Kaldırılacak yazılım güncelleştirmesi yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="9bb74-118">Name of the software update configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: BySucName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bb74-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9bb74-119">-PassThru</span></span>
<span data-ttu-id="9bb74-120">Geçiş, çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="9bb74-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="9bb74-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="9bb74-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9bb74-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bb74-122">-ResourceGroupName</span></span>
<span data-ttu-id="9bb74-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9bb74-123">The resource group name.</span></span>

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

### <span data-ttu-id="9bb74-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="9bb74-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="9bb74-125">Kaldırılacak yazılım güncelleştirmesi yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="9bb74-125">The software update configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration
Parameter Sets: BySuc
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bb74-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="9bb74-126">-Confirm</span></span>
<span data-ttu-id="9bb74-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9bb74-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bb74-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bb74-128">-WhatIf</span></span>
<span data-ttu-id="9bb74-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9bb74-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bb74-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9bb74-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bb74-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bb74-131">CommonParameters</span></span>
<span data-ttu-id="9bb74-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9bb74-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bb74-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bb74-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bb74-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9bb74-134">INPUTS</span></span>

### <span data-ttu-id="9bb74-135">System. String</span><span class="sxs-lookup"><span data-stu-id="9bb74-135">System.String</span></span>

### <span data-ttu-id="9bb74-136">Microsoft. Azure. Commands. Automation. model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="9bb74-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="9bb74-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9bb74-137">OUTPUTS</span></span>

### <span data-ttu-id="9bb74-138">System. void</span><span class="sxs-lookup"><span data-stu-id="9bb74-138">System.Void</span></span>

### <span data-ttu-id="9bb74-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9bb74-139">System.Boolean</span></span>

## <span data-ttu-id="9bb74-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9bb74-140">NOTES</span></span>

## <span data-ttu-id="9bb74-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9bb74-141">RELATED LINKS</span></span>
