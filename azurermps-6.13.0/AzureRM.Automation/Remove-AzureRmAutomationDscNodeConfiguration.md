---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6C6C7142-31CD-4245-BC55-CB7916EA12E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: 60f80f92723bbb66d1bf88c9fd8efea66c8c4e55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588624"
---
# <span data-ttu-id="91e8f-101">Remove-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="91e8f-101">Remove-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="91e8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91e8f-102">SYNOPSIS</span></span>
<span data-ttu-id="91e8f-103">Veri kaynağı yapılandırmalarından Otomasyon 'daki meta verileri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="91e8f-103">Removes metadata from DSC node configurations in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91e8f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="91e8f-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscNodeConfiguration [-Name] <String> [-Force] [-IgnoreNodeMappings]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91e8f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="91e8f-105">DESCRIPTION</span></span>
<span data-ttu-id="91e8f-106">**Remove-AzureRmAutomationDscNodeConfiguration** cmdlet 'ı, AP 'ler</span><span class="sxs-lookup"><span data-stu-id="91e8f-106">The **Remove-AzureRmAutomationDscNodeConfiguration** cmdlet removes metadata from APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="91e8f-107">Automation, DSC düğüm yapılandırmasını yönetilen nesne biçimi (MOF) yapılandırma belgesi olarak depolar.</span><span class="sxs-lookup"><span data-stu-id="91e8f-107">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="91e8f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="91e8f-108">EXAMPLES</span></span>

## <span data-ttu-id="91e8f-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="91e8f-109">PARAMETERS</span></span>

### <span data-ttu-id="91e8f-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="91e8f-110">-AutomationAccountName</span></span>
<span data-ttu-id="91e8f-111">Bu cmdlet 'in meta verileri kaldırdığı DSC düğüm yapılandırmalarını içeren bir Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91e8f-111">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet removes metadata.</span></span>

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

### <span data-ttu-id="91e8f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91e8f-112">-DefaultProfile</span></span>
<span data-ttu-id="91e8f-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="91e8f-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91e8f-114">-Force</span><span class="sxs-lookup"><span data-stu-id="91e8f-114">-Force</span></span>
<span data-ttu-id="91e8f-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="91e8f-115">ps_force</span></span>

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

### <span data-ttu-id="91e8f-116">-Ignorenodemappings</span><span class="sxs-lookup"><span data-stu-id="91e8f-116">-IgnoreNodeMappings</span></span>
<span data-ttu-id="91e8f-117">Bu cmdlet 'in düğüm eşlemelerini yoksaydiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="91e8f-117">Indicates that this cmdlet ignores node mappings.</span></span>

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

### <span data-ttu-id="91e8f-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="91e8f-118">-Name</span></span>
<span data-ttu-id="91e8f-119">Bu cmdlet 'in meta verileri kaldırdığı DSC düğüm yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91e8f-119">Specifies the name of the DSC node configuration for which this cmdlet removes metadata.</span></span>

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

### <span data-ttu-id="91e8f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91e8f-120">-ResourceGroupName</span></span>
<span data-ttu-id="91e8f-121">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91e8f-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="91e8f-122">Bu cmdlet, bu parametrenin belirttiği kaynak grubundaki DSC düğüm yapılandırmalarının meta verilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="91e8f-122">This cmdlet removes metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="91e8f-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="91e8f-123">-Confirm</span></span>
<span data-ttu-id="91e8f-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="91e8f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91e8f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91e8f-125">-WhatIf</span></span>
<span data-ttu-id="91e8f-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="91e8f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91e8f-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="91e8f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91e8f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91e8f-128">CommonParameters</span></span>
<span data-ttu-id="91e8f-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="91e8f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91e8f-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91e8f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91e8f-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="91e8f-131">INPUTS</span></span>

### <span data-ttu-id="91e8f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="91e8f-132">System.String</span></span>

## <span data-ttu-id="91e8f-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="91e8f-133">OUTPUTS</span></span>

### <span data-ttu-id="91e8f-134">System. void</span><span class="sxs-lookup"><span data-stu-id="91e8f-134">System.Void</span></span>

## <span data-ttu-id="91e8f-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="91e8f-135">NOTES</span></span>

## <span data-ttu-id="91e8f-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="91e8f-136">RELATED LINKS</span></span>

[<span data-ttu-id="91e8f-137">Get-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="91e8f-137">Get-AzureRmAutomationDscNodeConfiguration</span></span>](./Get-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="91e8f-138">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="91e8f-138">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="91e8f-139">Azure Otomasyonu cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="91e8f-139">Azure Automation Cmdlets</span></span>](./AzureRM.Automation.md)


