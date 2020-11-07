---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscConfiguration.md
ms.openlocfilehash: 1a556a92d59830a4be331c8415fde0c85ddba539
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761532"
---
# <span data-ttu-id="adb52-101">Remove-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="adb52-101">Remove-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="adb52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adb52-102">SYNOPSIS</span></span>
<span data-ttu-id="adb52-103">Otomasyondan DSC yapılandırmalarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="adb52-103">Removes DSC configurations from Automation.</span></span>

## <span data-ttu-id="adb52-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="adb52-104">SYNTAX</span></span>

```
Remove-AzAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="adb52-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="adb52-105">DESCRIPTION</span></span>
<span data-ttu-id="adb52-106">**Remove-AzAutomationDscConfiguration** cmdlet 'ı, APS</span><span class="sxs-lookup"><span data-stu-id="adb52-106">The **Remove-AzAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="adb52-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="adb52-107">EXAMPLES</span></span>

## <span data-ttu-id="adb52-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="adb52-108">PARAMETERS</span></span>

### <span data-ttu-id="adb52-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="adb52-109">-AutomationAccountName</span></span>
<span data-ttu-id="adb52-110">Bu cmdlet 'in kaldırdığı DSC yapılandırmalarını içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="adb52-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

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

### <span data-ttu-id="adb52-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adb52-111">-DefaultProfile</span></span>
<span data-ttu-id="adb52-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="adb52-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="adb52-113">-Force</span><span class="sxs-lookup"><span data-stu-id="adb52-113">-Force</span></span>
<span data-ttu-id="adb52-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="adb52-114">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adb52-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="adb52-115">-Name</span></span>
<span data-ttu-id="adb52-116">Bu cmdlet 'in kaldırıldığı DSC yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="adb52-116">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adb52-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adb52-117">-ResourceGroupName</span></span>
<span data-ttu-id="adb52-118">Bu cmdlet 'in DSC yapılandırmalarını aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="adb52-118">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="adb52-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="adb52-119">-Confirm</span></span>
<span data-ttu-id="adb52-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="adb52-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adb52-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adb52-121">-WhatIf</span></span>
<span data-ttu-id="adb52-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="adb52-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adb52-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="adb52-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adb52-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adb52-124">CommonParameters</span></span>
<span data-ttu-id="adb52-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="adb52-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adb52-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adb52-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adb52-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="adb52-127">INPUTS</span></span>

### <span data-ttu-id="adb52-128">System. String</span><span class="sxs-lookup"><span data-stu-id="adb52-128">System.String</span></span>

## <span data-ttu-id="adb52-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="adb52-129">OUTPUTS</span></span>

### <span data-ttu-id="adb52-130">System. void</span><span class="sxs-lookup"><span data-stu-id="adb52-130">System.Void</span></span>

## <span data-ttu-id="adb52-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="adb52-131">NOTES</span></span>

## <span data-ttu-id="adb52-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="adb52-132">RELATED LINKS</span></span>

[<span data-ttu-id="adb52-133">Dışarı aktarma-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="adb52-133">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="adb52-134">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="adb52-134">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="adb52-135">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="adb52-135">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


