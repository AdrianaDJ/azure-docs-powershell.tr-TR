---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: e0e74aa910c11a10c26cf6bed623d2e2c02f93ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588615"
---
# <span data-ttu-id="796f6-101">Remove-AzureRmAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="796f6-101">Remove-AzureRmAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="796f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="796f6-102">SYNOPSIS</span></span>
<span data-ttu-id="796f6-103">Azure Otomasyonu yazılım güncelleştirme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="796f6-103">Removes an azure automation software update configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="796f6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="796f6-104">SYNTAX</span></span>

### <span data-ttu-id="796f6-105">BySucName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="796f6-105">BySucName (Default)</span></span>
```
Remove-AzureRmAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="796f6-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="796f6-106">BySuc</span></span>
```
Remove-AzureRmAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="796f6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="796f6-107">DESCRIPTION</span></span>
<span data-ttu-id="796f6-108">Bu cmdlet bir Azure Otomasyonu yazılım güncelleştirme yapılandırmasını kaldırdı.</span><span class="sxs-lookup"><span data-stu-id="796f6-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="796f6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="796f6-109">EXAMPLES</span></span>

### <span data-ttu-id="796f6-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="796f6-110">Example 1</span></span>
<span data-ttu-id="796f6-111">Bu örnekte, ' MyUpdateConfiguration ' öğesinin Otomasyon hesabından kaldırılması gösterilmektedir</span><span class="sxs-lookup"><span data-stu-id="796f6-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzureRmAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="796f6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="796f6-112">PARAMETERS</span></span>

### <span data-ttu-id="796f6-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="796f6-113">-AutomationAccountName</span></span>
<span data-ttu-id="796f6-114">Otomasyon hesap adı.</span><span class="sxs-lookup"><span data-stu-id="796f6-114">The automation account name.</span></span>

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

### <span data-ttu-id="796f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="796f6-115">-DefaultProfile</span></span>
<span data-ttu-id="796f6-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="796f6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="796f6-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="796f6-117">-Name</span></span>
<span data-ttu-id="796f6-118">Kaldırılacak yazılım güncelleştirmesi yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="796f6-118">Name of the software update configuration to remove.</span></span>

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

### <span data-ttu-id="796f6-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="796f6-119">-PassThru</span></span>
<span data-ttu-id="796f6-120">Geçiş, çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="796f6-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="796f6-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="796f6-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="796f6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="796f6-122">-ResourceGroupName</span></span>
<span data-ttu-id="796f6-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="796f6-123">The resource group name.</span></span>

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

### <span data-ttu-id="796f6-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="796f6-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="796f6-125">Kaldırılacak yazılım güncelleştirmesi yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="796f6-125">The software update configuration to remove.</span></span>

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

### <span data-ttu-id="796f6-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="796f6-126">-Confirm</span></span>
<span data-ttu-id="796f6-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="796f6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="796f6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="796f6-128">-WhatIf</span></span>
<span data-ttu-id="796f6-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="796f6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="796f6-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="796f6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="796f6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="796f6-131">CommonParameters</span></span>
<span data-ttu-id="796f6-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="796f6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="796f6-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="796f6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="796f6-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="796f6-134">INPUTS</span></span>

### <span data-ttu-id="796f6-135">System. String</span><span class="sxs-lookup"><span data-stu-id="796f6-135">System.String</span></span>

### <span data-ttu-id="796f6-136">Microsoft. Azure. Commands. Automation. model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="796f6-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="796f6-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="796f6-137">OUTPUTS</span></span>

### <span data-ttu-id="796f6-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="796f6-138">System.Object</span></span>
## <span data-ttu-id="796f6-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="796f6-139">NOTES</span></span>

## <span data-ttu-id="796f6-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="796f6-140">RELATED LINKS</span></span>
