---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 4dceb934f5cf746908c289c7662de0dc3dae09a5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096871"
---
# <span data-ttu-id="ea8fc-101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ea8fc-101">Remove-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="ea8fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea8fc-102">SYNOPSIS</span></span>
<span data-ttu-id="ea8fc-103">Tümleştirme hesabı derlemesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ea8fc-103">Removes an integration account assembly.</span></span>

## <span data-ttu-id="ea8fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ea8fc-104">SYNTAX</span></span>

### <span data-ttu-id="ea8fc-105">Byıntegrationaccount (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ea8fc-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea8fc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ea8fc-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea8fc-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="ea8fc-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea8fc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ea8fc-108">DESCRIPTION</span></span>
<span data-ttu-id="ea8fc-109">**Remove-AzIntegrationAccountAssembly** cmdlet 'i, tümleştirme hesabından derleme kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ea8fc-109">The **Remove-AzIntegrationAccountAssembly** cmdlet removes an assembly from an integration account.</span></span>

## <span data-ttu-id="ea8fc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ea8fc-110">EXAMPLES</span></span>

### <span data-ttu-id="ea8fc-111">Örnek 1: bir derlemeyi parametrelerle kaldırma</span><span class="sxs-lookup"><span data-stu-id="ea8fc-111">Example 1: Remove an assembly by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"
```

<span data-ttu-id="ea8fc-112">"Sampleıntegrationaccount" tümleştirme hesabında bulunan "sampleAssembly" adlı derlemeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ea8fc-112">Removes the assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="ea8fc-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ea8fc-113">PARAMETERS</span></span>

### <span data-ttu-id="ea8fc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea8fc-114">-DefaultProfile</span></span>
<span data-ttu-id="ea8fc-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ea8fc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea8fc-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea8fc-116">-InputObject</span></span>
<span data-ttu-id="ea8fc-117">Tümleştirme hesabı derlemesi.</span><span class="sxs-lookup"><span data-stu-id="ea8fc-117">An integration account assembly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea8fc-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="ea8fc-118">-Name</span></span>
<span data-ttu-id="ea8fc-119">Tümleştirme hesabı derleme adı.</span><span class="sxs-lookup"><span data-stu-id="ea8fc-119">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8fc-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="ea8fc-120">-ParentName</span></span>
<span data-ttu-id="ea8fc-121">Tümleştirme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="ea8fc-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8fc-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ea8fc-122">-PassThru</span></span>
<span data-ttu-id="ea8fc-123">Komutun başarılı olup olmadığını döndürün.</span><span class="sxs-lookup"><span data-stu-id="ea8fc-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="ea8fc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea8fc-124">-ResourceGroupName</span></span>
<span data-ttu-id="ea8fc-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ea8fc-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8fc-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ea8fc-126">-ResourceId</span></span>
<span data-ttu-id="ea8fc-127">Tümleştirme hesabı derleme kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="ea8fc-127">The integration account assembly resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea8fc-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="ea8fc-128">-Confirm</span></span>
<span data-ttu-id="ea8fc-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ea8fc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea8fc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea8fc-130">-WhatIf</span></span>
<span data-ttu-id="ea8fc-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ea8fc-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea8fc-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ea8fc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea8fc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea8fc-133">CommonParameters</span></span>
<span data-ttu-id="ea8fc-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ea8fc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea8fc-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea8fc-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea8fc-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ea8fc-136">INPUTS</span></span>

### <span data-ttu-id="ea8fc-137">Microsoft. Azure. Commands. Logicuyg. modeller. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ea8fc-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="ea8fc-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ea8fc-138">System.String</span></span>

## <span data-ttu-id="ea8fc-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ea8fc-139">OUTPUTS</span></span>

### <span data-ttu-id="ea8fc-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ea8fc-140">System.Boolean</span></span>

## <span data-ttu-id="ea8fc-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ea8fc-141">NOTES</span></span>

## <span data-ttu-id="ea8fc-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ea8fc-142">RELATED LINKS</span></span>
