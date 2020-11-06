---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 2cd60a70b057689cf7edf154df28253b86e110a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591169"
---
# <span data-ttu-id="7a28f-101">Remove-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a28f-101">Remove-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="7a28f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a28f-102">SYNOPSIS</span></span>
<span data-ttu-id="7a28f-103">Otomasyondan DSC yapılandırmalarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7a28f-103">Removes DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a28f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7a28f-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a28f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7a28f-105">DESCRIPTION</span></span>
<span data-ttu-id="7a28f-106">**Remove-AzureRmAutomationDscConfiguration** cmdlet 'ı, AP 'ler için APS</span><span class="sxs-lookup"><span data-stu-id="7a28f-106">The **Remove-AzureRmAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="7a28f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7a28f-107">EXAMPLES</span></span>

## <span data-ttu-id="7a28f-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7a28f-108">PARAMETERS</span></span>

### <span data-ttu-id="7a28f-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7a28f-109">-AutomationAccountName</span></span>
<span data-ttu-id="7a28f-110">Bu cmdlet 'in kaldırdığı DSC yapılandırmalarını içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a28f-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7a28f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="7a28f-111">-Force</span></span>
<span data-ttu-id="7a28f-112">ps_force</span><span class="sxs-lookup"><span data-stu-id="7a28f-112">ps_force</span></span>

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

### <span data-ttu-id="7a28f-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="7a28f-113">-Name</span></span>
<span data-ttu-id="7a28f-114">Bu cmdlet 'in kaldırıldığı DSC yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a28f-114">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7a28f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a28f-115">-ResourceGroupName</span></span>
<span data-ttu-id="7a28f-116">Bu cmdlet 'in DSC yapılandırmalarını aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a28f-116">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="7a28f-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="7a28f-117">-Confirm</span></span>
<span data-ttu-id="7a28f-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7a28f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a28f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a28f-119">-WhatIf</span></span>
<span data-ttu-id="7a28f-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7a28f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a28f-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7a28f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a28f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a28f-122">-DefaultProfile</span></span>
<span data-ttu-id="7a28f-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7a28f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a28f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a28f-124">CommonParameters</span></span>
<span data-ttu-id="7a28f-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7a28f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a28f-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a28f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a28f-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7a28f-127">INPUTS</span></span>

## <span data-ttu-id="7a28f-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7a28f-128">OUTPUTS</span></span>

## <span data-ttu-id="7a28f-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7a28f-129">NOTES</span></span>

## <span data-ttu-id="7a28f-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7a28f-130">RELATED LINKS</span></span>

[<span data-ttu-id="7a28f-131">Dışarı aktarma-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a28f-131">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="7a28f-132">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a28f-132">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="7a28f-133">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a28f-133">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


