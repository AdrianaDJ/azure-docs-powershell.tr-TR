---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6C6C7142-31CD-4245-BC55-CB7916EA12E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 938fde14fb62ea7f7fd4e04baf5e309615957799
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761531"
---
# <span data-ttu-id="2e5cc-101">Remove-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e5cc-101">Remove-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="2e5cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e5cc-102">SYNOPSIS</span></span>
<span data-ttu-id="2e5cc-103">Veri kaynağı yapılandırmalarından Otomasyon 'daki meta verileri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2e5cc-103">Removes metadata from DSC node configurations in Automation.</span></span>

## <span data-ttu-id="2e5cc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e5cc-104">SYNTAX</span></span>

```
Remove-AzAutomationDscNodeConfiguration [-Name] <String> [-Force] [-IgnoreNodeMappings]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e5cc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e5cc-105">DESCRIPTION</span></span>
<span data-ttu-id="2e5cc-106">**Remove-AzAutomationDscNodeConfiguration** cmdlet 'ı, AP 'ler</span><span class="sxs-lookup"><span data-stu-id="2e5cc-106">The **Remove-AzAutomationDscNodeConfiguration** cmdlet removes metadata from APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="2e5cc-107">Automation, DSC düğüm yapılandırmasını yönetilen nesne biçimi (MOF) yapılandırma belgesi olarak depolar.</span><span class="sxs-lookup"><span data-stu-id="2e5cc-107">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="2e5cc-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e5cc-108">EXAMPLES</span></span>

## <span data-ttu-id="2e5cc-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e5cc-109">PARAMETERS</span></span>

### <span data-ttu-id="2e5cc-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2e5cc-110">-AutomationAccountName</span></span>
<span data-ttu-id="2e5cc-111">Bu cmdlet 'in meta verileri kaldırdığı DSC düğüm yapılandırmalarını içeren bir Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e5cc-111">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet removes metadata.</span></span>

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

### <span data-ttu-id="2e5cc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e5cc-112">-DefaultProfile</span></span>
<span data-ttu-id="2e5cc-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2e5cc-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e5cc-114">-Force</span><span class="sxs-lookup"><span data-stu-id="2e5cc-114">-Force</span></span>
<span data-ttu-id="2e5cc-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="2e5cc-115">ps_force</span></span>

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

### <span data-ttu-id="2e5cc-116">-Ignorenodemappings</span><span class="sxs-lookup"><span data-stu-id="2e5cc-116">-IgnoreNodeMappings</span></span>
<span data-ttu-id="2e5cc-117">Bu cmdlet 'in düğüm eşlemelerini yoksaydiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e5cc-117">Indicates that this cmdlet ignores node mappings.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e5cc-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="2e5cc-118">-Name</span></span>
<span data-ttu-id="2e5cc-119">Bu cmdlet 'in meta verileri kaldırdığı DSC düğüm yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e5cc-119">Specifies the name of the DSC node configuration for which this cmdlet removes metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e5cc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e5cc-120">-ResourceGroupName</span></span>
<span data-ttu-id="2e5cc-121">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e5cc-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="2e5cc-122">Bu cmdlet, bu parametrenin belirttiği kaynak grubundaki DSC düğüm yapılandırmalarının meta verilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2e5cc-122">This cmdlet removes metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2e5cc-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="2e5cc-123">-Confirm</span></span>
<span data-ttu-id="2e5cc-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2e5cc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e5cc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e5cc-125">-WhatIf</span></span>
<span data-ttu-id="2e5cc-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2e5cc-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e5cc-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2e5cc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e5cc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e5cc-128">CommonParameters</span></span>
<span data-ttu-id="2e5cc-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e5cc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e5cc-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e5cc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e5cc-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e5cc-131">INPUTS</span></span>

### <span data-ttu-id="2e5cc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2e5cc-132">System.String</span></span>

## <span data-ttu-id="2e5cc-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e5cc-133">OUTPUTS</span></span>

### <span data-ttu-id="2e5cc-134">System. void</span><span class="sxs-lookup"><span data-stu-id="2e5cc-134">System.Void</span></span>

## <span data-ttu-id="2e5cc-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e5cc-135">NOTES</span></span>

## <span data-ttu-id="2e5cc-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e5cc-136">RELATED LINKS</span></span>

[<span data-ttu-id="2e5cc-137">Get-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e5cc-137">Get-AzAutomationDscNodeConfiguration</span></span>](./Get-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="2e5cc-138">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e5cc-138">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="2e5cc-139">Azure Otomasyonu cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="2e5cc-139">Azure Automation Cmdlets</span></span>](./Az.Automation.md)


