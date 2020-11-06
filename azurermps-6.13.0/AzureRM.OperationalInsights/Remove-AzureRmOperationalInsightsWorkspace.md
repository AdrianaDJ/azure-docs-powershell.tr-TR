---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 5a222b404aa931cec468ee5dfc66963f48b23ada
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587221"
---
# <span data-ttu-id="638a4-101">Remove-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="638a4-101">Remove-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="638a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="638a4-102">SYNOPSIS</span></span>
<span data-ttu-id="638a4-103">Çalışma alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="638a4-103">Removes a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="638a4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="638a4-104">SYNTAX</span></span>

```
Remove-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="638a4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="638a4-105">DESCRIPTION</span></span>
<span data-ttu-id="638a4-106">**Remove-Azurermoperationalınsightsworkspace** cmdlet 'i var olan bir çalışma alanını siler.</span><span class="sxs-lookup"><span data-stu-id="638a4-106">The **Remove-AzureRmOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="638a4-107">Bu çalışma alanı, oluşturma sırasında *MüşteriNo* parametresi aracılığıyla varolan bir hesaba bağlanmışsa, çalışma</span><span class="sxs-lookup"><span data-stu-id="638a4-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="638a4-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="638a4-108">EXAMPLES</span></span>

### <span data-ttu-id="638a4-109">Örnek 1: çalışma alanını adla kaldırma</span><span class="sxs-lookup"><span data-stu-id="638a4-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="638a4-110">Bu komut MyWorkspace adlı çalışma alanını ContosoResourceGroup adlı kaynak grubundan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="638a4-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="638a4-111">Örnek 2: ardışık düzeni kullanarak bir çalışma alanını kaldırma</span><span class="sxs-lookup"><span data-stu-id="638a4-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzureRmOperationalInsightsWorkspace -Force
```

<span data-ttu-id="638a4-112">Bu komut MyWorkspace adlı çalışma alanını almak için Get-AzureRmOperationalInsightsWorkspace cmdlet 'ini kullanır ve ardından bunu kaldırmak için ardışık düzen işlecini kullanarak Remove **-Azurermoperationalınsightsworkspace** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="638a4-112">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="638a4-113">*Force* parametresi belirtildiğinden, komut çalışma alanını kaldırmadan önce sizi istemez.</span><span class="sxs-lookup"><span data-stu-id="638a4-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

## <span data-ttu-id="638a4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="638a4-114">PARAMETERS</span></span>

### <span data-ttu-id="638a4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="638a4-115">-DefaultProfile</span></span>
<span data-ttu-id="638a4-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="638a4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="638a4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="638a4-117">-Force</span></span>
<span data-ttu-id="638a4-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="638a4-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="638a4-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="638a4-119">-Name</span></span>
<span data-ttu-id="638a4-120">Çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="638a4-120">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="638a4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="638a4-121">-ResourceGroupName</span></span>
<span data-ttu-id="638a4-122">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="638a4-122">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="638a4-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="638a4-123">-Confirm</span></span>
<span data-ttu-id="638a4-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="638a4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="638a4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="638a4-125">-WhatIf</span></span>
<span data-ttu-id="638a4-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="638a4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="638a4-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="638a4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="638a4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="638a4-128">CommonParameters</span></span>
<span data-ttu-id="638a4-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="638a4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="638a4-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="638a4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="638a4-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="638a4-131">INPUTS</span></span>

### <span data-ttu-id="638a4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="638a4-132">System.String</span></span>

## <span data-ttu-id="638a4-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="638a4-133">OUTPUTS</span></span>

### <span data-ttu-id="638a4-134">System. void</span><span class="sxs-lookup"><span data-stu-id="638a4-134">System.Void</span></span>

## <span data-ttu-id="638a4-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="638a4-135">NOTES</span></span>

## <span data-ttu-id="638a4-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="638a4-136">RELATED LINKS</span></span>

[<span data-ttu-id="638a4-137">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="638a4-137">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="638a4-138">Get-Azurermoperationalınsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="638a4-138">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


